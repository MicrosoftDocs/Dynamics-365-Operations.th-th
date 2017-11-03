---
title: "การจัดโครงแบบของผลิตภัณฑ์ตามมิติ"
description: "การจัดโครงแบบของผลิตภัณฑ์ตามมิติแสดงโซลูชันแบบง่ายสำหรับการสร้างผลิตภัณฑ์ย่อยจำนวนมากจากผลิตภัณฑ์หลักเดียวและสูตรการผลิต"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7b46adf0bef79eafb1dd4b0809965abdd3b4410c
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="f1b0c-103">การจัดโครงแบบของผลิตภัณฑ์ตามมิติ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f1b0c-104">การจัดโครงแบบของผลิตภัณฑ์ตามมิติแสดงโซลูชันแบบง่ายสำหรับการสร้างผลิตภัณฑ์ย่อยจำนวนมากจากผลิตภัณฑ์หลักเดียวและสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="f1b0c-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="f1b0c-105">การจัดโครงแบบของผลิตภัณฑ์ตามมิติเป็นค่าใดค่าหนึ่งในสามเทคโนโลยีการจัดโครงแบบผลิตภัณฑ์ที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="f1b0c-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="f1b0c-106">เทคโนโลยีสองแบบมีตัวแปรที่กำหนดไว้ล่วงหน้าและการจัดโครงแบบตามข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="f1b0c-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="f1b0c-107">เทคโนโลยีทั้งสามแบบใช้ผลิตภัณฑ์หลักเป็นจุดเริ่มต้น และอนุญาตให้ผู้ใช้สามารถสร้างผลิตภัณฑ์ย่อยหลายสำหรับหนึ่งผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="f1b0c-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="f1b0c-108">แนวคิดหลัก</span><span class="sxs-lookup"><span data-stu-id="f1b0c-108">Key concepts</span></span>
<span data-ttu-id="f1b0c-109">การจัดโครงแบบของผลิตภัณฑ์ตามมิติตามแนวคิดหลักต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1b0c-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="f1b0c-110">ผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="f1b0c-110">Product masters</span></span>
-   <span data-ttu-id="f1b0c-111">มิติของผลิตภัณฑ์การจัดการโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-111">Configuration product dimension</span></span>
-   <span data-ttu-id="f1b0c-112">กลุ่มการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="f1b0c-112">Configuration groups</span></span>
-   <span data-ttu-id="f1b0c-113">สูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="f1b0c-114">กระบวนการผลิตที่ปรับเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="f1b0c-114">Configuration route</span></span>
-   <span data-ttu-id="f1b0c-115">กฎโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="f1b0c-116">ผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="f1b0c-116">Product masters</span></span>

<span data-ttu-id="f1b0c-117">ผลิตภัณฑ์หลักคือ จุดเริ่มต้นสำหรับกระบวนการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f1b0c-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="f1b0c-118">สำหรับการจัดโครงแบบของผลิตภัณฑ์ตามมิติ คุณจำเป็นต้อง มีเทคโนโลยีการตั้งค่าคอนฟิกเฉพาะนี้และกลุ่มมิติของผลิตภัณฑ์ที่มีมิติของผลิตภัณฑ์การจัดการโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="f1b0c-119">มิติของผลิตภัณฑ์การจัดการโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-119">Configuration product dimension</span></span>

<span data-ttu-id="f1b0c-120">มิติของผลิตภัณฑ์การจัดการโครงแบบ จะถูกระบุผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลัก กับเทคโนโลยีการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="f1b0c-121">ค่ามิติโครงแบบถูกป้อน โดยผู้ใช้ และควรช่วยในการระบุแต่ละผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="f1b0c-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="f1b0c-122">กลุ่มการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="f1b0c-122">Configuration groups</span></span>

<span data-ttu-id="f1b0c-123">กลุ่มมิติจะกำหนดอยู่ในเก็บส่วนกลาง และสามารถใช้สำหรับแบบจำลองการจัดโครงแบบของผลิตภัณฑ์ตามมิติทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f1b0c-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="f1b0c-124">กลุ่มมิติที่เกี่ยวข้องกับบรรทัด BOM แต่ละรายการ และระงับเข้าด้วยกันกับกลุ่มของบรรทัดที่เป็นแบบเฉพาะร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f1b0c-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="f1b0c-125">ซึ่งหมายความ ว่า คุณสามารถเลือกรายการเดียวเท่านั้นในกลุ่มสำหรับตัวแปรผลิตภัณฑ์ย่อยเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f1b0c-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="f1b0c-126">สูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="f1b0c-127">BOM แสดงส่วนประกอบตัวจัดโครงแบบของผลิตภัณฑ์ตามมิติ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="f1b0c-128">รวมถึงผลิตภัณฑ์อื่นทั้งหมดที่แตกต่างกันที่สามารถใช้ในผลิตภัณฑ์ย่อยใด ๆ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="f1b0c-129">แต่ละบรรทัดใน BOM สามารถอ้างอิงกลุ่มโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="f1b0c-130">ถ้าบรรทัดไม่ได้อ้างอิงกลุ่มโครงแบบ มันจะรวมอยู่ในผลิตภัณฑ์ย่อยทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f1b0c-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="f1b0c-131">กระบวนการผลิตที่ปรับเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="f1b0c-131">Configuration route</span></span>

<span data-ttu-id="f1b0c-132">เส้นทางการตั้งค่าคอนฟิกกำหนดลำดับของกลุ่มการตั้งค่าคอนฟิก ตามที่จะแสดงต่อผู้ใช้ในระหว่างกระบวนการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f1b0c-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="f1b0c-133">กฎโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-133">Configuration rules</span></span>

<span data-ttu-id="f1b0c-134">กฎโครงแบบแสดงกลไกการตรวจสอบว่า ผลิตภัณฑ์ที่รวมอยู่ในกลุ่มโครงแบบหนึ่งใน BOM บังคับใช้ทั้งการรวมและมีข้อยกเว้นของผลิตภัณฑ์ในกลุ่มโครงแบบที่แตกต่างกันใน BOM เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f1b0c-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="f1b0c-135">กระบวนการการสร้างแบบจำลองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f1b0c-135">Product modeling process</span></span>
<span data-ttu-id="f1b0c-136">ลำดับของการสร้างรุ่นผลิตภัณฑ์สำหรับผลิตภัณฑ์ตามมิติเริ่มต้น ด้วยการกำหนดกลุ่มโครงแบบที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f1b0c-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="f1b0c-137">มันเป็นสิ่งสำคัญเพื่อให้แน่ใจว่า มีการผลิตภัณฑ์ทั้งหมดที่จะถูกใช้ใน BOM ได้ถูกส่งออกไปยังบริษัทที่แบบจำลองผลิตภัณฑ์ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f1b0c-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="f1b0c-138">เมื่อส่วนประกอบเหล่านี้อยู่ในสถานที่ ผู้ใช้สามารถสร้าง BOM และกำหนดกลุ่มการตั้งค่าคอนฟิกให้กับบรรทัด BOM ที่เกี่ยวข้องทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f1b0c-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="f1b0c-139">เมื่อ BOM เสร็จสมบูรณ์แล้ว คุณสามารถกำหนดเส้นทางการตั้งค่าคอนฟิกสำหรับกลุ่มการตั้งค่าคอนฟิกการสั่งซื้อในลำดับที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="f1b0c-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="f1b0c-140">[![กระบวนการสร้างโมเดลผลิตภัณฑ์ตามมิติ](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) ถ้าผลิตภัณฑ์ที่แน่นอนจากกลุ่มการตั้งค่าคอนฟิกที่แตกต่างกันที่ต้องใช้ร่วมกันหรือต้องไม่ถูกใช้ร่วมกัน คุณสามารถสร้างกฎโครงแบบที่จะบังคับใช้ความสัมพันธ์ของผลิตภัณฑ์เหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="f1b0c-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="f1b0c-141">หลังจาก BOM ถูกเชื่อมโยงร่วมกับผลิตภัณฑ์หลักตามมิติโดยใช้เวอร์ชัน BOM และทั้งสองแบบได้รับการอนุมัติ และเรียกใช้งาน คุณสามารถสร้างการจัดโครงแบบผลิตภัณฑ์ และป้อนชื่อสำหรับแต่ละโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="f1b0c-142">คุณสามารถกำหนดโครงแบบก่อนธุรกรรมใด ๆ จะถูกสร้างขึ้น หรือสามารถทำเมื่อจำเป็นสำหรับการกำหนดค่าบางอย่างเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="f1b0c-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="f1b0c-143">แนะนำการใช้</span><span class="sxs-lookup"><span data-stu-id="f1b0c-143">Suggested use</span></span>

<span data-ttu-id="f1b0c-144">เทคโนโลยีการจัดโครงแบบตามมิติเหมาะสมที่จะใช้สำหรับผลิตภัณฑ์ที่ มีความผันแปรจำกัดและการรวมชุดของขนาดมิติผลิตภัณฑ์มาตรฐานมิติข สี ลักษณะ และตั้งค่าคอนฟิกที่ไม่เหมาะสมสำหรับการระบุตัวแปรผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="f1b0c-145">ตัวอย่างอาจเป็นจักรยาน กับความสูงเฟรม ขนาดวงล้อ ชนิดเบรค และเกียร์แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f1b0c-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="f1b0c-146">ขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="f1b0c-146">Next step</span></span> 

<span data-ttu-id="f1b0c-147">คู่มืองานแปดรายการดังต่อไปนี้จะแสดงรายการในใบสั่งที่คุณควรดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f1b0c-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="f1b0c-148">สร้างผลิตภัณฑ์หลักที่ใช้มิติ (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="f1b0c-149">นำผลิตภัณฑ์หลักที่ใช้มิติออกใช้ (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="f1b0c-150">ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="f1b0c-151">กำหนดกลุ่มการตั้งค่าคอนฟิก (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="f1b0c-152">สร้างสูตรการผลิตสำหรับผลิตภัณฑ์หลักตามมิติ (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="f1b0c-153">กำหนดเส้นทางการปรับเปลี่ยน (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="f1b0c-154">สร้างกฎโครงแบบ (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="f1b0c-155">สร้างการจัดโครงแบบตามมิติ (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="f1b0c-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)


