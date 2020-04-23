---
title: การประเมินต้นทุนใบสั่งผลิต
description: บทความนี้แสดงข้อมูลเกี่ยวกับการประเมินต้นทุนการผลิต  การประเมินต้นทุนการผลิตให้วัสดุที่คาดการณ์ไว้ และต้นทุนปริมาณการใช้ของกำลังการผลิตของการผลิตสินค้าในปริมาณใบสั่งผลิตตามแผน
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a101f82e60113941d389421b19cddc1ad123ce9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214538"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="39924-104">การประเมินต้นทุนใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="39924-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39924-105">บทความนี้แสดงข้อมูลเกี่ยวกับการประเมินต้นทุนการผลิต </span><span class="sxs-lookup"><span data-stu-id="39924-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="39924-106">การประเมินต้นทุนการผลิตให้วัสดุที่คาดการณ์ไว้ และต้นทุนปริมาณการใช้ของกำลังการผลิตของการผลิตสินค้าในปริมาณใบสั่งผลิตตามแผน</span><span class="sxs-lookup"><span data-stu-id="39924-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="39924-107">หลังจากที่คุณสร้างใบสั่งผลิต คุณต้องประเมินต้นทุนการผลิต </span><span class="sxs-lookup"><span data-stu-id="39924-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="39924-108">วัตถุประสงค์คือเพื่อประเมินปริมาณการใช้สินค้าและกระบวนการผลิตสำหรับกระบวนการผลิต เนื่องจากการประเมินเหล่านี้จะถูกใช้เป็นข้อมูลพื้นฐานสำหรับกระบวนการผลิตและการจัดกำหนดการในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="39924-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="39924-109">การประเมินต้นทุนการผลิต</span><span class="sxs-lookup"><span data-stu-id="39924-109">Production cost estimation</span></span>
<span data-ttu-id="39924-110">การประเมินต้นทุนการผลิตเป็นไปตามข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="39924-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="39924-111">ปริมาณในใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="39924-111">The quantity on the production order</span></span>
-   <span data-ttu-id="39924-112">ส่วนประกอบในสูตรการผลิต (BOMs)</span><span class="sxs-lookup"><span data-stu-id="39924-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="39924-113">ขั้นตอนของกระบวนการผลิตในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="39924-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="39924-114">ต้นทุนทางอ้อมที่ใช้กับส่วนประกอบและการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="39924-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="39924-115">ข้อมูลต้นทุนที่ใช้งาน ณ วันที่มีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="39924-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="39924-116">ถ้ามีสินค้าในรายการแฝงอยู่ใน BOMs สำหรับการผลิต การคำนวณสะท้อนถึงส่วนประกอบของรายการแฝง และขั้นตอนของกระบวนการผลิต </span><span class="sxs-lookup"><span data-stu-id="39924-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="39924-117">คุณสามารถใช้งานการประเมินเพื่อคำนวณต้นทุนที่ประเมินใหม่ เพื่อที่จะสะท้อนถึงข้อมูลที่อัพเดตแล้ว </span><span class="sxs-lookup"><span data-stu-id="39924-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="39924-118">ตัวอย่างเช่น ข้อมูลที่อัพเดตแล้วอาจเป็นการเปลี่ยนแปลงปริมาณในใบสั่งผลิต ส่วนประกอบใน BOMs ของกระบวนการผลิต ขั้นตอนของกระบวนการผลิตในกระบวนการผลิต ต้นทุนทางอ้อมที่ใช้กับองค์ประกอบเหล่านี้และการดำเนินงาน หรือข้อมูลต้นทุนที่ใช้งาน ณ วันที่มีการคำนวณใหม่ </span><span class="sxs-lookup"><span data-stu-id="39924-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="39924-119">การคำนวณต้นทุนที่ประเมินยังแนะนำราคาขายสำหรับสินค้าการผลิต ซึ่งใช้วิธีต้นทุนบวกการเพิ่มราคา </span><span class="sxs-lookup"><span data-stu-id="39924-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="39924-120">อีกทางหนึ่งคือ การคำนวณของต้นทุนที่ประเมินสามารถใช้กับใบสั่งอ้างอิงที่สะท้อนถึงใบสั่งผลิตอื่นๆที่เชื่อมโยงกับใบสั่งผลิตได้</span><span class="sxs-lookup"><span data-stu-id="39924-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="39924-121">ดูต้นทุนที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="39924-121">View the estimated costs</span></span>
<span data-ttu-id="39924-122">หลังจากที่คุณรันการประเมิน คุณสามารถดูผลลัพธ์ในหน้า **การคำนวณราคา** ได้</span><span class="sxs-lookup"><span data-stu-id="39924-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="39924-123">การประเมินคำนวณค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="39924-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="39924-124">**ต้นทุนการผลิต** – ต้นทุนการผลิตเป็นรายการบนสุดของการประเมิน</span><span class="sxs-lookup"><span data-stu-id="39924-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="39924-125">ต้นทุนการผลิตแสดงต้นทุนทั้งหมดของการรันใบสั่งผลิต และราคาขายรวมสำหรับการผลิต </span><span class="sxs-lookup"><span data-stu-id="39924-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="39924-126">เป็นผลรวมของรายการต้นทุนทั้งหมดในการประเมิน</span><span class="sxs-lookup"><span data-stu-id="39924-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="39924-127">**ต้นทุนกระบวนการผลิตหรือทรัพยากร** – ต้นทุนกระบวนการผลิตหรือทรัพยากร เป็นต้นทุนของการดำเนินงานการผลิต</span><span class="sxs-lookup"><span data-stu-id="39924-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="39924-128">ซึ่งรวมถึงต้นทุนขององค์ประกอบ เช่น เวลาการตั้งค่า เวลาที่ใช้ในการรัน และค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="39924-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="39924-129">**ต้นทุนวัสดุ** – ต้นทุนวัสดุเป็นต้นทุนและราคาของส่วนประกอบ BOM ที่ต้องใช้เพื่อผลิตสินค้า</span><span class="sxs-lookup"><span data-stu-id="39924-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="39924-130">ก่อนหน้านี้ ต้นทุนเหล่านี้ได้ถูกสร้างและป้อนเข้าในระบบไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="39924-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="39924-131">การใช้งานอื่นๆของการประเมินต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39924-131">Other uses of cost estimation</span></span>
<span data-ttu-id="39924-132">การประเมินต้นทุนยังให้ข้อมูลต่อไปนี้อีกด้วย:</span><span class="sxs-lookup"><span data-stu-id="39924-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="39924-133">ใบเสนอราคาที่มีประโยชน์</span><span class="sxs-lookup"><span data-stu-id="39924-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="39924-134">การประเมินผลกำไรของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="39924-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="39924-135">การประเมินการใช้วัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="39924-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="39924-136">การเปรียบเทียบข้อมูลต้นทุนจากการผลิตก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="39924-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="39924-137">ข้อมูลงบประมาณและการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="39924-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="39924-138">การประเมินขนาดการผลิตที่ต้องใช้ในการรักษาต้นทุนเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="39924-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>




