---
title: การวางแผนที่มีปริมาณคงคลังคงเหลือที่เป็นค่าลบ
description: หัวข้อนี้จะอธิบายวิธีการจัดการปริมาณคงคลังคงเหลือที่เป็นค่าลบ เมื่อคุณใช้การเพิ่มประสิทธิภาพของการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8803b0b90f22711b844442d16f717ab87dabf041
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209869"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="c56fb-103">การวางแผนที่มีปริมาณคงคลังคงเหลือที่เป็นค่าลบ</span><span class="sxs-lookup"><span data-stu-id="c56fb-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c56fb-104">ถ้าระบบแสดงปริมาณคงคลังคงเหลือแบบรวมที่เป็นค่าลบ กลไกจัดการการวางแผนจะถือว่าปริมาณเป็น 0 (ศูนย์) เพื่อช่วยหลีกเลี่ยงการจัดหาวัสดุมากเกินไป</span><span class="sxs-lookup"><span data-stu-id="c56fb-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="c56fb-105">วิธีการทำงานของฟังก์ชันนี้มีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="c56fb-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="c56fb-106">คุณลักษณะการเพิ่มประสิทธิภาพการวางแผนรวมปริมาณคงคลังคงเหลือที่ระดับมิติความครอบคลุมต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="c56fb-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="c56fb-107">(ตัวอย่างเช่น ถ้า *สถานที่* ไม่ใช่มิติความครอบคลุม การเพิ่มประสิทธิภาพการวางแผนรวมปริมาณคงคลังคงเหลือที่ระดับ *คลังสินค้า*)</span><span class="sxs-lookup"><span data-stu-id="c56fb-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="c56fb-108">ถ้าปริมาณคงคลังคงเหลือแบบรวมที่ระดับที่ต่ำที่สุดของมิติความครอบคลุมเป็นค่าลบ ระบบจะสันนิษฐานว่าปริมาณคงคลังคงเหลือเป็น 0 (ศูนย์) จริงๆ</span><span class="sxs-lookup"><span data-stu-id="c56fb-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c56fb-109">ระบบการวางแผนอาจมีความแม่นยำได้เท่ากับข้อมูลที่ป้อนเข้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="c56fb-110">ถ้าข้อมูลป้อนเข้าไม่ถูกต้อง เรกคอร์ดของปริมาณคงคลังคงเหลือที่เป็นค่าลบจะบ่งชี้ว่าข้อมูลสินค้าคงคลังใน Microsoft Dynamics 365 Supply Chain Management ไม่ได้ซิงค์กับโลกแห่งความจริง</span><span class="sxs-lookup"><span data-stu-id="c56fb-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="c56fb-111">ดังนั้น ผลลัพธ์ของการวางแผนจะบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c56fb-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="c56fb-112">เมื่อต้องการดูผลลัพธ์ของการวางแผนที่แม่นยำ คุณควรลดจำนวนเรกคอร์ดที่แสดงปริมาณคงคลังคงเหลือที่เป็นค่าลบ</span><span class="sxs-lookup"><span data-stu-id="c56fb-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="c56fb-113">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="c56fb-113">Example 1</span></span>

<span data-ttu-id="c56fb-114">คลังสินค้า 13 มีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c56fb-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="c56fb-115">**รหัสความครอบคลุม:** ต่ำสุด/สูงสุด</span><span class="sxs-lookup"><span data-stu-id="c56fb-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="c56fb-116">**ขั้นต่ำ:** 15 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="c56fb-117">**สูงสุด:** 25 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="c56fb-118">ระดับของมิติความครอบคลุมต่ำสุดคือ *คลังสินค้า* และปริมาณคงคลังคงเหลือต่อไปนี้จะถูกบันทึกในระดับ *สถานที่*:</span><span class="sxs-lookup"><span data-stu-id="c56fb-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="c56fb-119">**ไซต์ 1 คลังสินค้า 13 สถานที่ 1:** 20 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="c56fb-120">**ไซต์ 1 คลังสินค้า 13 สถานที่ 2:** &minus;8 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="c56fb-121">ดังนั้น ปริมาณคงคลังคงเหลือแบบรวมสำหรับคลังสินค้า 13 คือ 12 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="c56fb-122">(= 20 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-122">(= 20 pcs.</span></span> <span data-ttu-id="c56fb-123">&minus; 8 ชิ้น)</span><span class="sxs-lookup"><span data-stu-id="c56fb-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="c56fb-124">ในกรณีนี้ กลไกจัดการการวางแผนจะใช้ปริมาณคงคลังคงเหลือแบบรวมเป็น 12 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="c56fb-125">สำหรับคลังสินค้า 13</span><span class="sxs-lookup"><span data-stu-id="c56fb-125">for warehouse 13.</span></span>

<span data-ttu-id="c56fb-126">ผลลัพธ์คือแผนการใบสั่งของ 13 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="c56fb-127">(= 25 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-127">(= 25 pcs.</span></span> <span data-ttu-id="c56fb-128">&minus; 12 ชิ้น) เมื่อต้องการเติมสินค้าในคลังสินค้า 13 จาก 12 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="c56fb-129">เป็น 25 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="c56fb-130">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="c56fb-130">Example 2</span></span>

<span data-ttu-id="c56fb-131">คลังสินค้า 13 มีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c56fb-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="c56fb-132">**รหัสความครอบคลุม:** ต่ำสุด/สูงสุด</span><span class="sxs-lookup"><span data-stu-id="c56fb-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="c56fb-133">**ขั้นต่ำ:** 15 pcs</span><span class="sxs-lookup"><span data-stu-id="c56fb-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="c56fb-134">**สูงสุด:** 25 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="c56fb-135">ระดับของมิติความครอบคลุมต่ำสุดคือ *คลังสินค้า* และปริมาณคงคลังคงเหลือต่อไปนี้จะถูกบันทึกในระดับ *สถานที่*:</span><span class="sxs-lookup"><span data-stu-id="c56fb-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="c56fb-136">**ไซต์ 1 คลังสินค้า 13 สถานที่ 1:** 4 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="c56fb-137">**ไซต์ 1 คลังสินค้า 13 สถานที่ 2:** &minus;8 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="c56fb-138">ดังนั้น ปริมาณคงคลังคงเหลือแบบรวมสำหรับคลังสินค้า 13 คือ &minus;4 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="c56fb-139">(= 4 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-139">(= 4 pcs.</span></span> <span data-ttu-id="c56fb-140">&minus; 8 ชิ้น)</span><span class="sxs-lookup"><span data-stu-id="c56fb-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="c56fb-141">กล่าวอีกอย่างหนึ่งคือ น้อยกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="c56fb-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="c56fb-142">ในกรณีนี้ กลไกจัดการการวางแผนจะสันนิษฐานว่าปริมาณคงคลังคงเหลือสำหรับคลังสินค้า 13 คือ 0 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="c56fb-143">แทนที่จะเป็น &minus;4 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="c56fb-144">ผลลัพธ์คือแผนการใบสั่ง 25 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="c56fb-145">(= 25 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-145">(= 25 pcs.</span></span> <span data-ttu-id="c56fb-146">&minus; 0 ชิ้น) เมื่อต้องการเติมสินค้าในคลังสินค้า 13 จาก 0 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="c56fb-147">เป็น 25 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="c56fb-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c56fb-148">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c56fb-148">Related resources</span></span>

[<span data-ttu-id="c56fb-149">ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c56fb-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="c56fb-150">เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c56fb-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="c56fb-151">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c56fb-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="c56fb-152">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c56fb-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="c56fb-153">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c56fb-153">Cancel a planning job</span></span>](cancel-planning-job.md)
