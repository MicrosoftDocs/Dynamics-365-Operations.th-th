---
title: การตั้งค่าคอนฟิกต้นทุนสำหรับการจัดการใบสั่งแบบกระจาย (DOM)
description: หัวข้อนี้อธิบายถึงฟังก์ชันการตั้งค่าคอนฟิกต้นทุนสำหรับการจัดการใบสั่งแบบกระจาย (DOM) ใน Microsoft Dynamics 365 for Retail
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80e7a033467c3d94d55f06daa05f99bd27e19a29
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606790"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="0ff21-103">การตั้งค่าคอนฟิกต้นทุนสำหรับการจัดการใบสั่งแบบกระจาย (DOM)</span><span class="sxs-lookup"><span data-stu-id="0ff21-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ff21-104">องค์กรต่างๆ จะพิจารณาส่วนประกอบของต้นทุนหลายอย่างเพื่อกำหนดสถานที่ตั้งที่เหมาะสมที่สุดในการเติมสินค้าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="0ff21-105">ส่วนประกอบของต้นทุนเหล่านี้บางส่วนเป็นต้นทุนค่าจัดส่งสินค้า ต้นทุนค่าการจัดการ และต้นทุนค่าบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0ff21-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="0ff21-106">ชุดข้อมูลต้นทุนเหล่านี้จะมีการคำนวณเพื่อกำหนดสถานที่ตั้งในการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="0ff21-107">เมื่อการจัดการใบสั่งแบบกระจาย (DOM) เกิดซ้ำเป็นครั้งแรกใน Microsoft Dynamics 365 for Retail ที่ปรับให้เหมาะกับการกำหนดใบสั่งไปยังสถานที่ตั้งในการเติมสินค้า จะมีการนำระยะทางมาร่วมพิจารณาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ff21-107">When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="0ff21-108">แม้ว่าระยะทางจะสัมพันธ์กับต้นทุน แต่ก็ไม่ได้เหมือนกับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="0ff21-109">ตัวอย่างเช่น วิธีการจัดส่งสินค้าแบบข้ามคืนมีต้นทุนมากกว่าการจัดส่งสินค้าภายในสามวันหรือการจัดส่งสินค้าภายในเจ็ดวันสำหรับระยะทางที่เท่ากัน</span><span class="sxs-lookup"><span data-stu-id="0ff21-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="0ff21-110">คุณลักษณะการตั้งค่าคอนฟิกต้นทุนช่วยให้ผู้ขายปลีกสามารถกำหนดและตั้งค่าคอนฟิกส่วนประกอบของต้นทุนเพิ่มเติมที่จะคำนวณและนำมาร่วมพิจารณาเพื่อกำหนดสถานที่ตั้งที่เหมาะสมที่สุดในการเติมสินค้าของรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="0ff21-111">เมื่อตั้งค่าคอนฟิกส่วนประกอบของต้นทุน โปรแกรมแก้ปัญหา DOM จะใช้เฉพาะข้อกำหนดต้นทุนเหล่านั้นในการกำหนดสถานที่ตั้งที่เหมาะสมที่สุดสำหรับการเติมสินค้าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="0ff21-112">ข้อกำหนดดังกล่าวจะไม่ถือว่าส่วนประกอบระยะทางเป็นต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="0ff21-113">อย่างไรก็ตาม หากไม่ได้ตั้งค่าคอนฟิกส่วนประกอบของต้นทุน โปรแกรมแก้ปัญหา DOM จะใช้ส่วนประกอบระยะทางเป็นต้นทุนในการกำหนดสถานที่ตั้งที่เหมาะสมที่สุดสำหรับการเติมสินค้าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="0ff21-114">ตั้งค่าส่วนประกอบของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-114">Set up cost components</span></span>

<span data-ttu-id="0ff21-115">สามารถกำหนดชนิดส่วนประกอบของต้นทุนหลักๆ สองอย่างไว้ในระบบ: **การจัดส่งสินค้า** และ **อื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="0ff21-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="0ff21-116">ชนิดส่วนประกอบของต้นทุนทั้งคู่จะรองรับฐานการคำนวณหลายรายการดังที่แสดงอยู่ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0ff21-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0ff21-117">ชนิดส่วนประกอบของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-117">Cost component type</span></span></th>
<th><span data-ttu-id="0ff21-118">เกณฑ์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="0ff21-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0ff21-119">การจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0ff21-120">แบบง่าย</span><span class="sxs-lookup"><span data-stu-id="0ff21-120">Simple</span></span></li>
<li><span data-ttu-id="0ff21-121">ที่จัดระดับ</span><span class="sxs-lookup"><span data-stu-id="0ff21-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="0ff21-122">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="0ff21-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0ff21-123">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0ff21-123">Sales order</span></span></li>
<li><span data-ttu-id="0ff21-124">รายการขาย</span><span class="sxs-lookup"><span data-stu-id="0ff21-124">Sales line</span></span></li>
<li><span data-ttu-id="0ff21-125">สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="0ff21-126">ชนิดส่วนประกอบของต้นทุนการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-126">Shipping cost component type</span></span>

<span data-ttu-id="0ff21-127">ข้อมูลส่วนนี้จะอธิบายวิธีการตั้งค่าแต่ละชุดข้อมูลชนิดส่วนประกอบของต้นทุน **การจัดส่งสินค้า** และเกณฑ์การคำนวณสำหรับต้นทุนการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="0ff21-128">พร้อมกับอธิบายวิธีการที่โปรแกรมแก้ปัญหา DOM ใช้แต่ละชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0ff21-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="0ff21-129">ชนิดส่วนประกอบของต้นทุน = การจัดส่งสินค้าและเกณฑ์การคำนวณ = แบบง่าย</span><span class="sxs-lookup"><span data-stu-id="0ff21-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="0ff21-130">หากมีการใช้ชุดข้อมูลชนิดส่วนประกอบของต้นทุน **การจัดส่งสินค้า** และเกณฑ์การคำนวณ **แบบง่าย** ต้นทุนการจัดส่งสินค้าสำหรับวิธีการจัดส่งจะยึดตามต้นทุนแบบคงที่หรือระยะทาง</span><span class="sxs-lookup"><span data-stu-id="0ff21-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="0ff21-131">คุณต้องตั้งค่าฟิลด์ต่อไปนี้สำหรับชุดข้อมูลนี้:</span><span class="sxs-lookup"><span data-stu-id="0ff21-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="0ff21-132">**ตัวแปรต้นทุน** – ป้อนตัวระบุเฉพาะสำหรับตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="0ff21-133">**คำอธิบาย** – ป้อนชื่อและคำอธิบายของตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="0ff21-134">**วันที่เริ่มต้น** และ **วันที่สิ้นสุด** – คุณสามารถใช้ฟิลด์เหล่านี้เพื่อจำกัดตัวแปรต้นทุนสำหรับช่วงวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0ff21-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="0ff21-135">ถ้าคุณปล่อยให้ฟิลด์เหล่านี้ว่างเปล่า ตัวแปรต้นทุนจะใช้ได้สำหรับรอบระยะเวลาที่ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="0ff21-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="0ff21-136">**ใช้งาน** – แสดงว่าใช้งานตัวแปรต้นทุนอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0ff21-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="0ff21-137">DOM จะพิจารณาเฉพาะตัวแปรต้นทุนที่ใช้งานซึ่งเชื่อมโยงกับโพรไฟล์การเติมสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ff21-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="0ff21-138">**บริษัท** – ระบุนิติบุคคลที่มีการตั้งค่าคอนฟิกตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="0ff21-139">รายการของเกณฑ์การคำนวณทั้งหมดต้องใช้สำหรับนิติบุคคลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0ff21-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="0ff21-140">**วิธีการจัดส่ง** – ระบุวิธีการจัดส่งที่มีการตั้งค่าคอนฟิกต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="0ff21-141">**ชนิดการคำนวณ** – ระบุวิธีที่ควรมีการคำนวณต้นทุนสำหรับวิธีการจัดส่งเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0ff21-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="0ff21-142">รองรับชนิดการคำนวณสองแบบคือ:</span><span class="sxs-lookup"><span data-stu-id="0ff21-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="0ff21-143">**คงที่** – ต้นทุนแบบคงที่ใช้สำหรับวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="0ff21-144">หากคุณเลือกชนิดการคำนวณนี้ ฟิลด์ **ต้นทุน** จะกำหนดต้นทุนแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="0ff21-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="0ff21-145">**ต่อหน่วยของระยะทาง** – ต้นทุนสำหรับวิธีการจัดส่งได้รับการคำนวณเมื่อมูลค่าต้นทุนที่ระบุไว้ในฟิลด์ **ต้นทุน** กำหนดเวลาที่ใช้สำหรับระยะทางระหว่างที่อยู่ที่จัดส่งและสถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="0ff21-146">**ต้นทุน** – ระบุมูลค่าต้นทุนที่ใช้ร่วมกับฟิลด์ **ชนิดการคำนวณ** เพื่อคำนวณต้นทุนสำหรับวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="0ff21-147">ชนิดส่วนประกอบของต้นทุน = การจัดส่งสินค้าและเกณฑ์การคำนวณ = ที่จัดระดับ</span><span class="sxs-lookup"><span data-stu-id="0ff21-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="0ff21-148">หากมีการใช้ชุดข้อมูลชนิดส่วนประกอบของต้นทุน **การจัดส่งสินค้า** และเกณฑ์การคำนวณ **ที่จัดระดับ** ต้นทุนการจัดส่งสินค้าสำหรับวิธีการจัดส่งจะยึดตามต้นทุนแบบคงที่หรือระยะทาง</span><span class="sxs-lookup"><span data-stu-id="0ff21-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="0ff21-149">อย่างไรก็ตาม ในชุดข้อมูลนี้ ระยะทางมีการยึดตามช่วงของระยะทางที่จัดระดับ</span><span class="sxs-lookup"><span data-stu-id="0ff21-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="0ff21-150">คุณต้องตั้งค่าฟิลด์ต่อไปนี้สำหรับชุดข้อมูลนี้:</span><span class="sxs-lookup"><span data-stu-id="0ff21-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="0ff21-151">**ตัวแปรต้นทุน** – ป้อนตัวระบุเฉพาะสำหรับตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="0ff21-152">**คำอธิบาย** – ป้อนชื่อและคำอธิบายของตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="0ff21-153">**ต้นทุนเริ่มต้น** – ระบุต้นทุนที่ควรใช้สำหรับวิธีการจัดส่งหากระยะทางระหว่างที่อยู่ที่จัดส่งและสถานที่ตั้งไม่อยู่ในระยะทางที่จัดระดับใดๆ สำหรับวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="0ff21-154">**วันที่เริ่มต้น** และ **วันที่สิ้นสุด** – คุณสามารถใช้ฟิลด์เหล่านี้เพื่อจำกัดตัวแปรต้นทุนสำหรับช่วงวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0ff21-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="0ff21-155">ถ้าคุณปล่อยให้ฟิลด์เหล่านี้ว่างเปล่า ตัวแปรต้นทุนจะใช้ได้สำหรับรอบระยะเวลาที่ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="0ff21-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="0ff21-156">**ใช้งาน** – แสดงว่าใช้งานตัวแปรต้นทุนอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0ff21-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="0ff21-157">DOM จะพิจารณาเฉพาะตัวแปรต้นทุนที่ใช้งานซึ่งเชื่อมโยงกับโพรไฟล์การเติมสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ff21-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="0ff21-158">**บริษัท** – ระบุนิติบุคคลที่มีการตั้งค่าคอนฟิกตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="0ff21-159">รายการของเกณฑ์การคำนวณทั้งหมดต้องใช้สำหรับนิติบุคคลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0ff21-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="0ff21-160">**วิธีการจัดส่ง** – ระบุวิธีการจัดส่งที่มีการตั้งค่าคอนฟิกต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="0ff21-161">**ชนิดระยะทาง** – ระบุว่าข้อกำหนดระยะทางที่จัดระดับเป็นระยะทางทางอากาศหรือระยะทางทางถนน</span><span class="sxs-lookup"><span data-stu-id="0ff21-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="0ff21-162">**หน่วยระยะทาง** – ระบุหน่วยที่ใช้ในการวัดระยะทางที่จัดระดับ</span><span class="sxs-lookup"><span data-stu-id="0ff21-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="0ff21-163">**ระยะทางเริ่มต้น** – ระบุช่วงเริ่มต้นสำหรับระยะทางที่จัดระดับ</span><span class="sxs-lookup"><span data-stu-id="0ff21-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="0ff21-164">**ระยะทางสิ้นสุด** – ระบุช่วงสิ้นสุดสำหรับระยะทางที่จัดระดับ</span><span class="sxs-lookup"><span data-stu-id="0ff21-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="0ff21-165">**ชนิดการคำนวณ** – ระบุวิธีที่ควรมีการคำนวณต้นทุนสำหรับวิธีการจัดส่งเฉพาะและระยะทางที่จัดระดับ</span><span class="sxs-lookup"><span data-stu-id="0ff21-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="0ff21-166">รองรับชนิดการคำนวณสองแบบคือ:</span><span class="sxs-lookup"><span data-stu-id="0ff21-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="0ff21-167">**คงที่** – ต้นทุนแบบคงที่ใช้สำหรับวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="0ff21-168">หากคุณเลือกชนิดการคำนวณนี้ ฟิลด์ **ต้นทุน** จะกำหนดต้นทุนแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="0ff21-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="0ff21-169">**ต่อหน่วยของระยะทาง** – ต้นทุนสำหรับวิธีการจัดส่งและระยะทางที่จัดระดับได้รับการคำนวณเมื่อมูลค่าต้นทุนที่ระบุไว้ในฟิลด์ **ต้นทุน** กำหนดเวลาที่ใช้สำหรับระยะทางระหว่างที่อยู่ที่จัดส่งและสถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="0ff21-170">**ต้นทุน** – ระบุมูลค่าต้นทุนที่ใช้ร่วมกับฟิลด์ **ชนิดการคำนวณ** เพื่อคำนวณต้นทุนสำหรับวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="0ff21-171">เมื่อคุณกำหนดระยะทางที่จัดระดับ ระบบจะตรวจสอบว่าไม่มีระยะทางที่ขาดหายไปหรือระยะทางที่ทับซ้อน</span><span class="sxs-lookup"><span data-stu-id="0ff21-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="0ff21-172">ชนิดระยะทางที่ใช้สำหรับวิธีการจัดส่งต้องเท่ากันกับระยะทางที่จัดระดับทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0ff21-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="0ff21-173">ชนิดส่วนประกอบของต้นทุนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="0ff21-173">Other cost component type</span></span>

<span data-ttu-id="0ff21-174">ข้อมูลส่วนนี้จะอธิบายวิธีการตั้งค่าแต่ละชุดข้อมูลชนิดส่วนประกอบของต้นทุน **อื่นๆ** และชนิดต้นทุนอื่นๆ สำหรับต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="0ff21-175">พร้อมกับอธิบายวิธีการที่โปรแกรมแก้ปัญหา DOM ใช้แต่ละชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0ff21-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="0ff21-176">ชนิดส่วนประกอบของต้นทุน = อื่นๆ และชนิดต้นทุนอื่นๆ = ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0ff21-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="0ff21-177">ชุดข้อมูลชนิดส่วนประกอบของต้นทุน **อื่นๆ** และชนิดต้นทุนอื่นๆ ของ **ใบสั่งขาย** จะใช้ในการกำหนดต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้าในระดับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0ff21-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="0ff21-178">คุณต้องตั้งค่าฟิลด์ต่อไปนี้สำหรับชุดข้อมูลนี้:</span><span class="sxs-lookup"><span data-stu-id="0ff21-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="0ff21-179">**ตัวแปรต้นทุน** – ป้อนตัวระบุเฉพาะสำหรับตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="0ff21-180">**คำอธิบาย** – ป้อนชื่อและคำอธิบายของตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="0ff21-181">**วันที่เริ่มต้น** และ **วันที่สิ้นสุด** – คุณสามารถใช้ฟิลด์เหล่านี้เพื่อจำกัดตัวแปรต้นทุนสำหรับช่วงวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0ff21-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="0ff21-182">ถ้าคุณปล่อยให้ฟิลด์เหล่านี้ว่างเปล่า ตัวแปรต้นทุนจะใช้ได้สำหรับรอบระยะเวลาที่ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="0ff21-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="0ff21-183">**ใช้งาน** – แสดงว่าใช้งานตัวแปรต้นทุนอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0ff21-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="0ff21-184">DOM จะพิจารณาเฉพาะตัวแปรต้นทุนที่ใช้งานซึ่งเชื่อมโยงกับโพรไฟล์การเติมสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ff21-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="0ff21-185">**ต้นทุน** – ระบุมูลค่าต้นทุนสำหรับต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้าในระดับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0ff21-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="0ff21-186">ชนิดส่วนประกอบของต้นทุน = อื่นๆ และชนิดต้นทุนอื่นๆ = รายการขาย</span><span class="sxs-lookup"><span data-stu-id="0ff21-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="0ff21-187">ชุดข้อมูลชนิดส่วนประกอบของต้นทุน **อื่นๆ** และชนิดต้นทุนอื่นๆ เป็น **รายการขาย** จะใช้ในการกำหนดต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้าในระดับรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0ff21-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="0ff21-188">คุณต้องตั้งค่าฟิลด์ต่อไปนี้สำหรับชุดข้อมูลนี้:</span><span class="sxs-lookup"><span data-stu-id="0ff21-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="0ff21-189">**ตัวแปรต้นทุน** – ป้อนตัวระบุเฉพาะสำหรับตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="0ff21-190">**คำอธิบาย** – ป้อนชื่อและคำอธิบายของตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="0ff21-191">**วันที่เริ่มต้น** และ **วันที่สิ้นสุด** – คุณสามารถใช้ฟิลด์เหล่านี้เพื่อจำกัดตัวแปรต้นทุนสำหรับช่วงวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0ff21-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="0ff21-192">ถ้าคุณปล่อยให้ฟิลด์เหล่านี้ว่างเปล่า ตัวแปรต้นทุนจะใช้ได้สำหรับรอบระยะเวลาที่ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="0ff21-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="0ff21-193">**ใช้งาน** – แสดงว่าใช้งานตัวแปรต้นทุนอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0ff21-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="0ff21-194">DOM จะพิจารณาเฉพาะตัวแปรต้นทุนที่ใช้งานซึ่งเชื่อมโยงกับโพรไฟล์การเติมสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ff21-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="0ff21-195">**ต้นทุน** – ระบุมูลค่าต้นทุนสำหรับต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้าในระดับรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0ff21-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="0ff21-196">ชนิดส่วนประกอบของต้นทุน = อื่นๆ และชนิดต้นทุนอื่นๆ = สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="0ff21-197">ชุดข้อมูลชนิดส่วนประกอบของต้นทุน **อื่นๆ** และชนิดต้นทุนอื่นๆ เป็น **สถานที่ตั้ง** จะใช้ในการกำหนดต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้าสำหรับกลุ่มของสถานที่ตั้งหรือสถานที่ตั้งแต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="0ff21-198">คุณต้องตั้งค่าฟิลด์ต่อไปนี้สำหรับชุดข้อมูลนี้:</span><span class="sxs-lookup"><span data-stu-id="0ff21-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="0ff21-199">**ตัวแปรต้นทุน** – ป้อนตัวระบุเฉพาะสำหรับตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="0ff21-200">**คำอธิบาย** – ป้อนชื่อและคำอธิบายของตัวแปรต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ff21-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="0ff21-201">**วันที่เริ่มต้น** และ **วันที่สิ้นสุด** – คุณสามารถใช้ฟิลด์เหล่านี้เพื่อจำกัดตัวแปรต้นทุนสำหรับช่วงวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0ff21-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="0ff21-202">ถ้าคุณปล่อยให้ฟิลด์เหล่านี้ว่างเปล่า ตัวแปรต้นทุนจะใช้ได้สำหรับรอบระยะเวลาที่ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="0ff21-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="0ff21-203">**ใช้งาน** – แสดงว่าใช้งานตัวแปรต้นทุนอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0ff21-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="0ff21-204">DOM จะพิจารณาเฉพาะตัวแปรต้นทุนที่ใช้งานซึ่งเชื่อมโยงกับโพรไฟล์การเติมสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ff21-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="0ff21-205">**กลุ่มการเติมสินค้า** – ระบุกลุ่มของสถานที่ตั้งที่มีการกำหนดต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="0ff21-206">**สถานที่ตั้งในการเติมสินค้า** – ระบุสถานที่ตั้งที่มีการกำหนดต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ff21-207">คุณไม่สามารถระบุกลุ่มการเติมสินค้าและสถานที่ตั้งในการเติมสินค้าเป็นรายการเดียวกันสำหรับเกณฑ์การคำนวณตามสถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="0ff21-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="0ff21-208">**ต้นทุน** – ระบุมูลค่าต้นทุนสำหรับต้นทุนที่ไม่ใช่ค่าจัดส่งสินค้าในระดับกลุ่มการเติมสินค้าหรือระดับสถานที่ตั้งในการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ff21-209">สำหรับ DOM ที่จะพิจารณาต้นทุนเหล่านี้เมื่อดำเนินการ คุณต้องเพิ่มตัวแปรต้นทุนลงในโพรไฟล์การเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="0ff21-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
