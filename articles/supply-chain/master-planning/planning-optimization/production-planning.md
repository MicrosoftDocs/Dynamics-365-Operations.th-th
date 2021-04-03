---
title: การวางแผนการผลิต
description: หัวข้อนี้อธิบายการวางแผนการผลิตและอธิบายวิธีการแก้ไขแผนการใบสั่งผลิตโดยใช้การเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: f9b5e4122fbd83ff76e0605b2f0816e10d2d9aab
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470844"
---
# <a name="production-planning"></a><span data-ttu-id="cc405-103">การวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="cc405-103">Production planning</span></span>

<span data-ttu-id="cc405-104">การเพิ่มประสิทธิภาพการวางแผนสนับสนุนสถานการณ์การผลิตต่างๆ</span><span class="sxs-lookup"><span data-stu-id="cc405-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="cc405-105">ถ้าคุณย้ายมาจากกลไกจัดการการวางแผนหลักในตัวที่มีอยู่ คุณควรทราบถึงลักษณะการทำงานที่เปลี่ยนแปลงบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="cc405-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<span data-ttu-id="cc405-106">ภาพต่อไปนี้แสดงบทนําย่อเกี่ยวกับแนวคิดบางแนวคิดที่อธิบายไว้ในหัวข้อนี้: [การปรับปรุงประสิทธิภาพการวางแผน Dynamics 365 Supply Chain Management](https://youtu.be/u1pcmZuZBTw)</span><span class="sxs-lookup"><span data-stu-id="cc405-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="cc405-107">แผนการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="cc405-107">Planned production orders</span></span>

<span data-ttu-id="cc405-108">เมื่อการวางแผนหลักสร้างแผนการใบสั่งเพื่อตอบสนองความต้องการ ชนิดใบสั่งจะขึ้นอยู่กับค่าของฟิลด์ **ชนิดแผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="cc405-108">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="cc405-109">ถ้าฟิลด์ **ชนิดแผนการใบสั่ง** ได้รับการตั้งค่าเป็น *การผลิต* แผนการใบสั่งผลิตจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="cc405-109">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="cc405-110">แผนการใบสั่งผลิตเหล่านี้รวมข้อมูลเกี่ยวกับรายการวัสดุและส่วนประกอบ (BOM) ที่ใช้งานอยู่และรหัสกระบวนการผลิตจากการตั้งค่าการผลิตที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cc405-110">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="cc405-111">ความต้องการจาก BOM</span><span class="sxs-lookup"><span data-stu-id="cc405-111">Requirements from BOMs</span></span>

<span data-ttu-id="cc405-112">มีการให้ข้อมูล BOM ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="cc405-112">BOM information is honored during master planning.</span></span> <span data-ttu-id="cc405-113">ผลลัพธ์ของแผนประกอบด้วยการจัดหาวัสดุเพื่อครอบคลุมความต้องการวัสดุที่เกี่ยวข้องกันในการผลิต</span><span class="sxs-lookup"><span data-stu-id="cc405-113">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="cc405-114">ในระหว่างการวางแผนหลัก BOM ที่ใช้งานอยู่ในปัจจุบันจะถูกใช้ในการระบุวัสดุที่ต้องใช้ในการผลิต</span><span class="sxs-lookup"><span data-stu-id="cc405-114">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="cc405-115">ขั้นตอนนี้จะผ่านระดับโครงสร้าง BOM ทั้งหมดที่เกี่ยวข้องกับใบสั่งผลิตที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="cc405-115">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="cc405-116">เติมความต้องการวัสดุโดยใช้ปริมาณคงคลังคงเหลือที่มีอยู่ ปริมาณคงคลังคงเหลือที่มีอยู่ และแผนการใบสั่งที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="cc405-116">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="cc405-117">ถ้าต้องใช้วัสดุเพิ่มเติมที่ใดก็ตาม แผนการใบสั่งจะถูกสร้างขึ้นเพื่อครอบคลุมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="cc405-117">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="cc405-118">การจัดตารางการผลิตในระหว่างการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="cc405-118">Scheduling during firming</span></span>

<span data-ttu-id="cc405-119">แผนการใบสั่งผลิตรวมรหัสกระบวนการผลิตที่ต้องใช้ในการจัดตารางการผลิต</span><span class="sxs-lookup"><span data-stu-id="cc405-119">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="cc405-120">อย่างไรก็ตาม การสนับสนุนการจัดตารางการผลิตระหว่างการวางแผนการรันของแผนการใบสั่งยังคงค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="cc405-120">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="cc405-121">รหัสกระบวนการผลิตใช้ในการจัดตารางการผลิตแผนการใบสั่งผลิตในระหว่างการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="cc405-121">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="cc405-122">ดังนั้น ระยะเวลารอคอยสินค้าในแผนการใบสั่งผลิต จึงอาจแตกต่างจากระยะเวลารอคอยสินค้าในใบสั่งผลิตที่จัดตารางการผลิตที่เกี่ยวข้องที่ยืนยันไว้ซึ่งสร้างขึ้นจากใบสั่งผลิต ตามที่อธิบายไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="cc405-122">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="cc405-123">**แผนการใบสั่งผลิต** – ระยะเวลารอคอยสินค้าขึ้นอยู่กับระยะเวลารอคอยสินค้าที่คงที่จากผลิตภัณฑ์ที่ปล่อยงานออกใช้</span><span class="sxs-lookup"><span data-stu-id="cc405-123">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="cc405-124">**ใบสั่งผลิตที่ยืนยัน** – ระยะเวลารอคอยสินค้าขึ้นอยู่กับการจัดตารางการผลิตที่ใช้ข้อมูลกระบวนการผลิตและข้อจากข้อจากทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cc405-124">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="cc405-125">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความพร้อมใช้งานของคุณลักษณะที่คาดไว้ ให้ดูที่ [การวิเคราะห์ความเหมาะสมของการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="cc405-125">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="cc405-126">หากคุณขึ้นอยู่กับฟังก์ชันการผลิตที่ยังไม่มีอยู่ในการเพิ่มประสิทธิภาพการวางแผน คุณสามารถใช้กลไกจัดการการวางแผนหลักในตัวต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="cc405-126">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="cc405-127">ไม่มีข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="cc405-127">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="cc405-128">ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="cc405-128">Delays</span></span>

<span data-ttu-id="cc405-129">ถ้าระยะเวลารอคอยสินค้าของวัสดุที่ต้องการยาวกว่ารอบระยะเวลาระหว่างวันที่วันนี้และวันที่ความต้องการวัสดุ แผนการใบสั่งของวัสดุที่ต้องใช้และใบสั่งผลิตที่เกี่ยวข้องจะล่าช้า</span><span class="sxs-lookup"><span data-stu-id="cc405-129">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="cc405-130">ในแผนการใบสั่ง ความล่าช้า (ในหนึ่งวัน) จะคํานวณโดยใช้ระยะเวลารอคอยสินค้าจากผลิตภัณฑ์ที่ปล่อยออกใช้</span><span class="sxs-lookup"><span data-stu-id="cc405-130">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="cc405-131">จากนั้นข้อมูลความล่าช้าจะถูกเผยแพร่ผ่านระดับทั้งหมดของโครงสร้าง BOM</span><span class="sxs-lookup"><span data-stu-id="cc405-131">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="cc405-132">ดังนั้นคุณจึงสามารถติดตามผลกระทบของวัตถุดิบที่ล่าช้าตลอดทางไปยังใบสั่งขายของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cc405-132">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="cc405-133">แก้ไขแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cc405-133">Modifying planned orders</span></span>

<span data-ttu-id="cc405-134">เมื่อคุณเปลี่ยนแปลงข้อมูลในแผนการใบสั่ง คุณจะได้รับข้อความต่อไปนี้ :"โปรดทราบว่าผลกระทบของการเปลี่ยนแปลงด้วยตนเองบนแผนการใบสั่งจะไม่สะท้อนให้เห็นในส่วนที่เหลือของแผนจนกว่าการรันการวางแผนหลักถัดไป"</span><span class="sxs-lookup"><span data-stu-id="cc405-134">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="cc405-135">ถ้าคุณต้องการเปลี่ยนแปลงข้อมูลเกี่ยวกับแผนการใบสั่ง และดูผลกระทบของความต้องการวัสดุที่เกี่ยวข้อง ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cc405-135">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="cc405-136">อัปเดตแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cc405-136">Update the planned order.</span></span>
2. <span data-ttu-id="cc405-137">อนุมัติแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cc405-137">Approve the planned order.</span></span>
3. <span data-ttu-id="cc405-138">ดำเนินการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="cc405-138">Run master planning.</span></span>

<span data-ttu-id="cc405-139">เมื่อคุณรันการวางแผนหลัก คุณไม่ควรใช้ตัวกรองข้อมูลถ้ารวมแผนการใบสั่งผลิตไว้</span><span class="sxs-lookup"><span data-stu-id="cc405-139">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="cc405-140">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ส่วน [ตัวกรอง](#filters) ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="cc405-140">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="cc405-141">ถ้าวันที่จัดส่งของแผนการใบสั่งเปลี่ยนเป็นวันที่ในภายหลัง ความต้องการอาจถูกโยงกับแผนการใบสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="cc405-141">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="cc405-142">ลักษณะการทำงานนี้จะเกิดขึ้นเมื่อวันที่จัดหาวัสดุใหม่จะส่งผลให้เกิดความล่าช้าในความต้องการที่มีการเชื่อมโยงความต้องการกับการจัดหาวัสดุ แต่เพื่อหลีกเลี่ยงความล่าช้าดังกล่าวตามการตั้งค่าระยะเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="cc405-142">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="cc405-143">หน้าการกระจาย</span><span class="sxs-lookup"><span data-stu-id="cc405-143">Explosion page</span></span>

<span data-ttu-id="cc405-144">คุณสามารถใช้หน้า **การกระจาย** เพื่อวิเคราะห์ความต้องการที่ต้องใช้ในใบสั่งผลิตหนึ่ง ๆ หรือแผนการใบสั่งผลิต ความครอบคลุมที่เกี่ยวข้อง และข้อมูลการเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc405-144">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="cc405-145">รายละเอียดบนหน้า **การกระจาย** จะถูกอัปเดตในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="cc405-145">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="cc405-146">คุณไม่สามารถอัปเดตข้อมูลโดยตรงจากหน้า **การกระจาย** ได้</span><span class="sxs-lookup"><span data-stu-id="cc405-146">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="cc405-147">ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc405-147">Filters</span></span>

<span data-ttu-id="cc405-148">สำหรับสถานการณ์การวางแผนที่มีการผลิตรวมอยู่ด้วย เราขอแนะนำว่าคุณควรหลีกเลี่ยงการรันการวางแผนหลักที่มีการกรองข้อมูลแล้ว</span><span class="sxs-lookup"><span data-stu-id="cc405-148">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="cc405-149">เพื่อให้แน่ใจว่าการเพิ่มประสิทธิภาพการวางแผนจะมีข้อมูลที่ต้องใช้ในการคํานวณผลลัพธ์ที่ถูกต้อง คุณต้องรวมผลิตภัณฑ์ทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์ในโครงสร้าง BOM ทั้งหมดของแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cc405-149">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="cc405-150">แม้ว่ารายการรองที่ขึ้นต่อกันจะตรวจพบและรวมอยู่ในการวางแผนหลักโดยอัตโนมัติเมื่อใช้กลไกจัดการการวางแผนหลักในตัว แต่การเพิ่มประสิทธิภาพการวางแผนจะไม่ดำเนินการนี้</span><span class="sxs-lookup"><span data-stu-id="cc405-150">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="cc405-151">ตัวอย่างเช่น ถ้าสลักเกลียวเดียวจากโครงสร้าง BOM ของผลิตภัณฑ์ A ยังใช้ในการผลิตผลิตภัณฑ์ B ผลิตภัณฑ์ทั้งหมดในโครงสร้าง BOM ของผลิตภัณฑ์ A และ B ต้องรวมอยู่ในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="cc405-151">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="cc405-152">เนื่องจากอาจซับซ้อนมากเพื่อให้แน่ใจว่าผลิตภัณฑ์ทั้งหมดเป็นส่วนหนึ่งของตัวกรองข้อมูล เราจึงขอแนะนาว่าคุณควรหลีกเลี่ยงการรันการวางแผนหลักที่กรองข้อมูลแล้วเมื่อเกี่ยวข้องกับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="cc405-152">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]