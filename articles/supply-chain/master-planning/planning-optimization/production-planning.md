---
title: การวางแผนการผลิต
description: หัวข้อนี้อธิบายการวางแผนการผลิตและอธิบายวิธีการแก้ไขแผนการใบสั่งผลิตโดยใช้การเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 22b78f44940f71097ca8b1cdb74edb06274bba75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839234"
---
# <a name="production-planning"></a><span data-ttu-id="7e9d1-103">การวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="7e9d1-103">Production planning</span></span>

<span data-ttu-id="7e9d1-104">การเพิ่มประสิทธิภาพการวางแผนสนับสนุนสถานการณ์การผลิตต่างๆ</span><span class="sxs-lookup"><span data-stu-id="7e9d1-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="7e9d1-105">ถ้าคุณย้ายมาจากกลไกจัดการการวางแผนหลักในตัวที่มีอยู่ คุณควรทราบถึงลักษณะการทำงานที่เปลี่ยนแปลงบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="7e9d1-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<span data-ttu-id="7e9d1-106">ภาพต่อไปนี้แสดงบทนําย่อเกี่ยวกับแนวคิดบางแนวคิดที่อธิบายไว้ในหัวข้อนี้: [การปรับปรุงประสิทธิภาพการวางแผน Dynamics 365 Supply Chain Management](https://youtu.be/u1pcmZuZBTw)</span><span class="sxs-lookup"><span data-stu-id="7e9d1-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="7e9d1-107">เปิดใช้งานคุณลักษณะนี้สำหรับระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="7e9d1-107">Turn on this feature for your system</span></span>

<span data-ttu-id="7e9d1-108">ถ้าระบบของคุณยังไม่ได้รวมคุณลักษณะที่อธิบายไว้ในหัวข้อนี้ ให้ไปที่ [การจัดการคุณลักษณะ](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดคุณลักษณะ *แผนการใบสั่งผลิตสำหรับการเพิ่มประสิทธิภาพการวางแผน*</span><span class="sxs-lookup"><span data-stu-id="7e9d1-108">If your system doesn't already include the features described in this topic, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Planned production orders for Planning Optimization* feature.</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="7e9d1-109">แผนการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="7e9d1-109">Planned production orders</span></span>

<span data-ttu-id="7e9d1-110">เมื่อการวางแผนหลักสร้างแผนการใบสั่งเพื่อตอบสนองความต้องการ ชนิดใบสั่งจะขึ้นอยู่กับค่าของฟิลด์ **ชนิดแผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="7e9d1-110">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="7e9d1-111">ถ้าฟิลด์ **ชนิดแผนการใบสั่ง** ได้รับการตั้งค่าเป็น *การผลิต* แผนการใบสั่งผลิตจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7e9d1-111">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="7e9d1-112">แผนการใบสั่งผลิตเหล่านี้รวมข้อมูลเกี่ยวกับรายการวัสดุและส่วนประกอบ (BOM) ที่ใช้งานอยู่และรหัสกระบวนการผลิตจากการตั้งค่าการผลิตที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="7e9d1-112">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="7e9d1-113">ความต้องการจาก BOM</span><span class="sxs-lookup"><span data-stu-id="7e9d1-113">Requirements from BOMs</span></span>

<span data-ttu-id="7e9d1-114">มีการให้ข้อมูล BOM ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="7e9d1-114">BOM information is honored during master planning.</span></span> <span data-ttu-id="7e9d1-115">ผลลัพธ์ของแผนประกอบด้วยการจัดหาวัสดุเพื่อครอบคลุมความต้องการวัสดุที่เกี่ยวข้องกันในการผลิต</span><span class="sxs-lookup"><span data-stu-id="7e9d1-115">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="7e9d1-116">ในระหว่างการวางแผนหลัก BOM ที่ใช้งานอยู่ในปัจจุบันจะถูกใช้ในการระบุวัสดุที่ต้องใช้ในการผลิต</span><span class="sxs-lookup"><span data-stu-id="7e9d1-116">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="7e9d1-117">ขั้นตอนนี้จะผ่านระดับโครงสร้าง BOM ทั้งหมดที่เกี่ยวข้องกับใบสั่งผลิตที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-117">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="7e9d1-118">เติมความต้องการวัสดุโดยใช้ปริมาณคงคลังคงเหลือที่มีอยู่ ปริมาณคงคลังคงเหลือที่มีอยู่ และแผนการใบสั่งที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="7e9d1-118">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="7e9d1-119">ถ้าต้องใช้วัสดุเพิ่มเติมที่ใดก็ตาม แผนการใบสั่งจะถูกสร้างขึ้นเพื่อครอบคลุมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="7e9d1-119">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="7e9d1-120">การจัดตารางการผลิตในระหว่างการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="7e9d1-120">Scheduling during firming</span></span>

<span data-ttu-id="7e9d1-121">แผนการใบสั่งผลิตรวมรหัสกระบวนการผลิตที่ต้องใช้ในการจัดตารางการผลิต</span><span class="sxs-lookup"><span data-stu-id="7e9d1-121">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="7e9d1-122">อย่างไรก็ตาม การสนับสนุนการจัดตารางการผลิตระหว่างการวางแผนการรันของแผนการใบสั่งยังคงค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="7e9d1-122">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="7e9d1-123">รหัสกระบวนการผลิตใช้ในการจัดตารางการผลิตแผนการใบสั่งผลิตในระหว่างการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="7e9d1-123">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="7e9d1-124">ดังนั้น ระยะเวลารอคอยสินค้าในแผนการใบสั่งผลิต จึงอาจแตกต่างจากระยะเวลารอคอยสินค้าในใบสั่งผลิตที่จัดตารางการผลิตที่เกี่ยวข้องที่ยืนยันไว้ซึ่งสร้างขึ้นจากใบสั่งผลิต ตามที่อธิบายไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="7e9d1-124">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="7e9d1-125">**แผนการใบสั่งผลิต** – ระยะเวลารอคอยสินค้าขึ้นอยู่กับระยะเวลารอคอยสินค้าที่คงที่จากผลิตภัณฑ์ที่ปล่อยงานออกใช้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-125">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="7e9d1-126">**ใบสั่งผลิตที่ยืนยัน** – ระยะเวลารอคอยสินค้าขึ้นอยู่กับการจัดตารางการผลิตที่ใช้ข้อมูลกระบวนการผลิตและข้อจากข้อจากทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="7e9d1-126">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="7e9d1-127">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความพร้อมใช้งานของคุณลักษณะที่คาดไว้ ให้ดูที่ [การวิเคราะห์ความเหมาะสมของการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="7e9d1-127">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="7e9d1-128">หากคุณขึ้นอยู่กับฟังก์ชันการผลิตที่ยังไม่มีอยู่ในการเพิ่มประสิทธิภาพการวางแผน คุณสามารถใช้กลไกจัดการการวางแผนหลักในตัวต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-128">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="7e9d1-129">ไม่มีข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="7e9d1-129">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="7e9d1-130">ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="7e9d1-130">Delays</span></span>

<span data-ttu-id="7e9d1-131">ถ้าระยะเวลารอคอยสินค้าของวัสดุที่ต้องการยาวกว่ารอบระยะเวลาระหว่างวันที่วันนี้และวันที่ความต้องการวัสดุ แผนการใบสั่งของวัสดุที่ต้องใช้และใบสั่งผลิตที่เกี่ยวข้องจะล่าช้า</span><span class="sxs-lookup"><span data-stu-id="7e9d1-131">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="7e9d1-132">ในแผนการใบสั่ง ความล่าช้า (ในหนึ่งวัน) จะคํานวณโดยใช้ระยะเวลารอคอยสินค้าจากผลิตภัณฑ์ที่ปล่อยออกใช้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-132">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="7e9d1-133">จากนั้นข้อมูลความล่าช้าจะถูกเผยแพร่ผ่านระดับทั้งหมดของโครงสร้าง BOM</span><span class="sxs-lookup"><span data-stu-id="7e9d1-133">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="7e9d1-134">ดังนั้นคุณจึงสามารถติดตามผลกระทบของวัตถุดิบที่ล่าช้าตลอดทางไปยังใบสั่งขายของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7e9d1-134">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="7e9d1-135">แก้ไขแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7e9d1-135">Modifying planned orders</span></span>

<span data-ttu-id="7e9d1-136">เมื่อคุณเปลี่ยนแปลงข้อมูลในแผนการใบสั่ง คุณจะได้รับข้อความต่อไปนี้ :"โปรดทราบว่าผลกระทบของการเปลี่ยนแปลงด้วยตนเองบนแผนการใบสั่งจะไม่สะท้อนให้เห็นในส่วนที่เหลือของแผนจนกว่าการรันการวางแผนหลักถัดไป"</span><span class="sxs-lookup"><span data-stu-id="7e9d1-136">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="7e9d1-137">ถ้าคุณต้องการเปลี่ยนแปลงข้อมูลเกี่ยวกับแผนการใบสั่ง และดูผลกระทบของความต้องการวัสดุที่เกี่ยวข้อง ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-137">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="7e9d1-138">อัปเดตแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7e9d1-138">Update the planned order.</span></span>
2. <span data-ttu-id="7e9d1-139">อนุมัติแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7e9d1-139">Approve the planned order.</span></span>
3. <span data-ttu-id="7e9d1-140">ดำเนินการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="7e9d1-140">Run master planning.</span></span>

<span data-ttu-id="7e9d1-141">เมื่อคุณรันการวางแผนหลัก คุณไม่ควรใช้ตัวกรองข้อมูลถ้ารวมแผนการใบสั่งผลิตไว้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-141">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="7e9d1-142">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ส่วน [ตัวกรอง](#filters) ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-142">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="7e9d1-143">ถ้าวันที่จัดส่งของแผนการใบสั่งเปลี่ยนเป็นวันที่ในภายหลัง ความต้องการอาจถูกโยงกับแผนการใบสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="7e9d1-143">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="7e9d1-144">ลักษณะการทำงานนี้จะเกิดขึ้นเมื่อวันที่จัดหาวัสดุใหม่จะส่งผลให้เกิดความล่าช้าในความต้องการที่มีการเชื่อมโยงความต้องการกับการจัดหาวัสดุ แต่เพื่อหลีกเลี่ยงความล่าช้าดังกล่าวตามการตั้งค่าระยะเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="7e9d1-144">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="7e9d1-145">หน้าการกระจาย</span><span class="sxs-lookup"><span data-stu-id="7e9d1-145">Explosion page</span></span>

<span data-ttu-id="7e9d1-146">คุณสามารถใช้หน้า **การกระจาย** เพื่อวิเคราะห์ความต้องการที่ต้องใช้ในใบสั่งผลิตหนึ่ง ๆ หรือแผนการใบสั่งผลิต ความครอบคลุมที่เกี่ยวข้อง และข้อมูลการเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7e9d1-146">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="7e9d1-147">รายละเอียดบนหน้า **การกระจาย** จะถูกอัปเดตในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="7e9d1-147">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="7e9d1-148">คุณไม่สามารถอัปเดตข้อมูลโดยตรงจากหน้า **การกระจาย** ได้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-148">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="7e9d1-149">ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e9d1-149">Filters</span></span>

<span data-ttu-id="7e9d1-150">สำหรับสถานการณ์การวางแผนที่มีการผลิตรวมอยู่ด้วย เราขอแนะนำว่าคุณควรหลีกเลี่ยงการรันการวางแผนหลักที่มีการกรองข้อมูลแล้ว</span><span class="sxs-lookup"><span data-stu-id="7e9d1-150">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="7e9d1-151">เพื่อให้แน่ใจว่าการเพิ่มประสิทธิภาพการวางแผนจะมีข้อมูลที่ต้องใช้ในการคํานวณผลลัพธ์ที่ถูกต้อง คุณต้องรวมผลิตภัณฑ์ทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์ในโครงสร้าง BOM ทั้งหมดของแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7e9d1-151">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="7e9d1-152">แม้ว่ารายการรองที่ขึ้นต่อกันจะตรวจพบและรวมอยู่ในการวางแผนหลักโดยอัตโนมัติเมื่อใช้กลไกจัดการการวางแผนหลักในตัว แต่การเพิ่มประสิทธิภาพการวางแผนจะไม่ดำเนินการนี้</span><span class="sxs-lookup"><span data-stu-id="7e9d1-152">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="7e9d1-153">ตัวอย่างเช่น ถ้าสลักเกลียวเดียวจากโครงสร้าง BOM ของผลิตภัณฑ์ A ยังใช้ในการผลิตผลิตภัณฑ์ B ผลิตภัณฑ์ทั้งหมดในโครงสร้าง BOM ของผลิตภัณฑ์ A และ B ต้องรวมอยู่ในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="7e9d1-153">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="7e9d1-154">เนื่องจากอาจซับซ้อนมากเพื่อให้แน่ใจว่าผลิตภัณฑ์ทั้งหมดเป็นส่วนหนึ่งของตัวกรองข้อมูล เราจึงขอแนะนาว่าคุณควรหลีกเลี่ยงการรันการวางแผนหลักที่กรองข้อมูลแล้วเมื่อเกี่ยวข้องกับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="7e9d1-154">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]