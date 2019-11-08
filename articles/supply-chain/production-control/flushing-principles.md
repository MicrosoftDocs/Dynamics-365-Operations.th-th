---
title: หลักการตัดจ่าย
description: หัวข้อนี้อธิบายหลักการตัดจ่ายสี่รายการที่ใช้สำหรับการใช้วัตถุดิบ
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 84cada71937604c013dbaaa47435015e63203595
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552221"
---
# <a name="flushing-principles"></a><span data-ttu-id="07a83-103">หลักการตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="07a83-103">Flushing principles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07a83-104">หลักการตัดจ่ายสะท้อนถึงกลยุทธ์การใช้ที่แตกต่างกันสำหรับวัตถุดิบที่ใช้ในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="07a83-104">The flushing principles reflect different consumption strategies for raw materials that are used in production processes.</span></span> <span data-ttu-id="07a83-105">ปริมาณการใช้คือกระบวนการที่ลดวัสดุจากสินค้าคงคลังคงเหลือและตั้งค่าของวัสดุที่ใช้เป็น **งานระหว่างทำ** (WIP) สำหรับใบสั่งผลิตและใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="07a83-105">Consumption is the process that deducts material from the on-hand inventory and sets the value of the consumed materials to **Work in progress** (WIP) for production orders and batch orders.</span></span> <span data-ttu-id="07a83-106">โดยปกติแล้ววัตถุดิบจะถูกใช้จากสถานที่เก็บที่ตั้งค่าคอนฟิกสำหรับกระบวนการที่ใช้วัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="07a83-106">Raw materials are usually consumed from a location that is configured for the process that consumes the material.</span></span> <span data-ttu-id="07a83-107">ที่ตั้งนี้เรียกว่าที่ตั้งอินพุทการผลิต</span><span class="sxs-lookup"><span data-stu-id="07a83-107">This location is known as the production input location.</span></span>

<span data-ttu-id="07a83-108">ก่อนปริมาณการใช้วัสดุ วัสดุจะถูกย้ายไปยังที่ตั้งอินพุท</span><span class="sxs-lookup"><span data-stu-id="07a83-108">Before material consumption, the materials are moved to the input location.</span></span> <span data-ttu-id="07a83-109">ภาพประกอบต่อไปนี้แสดงกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="07a83-109">The following illustration shows the process.</span></span>

<span data-ttu-id="07a83-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span><span class="sxs-lookup"><span data-stu-id="07a83-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span></span>

1. <span data-ttu-id="07a83-111">คลังสินค้าวัสดุ</span><span class="sxs-lookup"><span data-stu-id="07a83-111">Material warehouse</span></span>
2. <span data-ttu-id="07a83-112">การเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="07a83-112">Raw material picking</span></span>
3. <span data-ttu-id="07a83-113">ที่ตั้งอินพุทการผลิต</span><span class="sxs-lookup"><span data-stu-id="07a83-113">Production input location</span></span>
4. <span data-ttu-id="07a83-114">ปริมาณการใช้วัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="07a83-114">Raw material consumption</span></span>
5. <span data-ttu-id="07a83-115">กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="07a83-115">Production process</span></span>

<span data-ttu-id="07a83-116">ปริมาณการใช้วัสดุถูกควบคุมโดยหลักการตัดจ่ายสี่รายการดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="07a83-116">Material consumption is controlled by the following four flushing principles:</span></span>

- <span data-ttu-id="07a83-117">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="07a83-117">Manual</span></span>
- <span data-ttu-id="07a83-118">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="07a83-118">Start</span></span>
- <span data-ttu-id="07a83-119">เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="07a83-119">Finish</span></span>
- <span data-ttu-id="07a83-120">มีอยู่ที่สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="07a83-120">Available at location</span></span>

<span data-ttu-id="07a83-121">หลักการตัดจ่ายถูกตั้งค่าคอนฟิกในลำดับชั้นของค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="07a83-121">The flushing principles are configured in a hierarchy of default values.</span></span> <span data-ttu-id="07a83-122">ลำดับชั้นเริ่มต้นที่ผลิตภัณฑ์ที่นำออกใช้ ซึ่งหลักการตัดจ่ายมีค่าเป็น **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="07a83-122">The hierarchy starts at the released product, where the flushing principle has the value **Start**.</span></span> <span data-ttu-id="07a83-123">ในสูตรการผลิต (BOM) หรือรายการสูตร สามารถแทนที่หลักการตัดจ่ายจากผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="07a83-123">On the bill of materials (BOM) or formula line, the flushing principle from the product can be overridden.</span></span> <span data-ttu-id="07a83-124">หลักการตัดจ่ายเริ่มต้นในรายการ BOM สำหรับการผลิตหรือรายการสูตรใบสั่งชุดงานได้มาจากผลิตภัณฑ์หรือค่าที่แทนที่ใน BOM หรือสูตร</span><span class="sxs-lookup"><span data-stu-id="07a83-124">The default flushing principle on the production BOM lines or batch order formula lines is taken from the product or the overridden value on the BOM or formulas.</span></span>

## <a name="description-of-the-flushing-principles"></a><span data-ttu-id="07a83-125">คำอธิบายหลักการตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="07a83-125">Description of the flushing principles</span></span>

### <a name="manual"></a><span data-ttu-id="07a83-126">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="07a83-126">Manual</span></span>
<span data-ttu-id="07a83-127">หลักการตัดจ่ายด้วยตนเองบ่งชี้ว่าการลงทะเบียนปริมาณการใช้วัสดุเป็นการดำเนินงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="07a83-127">The Manual flushing principle indicates that the registration of material consumption is a manual operation.</span></span> <span data-ttu-id="07a83-128">หลักการนี้จะเกี่ยวข้องถ้า ตัวอย่างเช่น คุณต้องการให้สามารถติดตามเวลา และปริมาณของหมายเลขชุดงานที่ใช้ไปหรือ หมายเลขลำดับประจำสินค้าจะต้องถูกนำมาพิจารณา สำหรับวัตถุประสงค์ในการติดตาม</span><span class="sxs-lookup"><span data-stu-id="07a83-128">This principle is relevant if, for example, you want to be able to track time, and the quantity of consumed batch numbers or serial numbers must be accounted for, for tracking purposes.</span></span> <span data-ttu-id="07a83-129">มีการลงทะเบียนปริมาณการใช้ด้วยตนเองในสมุดรายวันรายการเบิกสินค้าสำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="07a83-129">Manual consumption is registered in a production picking list journal.</span></span> <span data-ttu-id="07a83-130">สำหรับสินค้าที่เปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง สามารถใช้ขั้นตอนแฮนด์เฮลด์ได้</span><span class="sxs-lookup"><span data-stu-id="07a83-130">For items that are enabled for advanced warehouse processes, a hand-held flow can be applied.</span></span>

### <a name="start"></a><span data-ttu-id="07a83-131">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="07a83-131">Start</span></span>
<span data-ttu-id="07a83-132">หลักการตัดจ่ายเริ่มต้นบ่งชี้ว่าวัสดุจะถูกใช้โดยอัตโนมัติเมื่อเริ่มต้นใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="07a83-132">The Start flushing principle indicates that material will be automatically consumed when the production order is started.</span></span> <span data-ttu-id="07a83-133">ปริมาณวัสดุที่จะถูกใช้เป็นสัดส่วนกับปริมาณที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="07a83-133">The amount of material that is consumed is proportional to the quantity that is started.</span></span> <span data-ttu-id="07a83-134">เมื่อมีการใช้หลักการตัดจ่ายเริ่มต้นพร้อมกับระบบการดำเนินการผลิต จะสามารถใช้เพื่อตัดจ่ายวัสดุเมื่อมีการเริ่มต้นการดำเนินงานหรืองานกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="07a83-134">When the Start flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is started.</span></span> <span data-ttu-id="07a83-135">หลักการนี้จะเกี่ยวข้องถ้า ตัวอย่างเช่น ผลต่างในปริมาณการใช้อยู่ในระดับต่ำ วัสดุเป็นวัสดุที่มีมูลค่าต่ำ ไม่จำเป็นต้องมีการติดตามอีกต่อไป หรือมีเวลาที่ใช้ในการผลิตในการดำเนินงานที่สั้น</span><span class="sxs-lookup"><span data-stu-id="07a83-135">This principle is relevant if, for example, the variance in the consumption is low, the materials are low-value materials, there are no tracking requirements, or there is a short run time on operations.</span></span> 

### <a name="finish"></a><span data-ttu-id="07a83-136">เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="07a83-136">Finish</span></span>
<span data-ttu-id="07a83-137">หลักการตัดจ่าย เสร็จสิ้น บ่งชี้ว่าวัสดุจะถูกใช้โดยอัตโนมัติเมื่อใบสั่งผลิตถูกรายงานเป็นเสร็จสิ้น หรือเมื่อมีการลงทะเบียนการดำเนินงานที่ตั้งค่าให้ใช้วัสดุเป็นเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="07a83-137">The Finish flushing principle indicates that material will be automatically consumed when the production order is reported as finished, or when an operation that is set up to consume the materials is registered as completed.</span></span> <span data-ttu-id="07a83-138">ปริมาณวัสดุที่จะถูกใช้เป็นสัดส่วนกับปริมาณที่ถูกรายงานเป็นเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="07a83-138">The amount of material that is consumed is proportional to the quantity that is reported as finished.</span></span> <span data-ttu-id="07a83-139">เมื่อมีการใช้หลักการตัดจ่ายเสร็จสิ้นพร้อมกับระบบการดำเนินการผลิต จะสามารถใช้เพื่อตัดจ่ายวัสดุเมื่อการดำเนินงานหรืองานกระบวนการเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="07a83-139">When the Finish flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is completed.</span></span> <span data-ttu-id="07a83-140">หลักการนี้จะเกี่ยวข้องในสถานการณ์เดียวกันกับหลักเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="07a83-140">This principle is relevant in the same situations as the Start principle.</span></span> <span data-ttu-id="07a83-141">อย่างไรก็ตาม หลักเสร็จสิ้นมีไว้สำหรับการดำเนินงานที่มีเวลาที่ใช้ในการผลิตที่นานขึ้น โดยที่วัสดุไม่ควรถูกตั้งค่าเป็น WIP ก่อนที่การดำเนินงานจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="07a83-141">However, the Finish principle is for operations that have a longer run time, where materials should not be set to WIP before the operation is completed.</span></span> 

### <a name="available-at-location"></a><span data-ttu-id="07a83-142">มีอยู่ที่สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="07a83-142">Available at location</span></span>
<span data-ttu-id="07a83-143">หลักการตัดจ่ายแบบมีอยู่ในสถานที่ตั้งบ่งชี้ว่าวัสดุจะถูกใช้โดยอัตโนมัติเมื่อมีการลงทะเบียนเป็นเบิกสินค้าสำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="07a83-143">The Available at location flushing principle indicates that the material will be automatically consumed when it's registered as picked for production.</span></span> <span data-ttu-id="07a83-144">วัสดุจะถูกลงทะเบียนเป็นเบิกสินค้าจากสถานที่เมื่องานสำหรับการเบิกวัตถุดิบเสร็จสมบูรณ์ หรือเมื่อวัตถุดิบพร้อมใช้งานในสถานที่ตั้งอินพุทการผลิต และรายการวัสดุถูกเผยแพร่ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="07a83-144">The material is registered as picked from location when work for the raw material picking is completed, or when material is available on the production input location and the material line is released to the warehouse.</span></span> <span data-ttu-id="07a83-145">รายการเบิกสินค้าที่สร้างขึ้นในระหว่างกระบวนการถูกลงรายการบัญชีในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="07a83-145">The picking list that is generated during the process is posted in a batch job.</span></span> <span data-ttu-id="07a83-146">หลักการนี้จะเกี่ยวข้องถ้า ตัวอย่างเช่น คุณมีการเบิกสินค้าหลายกิจกรรมสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="07a83-146">This principle is relevant if, for example, you have many picking activities against one production order.</span></span> <span data-ttu-id="07a83-147">ในกรณีนี้ คุณไม่จำเป็นต้องอัพเดตรายการเบิกสินค้าด้วยตนเอง และคุณสามารถเรียกดูมุมมองปัจจุบันของยอดดุล WIP ได้</span><span class="sxs-lookup"><span data-stu-id="07a83-147">In this case, you don't have to update the picking list manually, and you can get a current view of the WIP balance.</span></span>
