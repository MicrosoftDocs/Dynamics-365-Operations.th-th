---
title: แก้ไขปัญหาการวางแผนหลัก
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับการวางแผนหลัก
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1492854b7d2da480942800e378be9d2bb60bb1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645076"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="b06a2-103">แก้ไขปัญหาการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="b06a2-103">Troubleshoot master planning</span></span>

<span data-ttu-id="b06a2-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="b06a2-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="b06a2-105">การกระจายสูตรการผลิตจะทำงานแตกต่างกันสำหรับใบสั่งผลิตที่ยืนยันและสำหรับใบสั่งผลิตที่ประเมินไว้สำหรับงานที่สร้างขึ้นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b06a2-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b06a2-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="b06a2-106">Issue description</span></span>

<span data-ttu-id="b06a2-107">เมื่อยืนยันใบสั่งผลิตสินค้า จะไม่มีการกระจายเมื่อคุณกระจายสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="b06a2-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="b06a2-108">อย่างไรก็ตาม เมื่อคุณสร้างใบสั่งงานด้วยตนเองแล้วประเมินใบสั่งผลิต จะมีการกระจายสินค้า</span><span class="sxs-lookup"><span data-stu-id="b06a2-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b06a2-109">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b06a2-109">Issue resolution</span></span>

<span data-ttu-id="b06a2-110">ระบบทำงานตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="b06a2-110">The system is working as expected.</span></span> <span data-ttu-id="b06a2-111">การกระจายที่เกิดขึ้นเมื่อยืนยันใบสั่งผลิตจะชี้ไปยังแผนการใบสั่ง แต่ไม่ได้แสดงว่าแผนการใบสั่งจะถูกยืนยันในกรณีนี้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="b06a2-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="b06a2-112">อย่างไรก็ตาม ถ้ามีการประเมินใบสั่งผลิตไว้ การกระจายจะถูกทริกเกอร์จากใบสั่งผลิตที่นำออกใช้ซึ่งไม่มีแผนการใบสั่งอยู่</span><span class="sxs-lookup"><span data-stu-id="b06a2-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="b06a2-113">ค่าความล่าช้าจะไม่ได้รับการอัพเดตเมื่อจัดกำหนดการแผนการใบสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="b06a2-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="b06a2-114">เมื่อต้องการอัพเดตการหน่วงเวลาสำหรับแผนการใบสั่ง ให้เปิดกล่องโต้ตอบ **การจัดกำหนดการใหม่** สำหรับใบสั่งที่วางแผน</span><span class="sxs-lookup"><span data-stu-id="b06a2-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="b06a2-115">บนแท็บด่วน **การกระจาย** โปรดตรวจสอบให้แน่ใจว่า มีการตั้งค่าตัวเลือก **ประมวลผลการกระจายหลังจากจัดกำหนดการใหม่** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="b06a2-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="b06a2-116">การจัดตารางการผลิตระดับการผลิตไม่ได้คำนึงถึงค่าเผื่อความปลอดภัยที่ตั้งค่าไว้ในความครอบคลุมสินค้าสำหรับการจัดหาวัสดุที่โยง</span><span class="sxs-lookup"><span data-stu-id="b06a2-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b06a2-117">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="b06a2-117">Issue description</span></span>

<span data-ttu-id="b06a2-118">การวางแผนหลักจะพิจารณาค่าเผื่อความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="b06a2-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="b06a2-119">อย่างไรก็ตาม ค่าเผื่อความปลอดภัยจะถูกละเว้นเมื่อมีการจัดกำหนดการใบสั่งผลิตที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="b06a2-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b06a2-120">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b06a2-120">Issue resolution</span></span>

<span data-ttu-id="b06a2-121">มีการพิจารณาระยะขอบเฉพาะในระหว่างการวางแผนหลัก ไม่ใช่ระหว่างการจัดตารางการผลิตด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b06a2-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="b06a2-122">ระยะขอบถูกออกแบบมาเพื่อทำหน้าที่เป็นบัฟเฟอร์ระหว่างระยะการวางแผน เพื่อให้ "ค่าเผื่อ" บางประการสำหรับกระบวนการจริง</span><span class="sxs-lookup"><span data-stu-id="b06a2-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="b06a2-123">เพื่อให้ได้ผลลัพธ์ที่ต้องการ คุณสามารถลบค่าเผื่อได้</span><span class="sxs-lookup"><span data-stu-id="b06a2-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="b06a2-124">กระบวนการผลิตต้องได้รับการอัพเดตแล้วเพื่อให้มีเวลาที่ต้องการ (ตัวอย่างเช่น ในขณะที่เวลาในการรอ)</span><span class="sxs-lookup"><span data-stu-id="b06a2-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="b06a2-125">การวางแผนหลักและการจัดกำหนดการด้วยตนเองควรสร้างผลลัพธ์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b06a2-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="b06a2-126">มีการสร้างแผนการใบสั่งถึงแม้ว่าจะมีสินค้าอยู่ในสินค้าคงคลังและใบสั่งผลิตมีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="b06a2-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="b06a2-127">คุณอาจสามารถแก้ไขปัญหานี้ได้โดยการเพิ่มค่า **จำนวนวันค่าบวก** สำหรับกลุ่มที่เกี่ยวข้องในหน้า **กลุ่มความครอบคลุม**</span><span class="sxs-lookup"><span data-stu-id="b06a2-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="b06a2-128">การเปลี่ยนแปลงนี้จะทำให้ระบบตรวจสอบว่าสามารถใช้ปริมาณคงคลังคงเหลือสำหรับความต้องการได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="b06a2-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="b06a2-129">ใบสั่งที่วางแผนไว้ใหม่จะไม่ถูกสร้างขึ้นสำหรับสินค้าที่อยู่ในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b06a2-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="b06a2-130">การวางแผนหลักดูเหมือนจะไม่เคารพข้อจำกัดกำลังการผลิตและมีการจัดกำหนดการมากกว่ากำลังการผลิตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="b06a2-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b06a2-131">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="b06a2-131">Issue description</span></span>

<span data-ttu-id="b06a2-132">เมื่อคุณใช้การจัดตารางการผลิตระดับการดำเนินงานที่มีกำลังการผลิตมีจำกัด และโดยที่กระบวนการผลิตจะระบุการรวมของความต้องการสำหรับทั้งกลุ่มทรัพยากรและทรัพยากรแต่ละรายการ มีโอกาสเล็ก ๆ ของการจองเกินเนื่องจากวิธีการที่อัลกอริทึมตรวจสอบความขัดแย้งของกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="b06a2-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="b06a2-133">การจองเกินนี้อาจเกิดขึ้นเมื่อคุณใช้ตัวช่วยในการรันการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="b06a2-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="b06a2-134">มีแนวโน้มมากที่สุดที่จะเกิดขึ้นถ้ามีงานจำนวนมากที่มีการรันไทม์ที่ค่อนข้างสั้น</span><span class="sxs-lookup"><span data-stu-id="b06a2-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b06a2-135">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b06a2-135">Issue resolution</span></span>

<span data-ttu-id="b06a2-136">ถ้าจำเป็นที่ไม่มีการจองเกินเกิดขึ้นสำหรับการจัดตารางการผลิตระดับการดำเนินงาน คุณสามารถทำให้ส่วนของการวางแผนหลักเป็นเธรดเดียวโดยการเปิดใช้ตัวเลือก **กำลังการผลิตมีจำกัดที่ถูกต้องสำหรับการจัดกำหนดการการดำเนินงาน** ในหน้า **พารามิเตอร์การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="b06a2-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="b06a2-137">ปุ่มนี้จะไม่พร้อมใช้งานตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b06a2-137">This option isn't available by default.</span></span> <span data-ttu-id="b06a2-138">คุณต้องเพิ่มด้วยตนเองให้กับหน้าโดยใช้ลักษณะการทำงานส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="b06a2-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="b06a2-139">เมื่อคุณใช้ตัวเลือกนี้ การจัดตารางการผลิตจะทำงานช้ามากขึ้นเนื่องจากการขาดการประมวลผลแบบขนาน</span><span class="sxs-lookup"><span data-stu-id="b06a2-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="b06a2-140">แผนการใบสั่งใช้เวลานานในการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b06a2-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b06a2-141">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="b06a2-141">Issue description</span></span>

<span data-ttu-id="b06a2-142">เมื่ออัพเดตปริมาณความต้องการและ/หรือวันที่จัดส่งในแผนการใบสั่ง โดยทั่วไปจะใช้เวลาอย่างน้อย 30 วินาทีสำหรับใบสั่งที่จะบันทึกการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b06a2-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b06a2-143">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b06a2-143">Issue resolution</span></span>

<span data-ttu-id="b06a2-144">นี่เป็นปัญหาที่ทราบด้วยกลไกจัดการการวางแผนหลักในตัว</span><span class="sxs-lookup"><span data-stu-id="b06a2-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="b06a2-145">เกิดขึ้นจากการกระจายโดยอัตโนมัติที่อยู่ภายใต้โครงสร้าง BOM ในระหว่างการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b06a2-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="b06a2-146">มีการแก้ไขปัญหานี้ในการเพิ่มประสิทธิภาพการวางแผน ซึ่งผู้วางแผนสามารถอัพเดตและอนุมัติใบสั่งที่เกี่ยวข้องและ เมื่อต้องการให้ ทริกเกอร์รันการวางแผนเพื่ออัพเดตแผนการใบสั่งสำหรับโครงสร้าง BOM ที่อยู่ภายใต้</span><span class="sxs-lookup"><span data-stu-id="b06a2-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="b06a2-147">วิธีการหนึ่งในการปรับปรุงประสิทธิภาพการทำงานด้วยกลไกจัดการการวางแผนหลักในตัวคือให้ทำสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b06a2-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="b06a2-148">ไปที่ **การวางแผนหลัก \> การตั้งค่า \> แผน \> แผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="b06a2-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="b06a2-149">เลือกแผน</span><span class="sxs-lookup"><span data-stu-id="b06a2-149">Select a plan.</span></span>
1. <span data-ttu-id="b06a2-150">ขยายแท็บด่วน **กรอบเวลาในหน่วยวัน**</span><span class="sxs-lookup"><span data-stu-id="b06a2-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="b06a2-151">ตั้งค่า **การกระจาย** เป็น *ใช่* และตั้งค่าฟิลด์ด้านล่างนี้เป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="b06a2-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="b06a2-152">การดำเนินการนี้จะจำกัดรอบระยะเวลาสำหรับการกระจายสำหรับแผนหลักนี้เป็นวันเดียว</span><span class="sxs-lookup"><span data-stu-id="b06a2-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>
