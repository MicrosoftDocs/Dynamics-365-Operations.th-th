---
title: อัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมการผลิต
description: บทความนี้ให้คำแนะนำเกี่ยวกับวิธีการอัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมการผลิต
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea810daab0ecdee59aba703f38d0001e2965f936
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214170"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="decc4-103">อัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="decc4-103">Update standard costs in a manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="decc4-104">บทความนี้ให้คำแนะนำเกี่ยวกับวิธีการอัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="decc4-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="decc4-105">การอัพเดตสามารถสะท้อนสินค้าใหม่ ประเภทต้นทุน หรือสูตรการคำนวณต้นทุนทางอ้อมได้</span><span class="sxs-lookup"><span data-stu-id="decc4-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="decc4-106"> ทั้งยังสามารถสะท้อนถึงการแก้ไขและต้นทุนการเปลี่ยนแปลงอีกด้วย </span><span class="sxs-lookup"><span data-stu-id="decc4-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="decc4-107">ชนิดของการอัพเดตมีผลต่อขั้นตอนที่คุณต้องทำให้เสร็จสมบูรณ์ เพื่ออัพเดตต้นทุนมาตรฐาน ดังที่แสดงในกรณีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="decc4-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="decc4-108">ป้อนการเปลี่ยนแปลงต้นทุนมาตรฐานที่คาดหวังไว้สำหรับสินค้าที่ซื้อ และจากนั้นเปลี่ยนสถานะของเรกคอร์ดต้นทุนสินค้าเป็น **ใช้งาน** ในวันที่ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="decc4-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="decc4-109">อย่างไรก็ตาม ไม่ต้องคำนวณต้นทุนของสินค้าที่ผลิตซึ่งใช้สินค้าที่ซื้ออีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="decc4-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="decc4-110">ป้อนต้นทุนมาตรฐานสำหรับสินค้าที่ซื้อใหม่ แต่ไม่ต้องคำนวณต้นทุนสินค้าที่ผลิตใหม่ที่มีเวอร์ชันสูตรการผลิต (BOM) ที่มีสินค้าที่ซื้อเป็นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="decc4-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="decc4-111">แก้ไขหรือเปลี่ยนแปลงต้นทุนของสินค้าที่ซื้อ หรือเปลี่ยนแปลงกลุ่มต้นทุนที่ได้รับมอบหมายให้กับสินค้าที่ซื้อ และคำนวณต้นทุนสำหรับสินค้าที่ผลิตทั้งหมดที่มีเวอร์ชัน BOM ที่มีสินค้าที่ซื้อเป็นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="decc4-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="decc4-112">เปลี่ยนแปลงต้นทุนสำหรับประเภทต้นทุน และคำนวณต้นทุนสำหรับสินค้าที่ผลิตทั้งหมด ที่มีเวอร์ชันกระบวนการผลิตซึ่งมีการดำเนินการสายงานการผลิตที่ใช้ประเภทต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="decc4-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="decc4-113">เปลี่ยนแปลงประเภทต้นทุนที่ถูกกำหนดให้กับการดำเนินการสายงานการผลิต หรือกลุ่มต้นทุนที่ถูกกำหนดให้กับประเภทต้นทุน </span><span class="sxs-lookup"><span data-stu-id="decc4-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="decc4-114">และจากนั้น คำนวณต้นทุนสำหรับสินค้าที่ผลิตทั้งหมดที่มีเวอร์ชันกระบวนการผลิตซึ่งมีการดำเนินการสายงานการผลิตที่ใช้ประเภทต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="decc4-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="decc4-115">เปลี่ยนแปลงสูตรการคำนวณต้นทุนทางอ้อม และคำนวณต้นทุนสำหรับสินค้าที่ผลิตทั้งหมดที่ได้รับผลกระทบจากการเปลี่ยนแปลงนี้</span><span class="sxs-lookup"><span data-stu-id="decc4-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="decc4-116">เปลี่ยนแปลงหรือเพิ่มไซต์การผลิตสำหรับสินค้าที่ผลิต และคำนวณต้นทุนการผลิตของสินค้าสำหรับไซต์นี้</span><span class="sxs-lookup"><span data-stu-id="decc4-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="decc4-117">คำนวณ หรือคำนวณใหม่ ต้นทุนสำหรับสินค้าที่ผลิต และคำนวณต้นทุนสำหรับสินค้าที่ผลิตทั้งหมดอีกครั้งที่มีเวอร์ชัน BOM ซึ่งมีสินค้าที่ผลิตเป็นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="decc4-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="decc4-118">คำนวณต้นทุนสำหรับสินค้าที่ผลิตใหม่ ตาม BOM ซึ่งได้รับการกำหนด อนุมัติ และใช้งานอยู่ และข้อมูลกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="decc4-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="decc4-119">แต่ละกรณีต้องได้รับการพิจารณาอย่างถี่ถ้วนเกี่ยวกับวิธีอัพเดตต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="decc4-119">Each case requires careful consideration about how to update standard costs.</span></span>



