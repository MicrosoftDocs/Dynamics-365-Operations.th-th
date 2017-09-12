---
title: "การตรวจนับตามรอบของสถานที่บางส่วน"
description: "แผนการตรวจนับตามรอบเป็นคู่มือการดำเนินงานการนับตามจริง คุณสามารถร้องขอผลิตภัณฑ์เฉพาะอย่างและผลิตภัณฑ์ย่อยที่จะตรวจนับแทนสินค้าคงคลังคงเหลือในสถานที่เก็บทั้งหมด"
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2ee4de8eabc55271e272ca3026746787353f5fc3
ms.contentlocale: th-th
ms.lasthandoff: 07/18/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="8125a-105">การตรวจนับตามรอบของสถานที่บางส่วน</span><span class="sxs-lookup"><span data-stu-id="8125a-105">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8125a-106">แผนการตรวจนับตามรอบเป็นคู่มือการดำเนินงานการนับตามจริง</span><span class="sxs-lookup"><span data-stu-id="8125a-106">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="8125a-107">คุณสามารถร้องขอผลิตภัณฑ์เฉพาะอย่างและผลิตภัณฑ์ย่อยที่จะตรวจนับแทนสินค้าคงคลังคงเหลือในสถานที่เก็บทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8125a-107">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="8125a-108">โดยใช้แผนการตรวจนับเพื่อสร้างงานการตรวจนับ คุณสามารถนำทางไปยังการดำเนินงานการตรวจนับตามจริง</span><span class="sxs-lookup"><span data-stu-id="8125a-108">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="8125a-109">คุณสามารถร้องขอผลิตภัณฑ์เฉพาะอย่างและผลิตภัณฑ์ย่อยที่จะตรวจนับแทนสินค้าคงคลังคงเหลือในสถานที่เก็บทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8125a-109">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="8125a-110">โดยการกรองผลิตภัณฑ์ฉพาะ ผู้จัดการคลังสินค้าสามารถลดโสหุ้ยในการตรวจทาน หลีกเลี่ยงข้อผิดพลาดในการรวมบัญชี และประหยัดเวลา</span><span class="sxs-lookup"><span data-stu-id="8125a-110">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="8125a-111">วิธีการตั้งค่าคอนฟิกการตรวจนับตามรอบของสถานที่เก็บบางส่วน</span><span class="sxs-lookup"><span data-stu-id="8125a-111">How to configure partial location cycle counting</span></span>
<span data-ttu-id="8125a-112">เมื่อคุณใช้กระบวนการงานคลังสินค้าสำหรับการดำเนินงานการตรวจนับ จะมีการสร้างหัวข้องานขึ้นสำหรับที่ตั้งแต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="8125a-112">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="8125a-113">เมื่อคุณกำหนดแผนการตรวจนับตามรอบ คุณสามารถใช้การสอบถาม **เลือกสถานที่เก็บ** เพื่อจำกัดงานการตรวจนับตามรอบที่ถูกสร้างขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="8125a-113">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="8125a-114">เมื่อคุณเลือกผลิตภัณฑ์สำหรับแผนการตรวจนับตามรอบ คุณสามารถเลือกการสอบถามผลิตภัณฑ์และผลิตภัณฑ์ย่อย เพื่อกำหนดสิ่งที่จะตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="8125a-114">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="8125a-115">คุณสามารถเชื่อมโยง **เท็มเพลตงาน** กับแผนการตรวจนับตามรอบเพื่อกำหนดว่าควรสร้างงานการตรวจสอบตามรอบได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="8125a-115">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="8125a-116">เท็มเพลตงานสำหรับการดำเนินงานการตรวจนับมีการอ้างอิงจากแผนการตรวจนับตามรอบโดยตรง</span><span class="sxs-lookup"><span data-stu-id="8125a-116">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="8125a-117">เมื่อคุณกำหนดรายละเอียดเท็มเพลตของงาน คุณสามารถใช้ตัวเลือก **การจำแนกรายการงาน** เพื่อระบุว่า รายการงานการตรวจนับจะต้องจัดกลุ่มตามหมายเลขสินค้าหรือหมายเลขตัวแปรของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8125a-117">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="8125a-118">จะต้องตั้งค่านี้ ถ้าคุณต้องการนับสินค้าคงคลังคงเหลือสำหรับผลิตภัณฑ์เฉพาะในสถานที่เก็บแห่งหนึ่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8125a-118">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="8125a-119">รายการงานการตรวจนับตามรอบที่สร้างขึ้นจะมีระดับของข้อมูลที่คุณกำหนดไว้ที่นี่ และการดำเนินการตรวจนับที่แนะนำจะถูกจัดการตามระดับนี้</span><span class="sxs-lookup"><span data-stu-id="8125a-119">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="8125a-120">ถ้าคุณเชื่อมโยงแผนการตรวจนับตามรอบกับแทมเพลตของงานโดยใช้ตัวเลือก **การจำแนกรายการงาน** ฟิลด์ของ **การตรวจนับตามรอบบางส่วน** จะถูกเลือก สำหรับงานการตรวจนับตามรอบที่ถูกสร้างขึ้น และรายการงานการตรวจนับตามรอบหลายรายการจะถูกสร้างขึ้นตามข้อกำหนดของเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="8125a-120">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="8125a-121">ก่อนที่จะประมวลผลงานการตรวจนับตามรอบบางส่วน คุณต้องเลือก **แสดงหมายเลขสินค้า** เป็นอย่างน้อย สำหรับรายการเมนูบนอุปกรณ์เคลื่อนที่เป็นส่วนหนึ่งของการตั้งค่าการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="8125a-121">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="8125a-122">จะมีการถามผู้ปฏิบัติงานคลังสินค้าเพื่อบันทึกข้อมูลการตรวจนับที่เกี่ยวข้องกับรายการการตรวจนับ (หมายเลขสินค้าและมิติของผลิตภัณฑ์) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8125a-122">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="8125a-123">ปริมาณคงคลังคงเหลือทั้งหมดจะถูกละเว้นสำหรับกระบวนการตรวจนับนี้</span><span class="sxs-lookup"><span data-stu-id="8125a-123">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="8125a-124">สำหรับกระบวนการตรวจนับตามรอบบางส่วน จะไม่มีการอัพเดตวันที่/เวลาของ **การตรวจนับตามรอบล่าสุด** สำหรับสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="8125a-124">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="8125a-125">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8125a-125">Example</span></span>
<span data-ttu-id="8125a-126">สำหรับตัวอย่างนี้ จะต้องมีการตรวจนับเฉพาะหมายเลขสินค้า A0001 ในคลังสินค้า 61</span><span class="sxs-lookup"><span data-stu-id="8125a-126">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="8125a-127">มีการสร้างเท็มเพลตงานใหม่สำหรับวการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="8125a-127">A new work template for cycle counting is created.</span></span> <span data-ttu-id="8125a-128">ตัวเลือก **การจำแนกรายการงาน** จะใช้เพื่อจัดกลุ่มรายการงานที่ตรวจนับตามหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="8125a-128">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="8125a-129">ดังนั้น งานการตรวจนับตามรอบที่สร้างขึ้นจะมีรายการสำหรับแต่ละหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="8125a-129">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="8125a-130">นอกจากนี้ คุณยังสามารถจัดกลุ่มรายการตามหมายเลขตัวแปรของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8125a-130">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="8125a-131">มีการสร้างแผนการตรวจนับตามรอบใหม่ที่อ้างอิงเท็มเพลตงานที่เพิ่งสร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="8125a-131">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="8125a-132">แผนการตรวจนับตามรอบรวมถึงสถานทั้งหมดในคลังสินค้า 61 (แบบสอบถาม **เลือกสถานที่เก็บ** ) ที่เก็บสินค้าคงคลังสำหรับหมายเลขสินค้า A0001</span><span class="sxs-lookup"><span data-stu-id="8125a-132">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="8125a-133">มีการกำหนดการเลือกผลิตภัณฑ์เฉพาะไว้ในส่วนของ **การเลือกผลิตภัณฑ์ที่ตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="8125a-133">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="8125a-134">คุณสามารถเลือกผลิตภัณฑ์สำหรับแผนการตรวจนับตามรอบ ด้วยการตั้งค่าฟิลด์ **สถานที่ว่างเปล่า** ไปเป็น **ไม่รวมส่วนที่ว่าง** เมื่อประมวลผลแผนการตรวจนับตามรอบ จะมีสร้างงานการตรวจนับตามรอบบางส่วนสำหรับหมายเลขสินค้า A0001</span><span class="sxs-lookup"><span data-stu-id="8125a-134">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="8125a-135">สามารถดำเนินการกระบวนการตรวจนับตามจริงโดยการใช้รายการเมนูบนอุปกรณ์เคลื่อนสำหรับการตรวจนับตามรอบที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="8125a-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="8125a-136">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="8125a-136">See also</span></span>
--------

[<span data-ttu-id="8125a-137">การตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="8125a-137">Cycle counting</span></span>](cycle-counting.md)


