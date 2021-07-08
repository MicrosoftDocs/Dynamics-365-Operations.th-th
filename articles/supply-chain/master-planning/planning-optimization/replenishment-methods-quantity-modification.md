---
title: วิธีการเติมสินค้าและการแก้ไขปริมาณ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการเติมสินค้าในการเพิ่มประสิทธิภาพการวางแผน และยังอธิบายวิธีการที่ปริมาณการสั่งหลายใบสั่งของผลิตภัณฑ์มีผลกระทบต่อผลลัพธ์
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261707"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="32f4a-104">วิธีการเติมสินค้าและการแก้ไขปริมาณ</span><span class="sxs-lookup"><span data-stu-id="32f4a-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32f4a-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการเติมสินค้าในการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="32f4a-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="32f4a-106">และยังอธิบายวิธีการที่ปริมาณการสั่งหลายใบสั่งของผลิตภัณฑ์มีผลกระทบต่อผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="32f4a-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="32f4a-107">วิธีการเติมสินค้าเรียกอีกอย่างว่าวิธีการครอบคลุมและวิธีการปรับขนาดล็อต</span><span class="sxs-lookup"><span data-stu-id="32f4a-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="32f4a-108">รหัสความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="32f4a-108">Coverage codes</span></span>

<span data-ttu-id="32f4a-109">การเพิ่มประสิทธิภาพการวางแผนสามารถตั้งค่าคอนฟิกเพื่อใช้วิธีการเติมสินค้าที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="32f4a-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="32f4a-110">วิธีการเติมสินค้าคือเทคนิคที่ระบบใช้ในการคํานวณความต้องการผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="32f4a-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="32f4a-111">วิธีการเติมสินค้ากําหนดโดยรหัสความครอบคลุมที่คุณสามารถตั้งค่าในกลุ่มความครอบคลุมหรือผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="32f4a-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="32f4a-112">สามารถใช้รหัสความครอบคลุมต่อไปนี้ในการเพิ่มประสิทธิภาพการวางแผน:</span><span class="sxs-lookup"><span data-stu-id="32f4a-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="32f4a-113">**รอบระยะเวลา** – วิธีการเติมสินค้าซึ่งรวมความต้องการทั้งหมดในรอบระยะเวลาหนึ่งสำหรับผลิตภัณฑ์หนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="32f4a-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="32f4a-114">ใบสั่งจะถูกวางแผนสำหรับวันแรกของรอบระยะเวลา และปริมาณของสินค้าจะเป็นไปตามข้อกำหนดสุทธิในรอบระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="32f4a-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="32f4a-115">รอบระยะเวลาจะเริ่มต้นด้วยความต้องการผลิตภัณฑ์ชิ้นแรกและครอบคลุมระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="32f4a-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="32f4a-116">รอบระยะเวลาถัดไปจะเริ่มต้นจากความต้องการของผลิตภัณฑ์ชิ้นถัดไป</span><span class="sxs-lookup"><span data-stu-id="32f4a-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="32f4a-117">รหัสความครอบคลุม *รอบระยะเวลา* มักใช้สนับสนุนการออกสินค้าคงคลังที่สามารถคาดการณ์ได้ ผลิตภัณฑ์ที่มีอิทธิพลต่อฤดูกาล หรือผลิตภัณฑ์ที่มีต้นทุนสูง</span><span class="sxs-lookup"><span data-stu-id="32f4a-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="32f4a-118">ในแผนภาพต่อไปนี้แสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="32f4a-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="32f4a-119">![ตัวอย่างของการใช้รหัสความครอบคลุมรอบระยะเวลา](./media/coverage-code-period.png "ตัวอย่างของการใช้รหัสความครอบคลุมรอบระยะเวลา")</span><span class="sxs-lookup"><span data-stu-id="32f4a-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="32f4a-120">**ความต้องการ** – ในวิธีการเติมสินค้า ระบบจะสร้างการสั่งซื้อ การโอนย้าย หรือใบสั่งผลิตที่วางแผนไว้แล้ว ต่อความต้องการของแต่ละรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="32f4a-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="32f4a-121">วิธีการนี้จะใช้กับผลิตภัณฑ์ที่มีราคาแพงที่มีความต้องการไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="32f4a-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="32f4a-122">รหัสความครอบคลุม *ความต้องการ* มักใช้เมื่อจัดโครงแบบผลิตภัณฑ์ได้หรือสถานการณ์การผลิตตามสั่ง</span><span class="sxs-lookup"><span data-stu-id="32f4a-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="32f4a-123">ในแผนภาพต่อไปนี้แสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="32f4a-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="32f4a-124">![ตัวอย่างของการใช้รหัสความครอบคลุมความต้องการ](./media/coverage-code-requirement.png "ตัวอย่างของการใช้รหัสความครอบคลุมความต้องการ")</span><span class="sxs-lookup"><span data-stu-id="32f4a-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="32f4a-125">**ค่าน้อยสุด/ค่ามากสุด**</span><span class="sxs-lookup"><span data-stu-id="32f4a-125">**Min./Max.**</span></span> <span data-ttu-id="32f4a-126">– วิธีการเติมสินค้าจะขึ้นอยู่กับระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="32f4a-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="32f4a-127">โดยจะกําหนดการเติมสินค้าคงคลังให้อยู่ในระดับหนึ่งๆ เมื่อระดับปริมาณคงคลังคงเหลือที่คาดการณ์ไว้ต่ำกว่าขีดกําหนดหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="32f4a-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="32f4a-128">ปริมาณการเติมสินค้าจะแตกต่างกันกันไประหว่างระดับสูงสุดและระดับปริมาณคงคลังที่คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="32f4a-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="32f4a-129">*ค่าน้อยสุด/ค่ามากสุด*</span><span class="sxs-lookup"><span data-stu-id="32f4a-129">The *Min./Max.*</span></span> <span data-ttu-id="32f4a-130">รหัสความครอบคลุมมักใช้เพื่อการออกสินค้าคงคลังที่สามารถคาดการณ์ได้ สินค้าราคาขายสูง หรือผลิตภัณฑ์ที่มีราคาแพงน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="32f4a-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="32f4a-131">ในแผนภาพต่อไปนี้แสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="32f4a-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="32f4a-132">![ตัวอย่างของการใช้รหัสความครอบคลุมค่าน้อยสุด/ค่ามากสุด](./media/coverage-code-min-max.png "ตัวอย่างของการใช้รหัสความครอบคลุมค่าน้อยสุด/ค่ามากสุด")</span><span class="sxs-lookup"><span data-stu-id="32f4a-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="32f4a-133">**ด้วยตนเอง** - ในวิธีการเติมสินค้า ระบบจะไม่แนะนำใบสั่งซื้อโอนย้ายหรือใบสั่งผลิตสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="32f4a-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="32f4a-134">แต่ผู้วางแผนผลิตภัณฑ์จะรับผิดชอบการสร้างใบสั่งที่ต้องใช้ในการเติมสินค้าของผลิตภัณฑ์แทน</span><span class="sxs-lookup"><span data-stu-id="32f4a-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="32f4a-135">รหัสความครอบคลุม *ที่ป้อนเอง* มักใช้เฉพาะกับผลิตภัณฑ์ที่แผนการใบสั่งที่ระบบสร้างขึ้นไม่ต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="32f4a-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="32f4a-136">ผลกระทบของปริมาณในใบสั่งจากการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="32f4a-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="32f4a-137">บนหน้า **การตั้งค่าใบสั่งเริ่มต้น** เกี่ยวกับผลิตภัณฑ์ที่นำออกใช้ คุณสามารถระบุการตั้งค่าปริมาณต่างๆ ต่อไปนี้บนแท็บด่วน **ใบสั่งซื้อ** **สินค้าคงคลัง** และ **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="32f4a-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="32f4a-138">(แท็บด่วน **สินค้าคงคลัง** จะใช้สำหรับทั้งใบสั่งโอนย้ายและใบสั่งผลิต)</span><span class="sxs-lookup"><span data-stu-id="32f4a-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="32f4a-139">**ตัวคูณ** – แผนการใบสั่งจะเป็นตัวคูณของปริมาณนี้</span><span class="sxs-lookup"><span data-stu-id="32f4a-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="32f4a-140">ตัวอย่างเช่น ถ้าฟิลด์ **ตัวคูณ** มีการตั้งค่าเป็น *5* ใบสั่งอาจเป็นปริมาณ 5, 10, 15, 20 และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="32f4a-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="32f4a-141">**ปริมาณต่ำสุดของใบสั่ง** – แผนการใบสั่งต้องไม่น้อยกว่าค่าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="32f4a-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="32f4a-142">ตัวอย่างเช่น ถ้าฟิลด์ **ปริมาณต่ำสุดของใบสั่ง** มีการตั้งค่าเป็น *10* จะมีการสร้างแผนการใบสั่งปริมาณ 10 แม้ว่าความต้องการจะต้องใช้เพียงสี่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="32f4a-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="32f4a-143">**ปริมาณสูงสุดของใบสั่ง** – แผนการใบสั่งต้องไม่เกินค่าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="32f4a-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="32f4a-144">ถ้าความต้องการมากกว่าค่า **ปริมาณสูงสุดของใบสั่ง** แผนการใบสั่งหลายแผนจะถูกสร้างขึ้นเพื่อครอบคลุมใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="32f4a-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="32f4a-145">ตัวอย่างเช่น ถ้าฟิลด์ **ปริมาณสูงสุดของใบสั่ง** ถูกตั้งค่าเป็น *100* และความต้องการคือ 450 แผนการใบสั่งสี่แผนในปริมาณเท่ากับ 100 และจะมีการสร้างแผนการใบสั่งหนึ่งแผนการใบสั่งปริมาณ 50</span><span class="sxs-lookup"><span data-stu-id="32f4a-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="32f4a-146">ตัวอย่างของการเติมสินค้าที่ใช้ค่าต่ำสุด/สูงสุด</span><span class="sxs-lookup"><span data-stu-id="32f4a-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="32f4a-147">รหัสความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="32f4a-147">coverage code</span></span>

<span data-ttu-id="32f4a-148">ถ้าคุณไม่ได้ระบุค่าในฟิลด์ **ตัวคูณ** ของผลิตภัณฑ์ในหน้า **การตั้งค่าใบสั่งเริ่มต้น** และถ้าคุณจะใช้ *ค่าน้อยสุด/ค่ามากสุด*</span><span class="sxs-lookup"><span data-stu-id="32f4a-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="32f4a-149">วิธีการเติมสินค้า การเพิ่มประสิทธิภาพการวางแผนจะเติมสินค้าคงคลังให้อยู่ในระดับหนึ่งๆ เมื่อระดับปริมาณคงคลังคงเหลือที่คาดการณ์ไว้ต่ำกว่าขีดกําหนดหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="32f4a-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="32f4a-150">ถ้าคุณกําหนดปริมาณตัวคูณของผลิตภัณฑ์หนึ่งๆ *ต่ำสุด/สูงสุด*</span><span class="sxs-lookup"><span data-stu-id="32f4a-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="32f4a-151">วิธีการเติมสินค้าจะเปลี่ยนลักษณะการทำงานและพิจารณาค่า **ตัวคูณ**</span><span class="sxs-lookup"><span data-stu-id="32f4a-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="32f4a-152">กล่าวอีกอย่างคือ การเพิ่มประสิทธิภาพการวางแผนจะยังคงเติมสินค้าคงคลังให้อยู่ในระดับสูงสุดที่กําหนดไว้เมื่อระดับปริมาณคงคลังคงเหลือที่คาดการณ์ไว้น้อยกว่าระดับต่ำสุดที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="32f4a-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="32f4a-153">อย่างไรก็ตาม ปริมาณการเติมสินค้าจะต้องเป็นตัวคูณของค่า **ตัวคูณ**</span><span class="sxs-lookup"><span data-stu-id="32f4a-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="32f4a-154">ถ้าปริมาณการเติมสินค้า (ผลต่างระหว่างระดับสูงสุดและระดับปริมาณคงคลังคงเหลือที่คาดการณ์ไว้) ไม่ใช่ตัวคูณของปริมาณหลายปริมาณที่กําหนด ประสิทธิภาพการวางแผนจะใช้ค่าแรกที่เป็นไปได้ซึ่งเมื่อใช้ร่วมกับระดับปริมาณคงคลังคงเหลือที่คาดการณ์ไว้ จะต่ำกว่าระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="32f4a-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="32f4a-155">ถ้าผลรวมน้อยกว่าระดับต่ำสุด การเพิ่มประสิทธิภาพการวางแผนจะใช้ค่าแรกที่พร้อมคาดการณ์ไว้ว่าปริมาณคงคลังคงเหลือจะสูงกว่าระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="32f4a-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="32f4a-156">ส่วนย่อยต่อไปนี้แสดงตัวอย่างที่แสดงให้เห็นว่าปริมาณใบสั่งหลายชุดของผลิตภัณฑ์หนึ่งๆ ส่งผลกระทบต่อผลลัพธ์ของค่า *ต่ำสุด/สูงสุด* อย่างไร</span><span class="sxs-lookup"><span data-stu-id="32f4a-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="32f4a-157">วิธีการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="32f4a-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="32f4a-158">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="32f4a-158">Example 1</span></span>

<span data-ttu-id="32f4a-159">ผลิตภัณฑ์มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32f4a-159">A product has the following configuration:</span></span>

- <span data-ttu-id="32f4a-160">**รหัสความครอบคลุม:** *ต่ำสุด/สูงสุด*</span><span class="sxs-lookup"><span data-stu-id="32f4a-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="32f4a-161">**ต่ำสุด:** *15*</span><span class="sxs-lookup"><span data-stu-id="32f4a-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="32f4a-162">**สูงสุด:** *22*</span><span class="sxs-lookup"><span data-stu-id="32f4a-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="32f4a-163">**หลายรายการ:** *0*</span><span class="sxs-lookup"><span data-stu-id="32f4a-163">**Multiple:** *0*</span></span>

<span data-ttu-id="32f4a-164">มีปริมาณคงคลังคงเหลือ 10 ชิ้นของผลิตภัณฑ์และไม่มีความต้องการหรือการจัดหาวัสดุอื่น</span><span class="sxs-lookup"><span data-stu-id="32f4a-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="32f4a-165">เมื่อการวางแผนหลักรัน แผนการใบสั่ง 12 ชิ้นจะถูกสร้างขึ้นเพื่อเติมสินค้าจากสินค้าคงคลังให้ถึงปริมาณสูงสุด</span><span class="sxs-lookup"><span data-stu-id="32f4a-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="32f4a-166">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="32f4a-166">Example 2</span></span>

<span data-ttu-id="32f4a-167">ผลิตภัณฑ์มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32f4a-167">A product has the following configuration:</span></span>

- <span data-ttu-id="32f4a-168">**รหัสความครอบคลุม:** *ต่ำสุด/สูงสุด*</span><span class="sxs-lookup"><span data-stu-id="32f4a-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="32f4a-169">**ต่ำสุด:** *15*</span><span class="sxs-lookup"><span data-stu-id="32f4a-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="32f4a-170">**สูงสุด:** *22*</span><span class="sxs-lookup"><span data-stu-id="32f4a-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="32f4a-171">**หลายรายการ:** *5*</span><span class="sxs-lookup"><span data-stu-id="32f4a-171">**Multiple:** *5*</span></span>

<span data-ttu-id="32f4a-172">มีปริมาณคงคลังคงเหลือ 10 ชิ้นของผลิตภัณฑ์และไม่มีความต้องการหรือการจัดหาวัสดุอื่น</span><span class="sxs-lookup"><span data-stu-id="32f4a-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="32f4a-173">เมื่อการวางแผนหลักรัน แผนการใบสั่ง 10 ชิ้นจะถูกสร้างขึ้น (เนื่องจากการเติมสินค้า 15 ชิ้นบวกปริมาณคงคลังคงเหลือ 10 ชิ้นจะเกินปริมาณสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="32f4a-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="32f4a-174">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="32f4a-174">Example 3</span></span>

<span data-ttu-id="32f4a-175">ผลิตภัณฑ์มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32f4a-175">A product has the following configuration:</span></span>

- <span data-ttu-id="32f4a-176">**รหัสความครอบคลุม:** *ต่ำสุด/สูงสุด*</span><span class="sxs-lookup"><span data-stu-id="32f4a-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="32f4a-177">**ต่ำสุด:** *21*</span><span class="sxs-lookup"><span data-stu-id="32f4a-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="32f4a-178">**สูงสุด:** *24*</span><span class="sxs-lookup"><span data-stu-id="32f4a-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="32f4a-179">**หลายรายการ:** *5*</span><span class="sxs-lookup"><span data-stu-id="32f4a-179">**Multiple:** *5*</span></span>

<span data-ttu-id="32f4a-180">มีปริมาณคงคลังคงเหลือ 10 ชิ้นของผลิตภัณฑ์และไม่มีความต้องการหรือการจัดหาวัสดุอื่น</span><span class="sxs-lookup"><span data-stu-id="32f4a-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="32f4a-181">เมื่อการวางแผนหลักรัน แผนการใบสั่ง 15 ชิ้นจะถูกสร้างขึ้น (เนื่องจากการเติมสินค้า 10 ชิ้นบวกปริมาณคงคลังคงเหลือ 10 ชิ้นจะน้อยกว่าปริมาณต่ำสุด)</span><span class="sxs-lookup"><span data-stu-id="32f4a-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
