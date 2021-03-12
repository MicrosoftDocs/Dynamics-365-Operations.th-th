---
title: การเตรียมการรักษาต้นทุนมาตรฐานสำหรับสินค้าที่ผลิต
description: หัวข้อนี้อธิบายขั้นตอนสำหรับการเตรียมการในการรักษาต้นทุนสำหรับสินค้าที่ผลิต
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b35e424c582c173e3fa1f4d0a335106e413b6660
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967419"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="8b24b-103">การเตรียมการรักษาต้นทุนมาตรฐานสำหรับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="8b24b-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b24b-104">หัวข้อนี้อธิบายขั้นตอนสำหรับการเตรียมการในการรักษาต้นทุนสำหรับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="8b24b-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="8b24b-105">ขั้นตอนสำหรับสินค้าที่ผลิตแตกต่างกันเล็กน้อยจากขั้นตอนสำหรับสินค้าที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="8b24b-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="8b24b-106">นโยบายที่ถูกกำหนดให้กับสินค้าที่ผลิตสามารถส่งผลต่อการคำนวณต้นทุนสำหรับสินค้าหลักที่ผลิตได้</span><span class="sxs-lookup"><span data-stu-id="8b24b-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="8b24b-107">ในการเตรียมการเพื่อรักษาต้นทุนสำหรับสินค้าที่ผลิต ให้ดำเนินการตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8b24b-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="8b24b-108">กำหนดกลุ่มแบบจำลองสินค้าให้กับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="8b24b-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="8b24b-109">กลุ่มแบบจำลองสินค้าระบุว่าจะมีการใช้ต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="8b24b-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="8b24b-110">กำหนดกลุ่มสินค้าให้กับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="8b24b-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="8b24b-111">กลุ่มสินค้ามีบัญชีแยกประเภทที่ใช้งานกับสินค้าที่ผลิต </span><span class="sxs-lookup"><span data-stu-id="8b24b-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="8b24b-112">บัญชีแยกประเภทสำหรับสินค้าที่ผลิตที่มีแบบจำลองสินค้าคงคลังของต้นทุนมาตรฐาน รวมเอาผลต่างการผลิตต่างๆ ผลต่างการเปลี่ยนแปลงต้นทุน และการประเมินค่าต้นทุนสินค้าคงคลังใหม่</span><span class="sxs-lookup"><span data-stu-id="8b24b-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="8b24b-113">กำหนดหน่วยวัดสินค้าคงคลังให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="8b24b-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="8b24b-114">ต้นทุนของสินค้าจะแสดงอยู่ในหน่วยวัดสินค้าคงคลังของสินค้าเสมอ</span><span class="sxs-lookup"><span data-stu-id="8b24b-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="8b24b-115">ไม่ต้องกำหนดกลุ่มต้นทุนให้กับสินค้าที่ผลิต นอกเสียจากว่าจะถือว่าสินค้าเป็นสินค้าที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="8b24b-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="8b24b-116">กำหนดกลุ่มการคำนวณสูตรการผลิต BOM ให้กับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="8b24b-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="8b24b-117">กลุ่มการคำนวณ BOM ของสินค้ากำหนดเงื่อนไขการเตือนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8b24b-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="8b24b-118">ในวิธีนั้น เมื่อทำการคำนวณ BOM เรียบร้อยแล้ว สามารถสร้างข้อความเตือนเกี่ยวกับแหล่งที่มาที่เป็นไปได้ของข้อผิดพลาดในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="8b24b-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="8b24b-119">ตัวอย่างเช่น ข้อความเตือนสามารถแจ้งให้ทราบได้ เมื่อไม่มี BOM หรือกระบวนการผลิตที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="8b24b-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="8b24b-120">กลุ่มการคำนวณ BOM มีนโยบายหยุดการกระจายที่ระบุเวลาที่ควรดำเนินการกับสินค้าที่ผลิตในฐานะสินค้าที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="8b24b-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="8b24b-121">ถ้าสินค้าที่ผลิตเมื่อมีต้นทุนคงที่ ให้มอบหมายปริมาณการสั่งมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="8b24b-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="8b24b-122">ปริมาณการสั่งมาตรฐานเป็นขนาดล็อตบัญชีสำหรับการตัดจำหน่ายต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8b24b-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="8b24b-123">ตัวอย่างของต้นทุนคงที่ประกอบด้วย เวลาในการตั้งค่าในการดำเนินงานกระบวนการผลิตและปริมาณส่วนประกอบคงที่ใน BOM</span><span class="sxs-lookup"><span data-stu-id="8b24b-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="8b24b-124">กำหนด BOM สำหรับสินค้าที่ผลิต </span><span class="sxs-lookup"><span data-stu-id="8b24b-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="8b24b-125">คุณสามารถกำหนดเวอร์ชัน BOM หนึ่งหรือหลายเวอร์ชันให้กับสินค้าที่ผลิตได้ </span><span class="sxs-lookup"><span data-stu-id="8b24b-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="8b24b-126">ตรวจสอบว่าเวอร์ชันที่คุณต้องการได้ถูกทำเครื่องหมายเป็น ผ่านการอนุมัติและใช้งานได้ และตรวจสอบว่ามีวันที่ที่มีผลบังคับใช้ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="8b24b-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="8b24b-127">เวอร์ชัน BOM สามารถเป็น ทั้งบริษัท หรือ เฉพาะไซต์</span><span class="sxs-lookup"><span data-stu-id="8b24b-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="8b24b-128">กำหนดสายงานการผลิตสำหรับสินค้าที่ผลิต </span><span class="sxs-lookup"><span data-stu-id="8b24b-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="8b24b-129">คุณสามารถกำหนดเวอร์ชันสายงานการผลิตหนึ่งหรือหลายเวอร์ชันให้กับสินค้าที่ผลิตได้ </span><span class="sxs-lookup"><span data-stu-id="8b24b-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="8b24b-130">ตรวจสอบว่าเวอร์ชันที่คุณต้องการได้ถูกทำเครื่องหมายเป็น ผ่านการอนุมัติและใช้งานได้ และตรวจสอบว่ามีวันที่ที่มีผลบังคับใช้ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="8b24b-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="8b24b-131">เวอร์ชันกระบวนการผลิตต้องเป็นเฉพาะไซต์</span><span class="sxs-lookup"><span data-stu-id="8b24b-131">The route version must be site-specific.</span></span>

<span data-ttu-id="8b24b-132">ถ้าคุณต้องการใช้ข้อมูลสายงานการผลิตสำหรับวัตถุประสงค์เพื่อการคำนวณต้นทุน จะต้องมีขั้นตอนการเตรียมการเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8b24b-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="8b24b-133">ตัวอย่างเช่น ประเภทต้นทุนที่ถูกกำหนดให้กับการดำเนินการสายงานการผลิตต้องถูกต้องและสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8b24b-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="8b24b-134">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8b24b-134">Related topics</span></span>
--------

[<span data-ttu-id="8b24b-135">การตัดจำหน่ายต้นทุนคงที่สำหรับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="8b24b-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="8b24b-136">ตั้งค่าผลิตภัณฑ์ที่สามารถถูกผลิตหรือจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="8b24b-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)

