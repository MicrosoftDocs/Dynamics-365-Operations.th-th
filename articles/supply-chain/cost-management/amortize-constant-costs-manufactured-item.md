---
title: ตัดจำหน่ายต้นทุนคงที่สำหรับสินค้าที่ผลิต
description: ต้นทุนคงที่ของสินค้าที่ผลิตจะสะท้อนเวลาเซ็ตอัพของการดำเนินการและส่วนประกอบที่มีปริมาณคงที่หรือยอดของเสียแบบคงที่
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 70d2a308f801b1e58585f571355e3a860d99da95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011933"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="39072-103">ตัดจำหน่ายต้นทุนคงที่สำหรับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="39072-103">Amortize constant costs for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39072-104">ต้นทุนคงที่ของสินค้าที่ผลิตจะสะท้อนเวลาเซ็ตอัพของการดำเนินการและส่วนประกอบที่มีปริมาณคงที่หรือยอดของเสียแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="39072-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="39072-105">แนวคิดเกี่ยวกับขนาดล็อตการคำนวณต้นทุนจะใช้ในการตัดจำหน่ายต้นทุนคงที่เหล่านี้ในต้นทุนที่คำนวณของสินค้าที่ผลิต </span><span class="sxs-lookup"><span data-stu-id="39072-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="39072-106">แนวคิดนี้มีคำที่มีความหมายเดียวกันหลายคำ ตัวอย่างหนึ่งเช่น ขนาดล็อตบัญชี</span><span class="sxs-lookup"><span data-stu-id="39072-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="39072-107">และแนวคิดต้นทุนคงที่การตัดจำหน่ายก็คำที่มีความหมายเดียวกันหลายคำด้วยเช่นกัน ตัวอย่างหนึ่งเช่น ต้นทุนคงที่เป็นสัดส่วน</span><span class="sxs-lookup"><span data-stu-id="39072-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="39072-108">ปริมาณขนาดล็อตการคำนวณต้นทุนสำหรับสินค้าที่ผลิตจะใช้ในการคำนวณสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="39072-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="39072-109">ปริมาณจะขึ้นอยู่กับวิธีการที่คุณเริ่มต้นและดำเนินการคำนวณ BOM ดังที่แสดงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="39072-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="39072-110">ปริมาณการคำนวณเริ่มต้นในการคำนวณ BOM ของสินค้า − ปริมาณใบสั่งมาตรฐานของสินค้าสำหรับสินค้าคงคลัง ทำหน้าที่เป็นขนาดล็อตการคำนวณต้นทุน แต่ค่าเริ่มต้นอาจเป็นปริมาณที่มากกว่าเพื่อสะท้อนปริมาณการสั่งของสินค้าจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="39072-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="39072-111">ปริมาณการสั่งมาตรฐานหรือจำนวนมากของสินค้าสามารถกำหนดได้ภายในการตั้งค่าใบสั่งเริ่มต้นของการสั่งได้ หรือการตั้งค่าใบสั่งเฉพาะไซต์</span><span class="sxs-lookup"><span data-stu-id="39072-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="39072-112">ปริมาณการคำนวณที่ระบุในการคำนวณ BOM ของสินค้า − ปริมาณการคำนวณที่ระบุจะทำหน้าที่เป็นขนาดล็อตการคำนวณต้นทุนสำหรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="39072-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="39072-113">ปริมาณการคำนวณเริ่มแรกจะใช้ปริมาณการสั่งมาตรฐานของสินค้า แต่ค่าเริ่มต้นสามารถแทนที่ได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="39072-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="39072-114">ปริมาณการคำนวณที่ระบุจะแสดงถึงขนาดล็อตการคำนวณต้นทุนสำหรับสินค้าที่ระบุ และสำหรับส่วนประกอบที่ผลิตที่มีชนิดบรรทัดรายการ BOM ของการผลิต</span><span class="sxs-lookup"><span data-stu-id="39072-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="39072-115">ทั้งนี้เนื่องจากมีการสมมติว่าส่วนประกอบจะถูกผลิตขึ้นตามปริมาณที่แน่นอน</span><span class="sxs-lookup"><span data-stu-id="39072-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="39072-116">ขนาดล็อตของการคำนวณต้นทุนสำหรับส่วนประกอบที่ผลิตอื่นๆ ที่มีชนิดบรรทัด BOM ของสินค้า จะสะท้อนปริมาณการสั่งมาตรฐานของขนาดล็อตการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39072-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="39072-117">ระบุปริมาณการคำนวณการผลิตตามสั่งในการคำนวณ BOM ของสินค้า − ปริมาณการคำนวณที่ระบุจะทำหน้าที่เป็น ขนาดล็อตการคำนวณต้นทุนสำหรับสินค้าและส่วนประกอบที่ผลิตของสินค้าเมื่อการคำนวณ BOM ใช้โหมดการกระจายการผลิตตามสั่ง </span><span class="sxs-lookup"><span data-stu-id="39072-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="39072-118">โดยจะถือว่าเป็นส่วนประกอบที่ผลิตจะได้รับการผลิตในปริมาณที่แน่นอน เช่นเดียวกับส่วนประกอบที่ผลิตโดยใช้ชนิดบรรทัด BOM ของการผลิต</span><span class="sxs-lookup"><span data-stu-id="39072-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="39072-119">ปริมาณการคำนวณที่ระบุในการคำนวณ BOM เฉพาะใบสั่ง− การคำนวณ BOM เฉพาะใบสั่งสามารถดำเนินกับบรรทัดสินค้าบนใบสั่งขาย ใบเสนอราคาขาย หรือใบสั่งบริการ </span><span class="sxs-lookup"><span data-stu-id="39072-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="39072-120">ปริมาณการคำนวณที่ระบุจะใช้ปริมาณของบรรทัดสินค้าดั้งเดิม แต่ปริมาณเริ่มต้นสามารถแทนที่ได้</span><span class="sxs-lookup"><span data-stu-id="39072-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="39072-121">คุณสามารถเลือกว่าการคำนวณ BOM เฉพาะใบสั่งจะใช้โหมดการกระจายตามสั่งหรือหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="39072-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="39072-122">ยอดเงินที่คำนวณของต้นทุนคงที่ของสินค้าที่ผลิตที่ตัดจำหน่ายจะเรียกว่าค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="39072-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>





