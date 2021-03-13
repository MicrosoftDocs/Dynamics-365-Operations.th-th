---
title: แหล่งที่มาทั่วไปของผลต่างการผลิต
description: บทความนี้อธิบายถึงแหล่งที่มาทั่วไปต่างๆของผลต่างการผลิตแต่ละชนิด
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55d108ff71f0af773fa521833d57ce96d36251fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008252"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="871b7-103">แหล่งที่มาทั่วไปของผลต่างการผลิต</span><span class="sxs-lookup"><span data-stu-id="871b7-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="871b7-104">บทความนี้อธิบายถึงแหล่งที่มาทั่วไปต่างๆของผลต่างการผลิตแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="871b7-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="871b7-105">นี่่เป็นแหล่งที่มาทั่วไปบางแห่งของผลต่างของ **ขนาดล็อต**:</span><span class="sxs-lookup"><span data-stu-id="871b7-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="871b7-106">ปริมาณสินค้าสำหรับใบสั่งผลิตจะแตกต่างจากปริมาณการคำนวณที่ใช้ในการคำนวณต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="871b7-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="871b7-107">ปริมาณจะให้ข้อมูลพื้นฐานสำหรับการตัดจำหน่ายต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="871b7-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="871b7-108">มูลค่าต้นทุนคงที่ในใบสั่งผลิตแตกต่างจากต้นทุนคงที่ใช้ในการคำนวณต้นทุนมาตรฐาน </span><span class="sxs-lookup"><span data-stu-id="871b7-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="871b7-109">ต้นทุนคงที่ในใบสั่งผลิตอาจแตกต่างด้วยเหตุผลหลายประการ </span><span class="sxs-lookup"><span data-stu-id="871b7-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="871b7-110">ตัวอย่างเช่น ต้นทุนคงอาจสะท้อนถึงปัจจัยต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="871b7-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="871b7-111">การเปลี่ยนแปลงด้วยตนเองไปยังสูตรการผลิต (BOM) หรือกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="871b7-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="871b7-112">การเลือกของเวอร์ชัน BOM หรือเวอร์ชันกระบวนการผลิตต่างๆ เมื่อคุณสร้างใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="871b7-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="871b7-113">การเปลี่ยนแปลงทางวิศวกรรมที่วางแผนไว้ไปยังเวอร์ชัน BOM หรือเวอร์ชันกระบวนการผลิต ที่กำหนดให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="871b7-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="871b7-114">นี่่เป็นแหล่งที่มาทั่วไปบางแห่งของผลต่างของ **ราคาการผลิต**:</span><span class="sxs-lookup"><span data-stu-id="871b7-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="871b7-115">ประเภทต้นทุน (และราคาประเภทต้นทุน) สำหรับการใช้ที่มีการรายงานของกระบวนการการดำเนินการผลิต จะแตกต่างจากประเภทต้นทุนที่ใช้ในการคำนวณต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="871b7-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="871b7-116">ต้นทุนที่ใช้งานอยู่สำหรับราคาประเภทต้นทุนจะแตกต่างจากราคาประเภทต้นทุนที่ใช้ในการคำนวณต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="871b7-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="871b7-117">นี่่เป็นแหล่งที่มาทั่วไปบางแห่งของผลต่างของ **ปริมาณการผลิต**:</span><span class="sxs-lookup"><span data-stu-id="871b7-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="871b7-118">คุณตัดส่วนประกอบวัสดุที่มากเกินไป หรือตัดส่วนประกอบวัสดุที่น้อยเกินไป</span><span class="sxs-lookup"><span data-stu-id="871b7-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="871b7-119">คุณรายงานการดำเนินกระบวนการผลิตที่มากเกินไป หรือรายงานการดำเนินกระบวนการผลิตที่น้อยเกินไป</span><span class="sxs-lookup"><span data-stu-id="871b7-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="871b7-120">คุณได้รับปริมาณสินค้าที่มากเกินไป หรือได้รับปริมาณสินค้าที่น้อยเกินไปของสินค้าหลักซึ่งสัมพันธ์กับปริมาณการสั่ง </span><span class="sxs-lookup"><span data-stu-id="871b7-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="871b7-121">อย่างไรก็ตาม คุณตัดส่วนประกอบออกและรายงานการดำเนินงานทั้งหมด ซึ่งจะเป็นไปตามปริมาณการสั่งสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="871b7-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="871b7-122">นี่่เป็นแหล่งที่มาทั่วไปบางแห่งของผลต่างของ **การแทนที่การผลิต**:</span><span class="sxs-lookup"><span data-stu-id="871b7-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="871b7-123">คุณตัดส่วนประกอบวัสดุที่ไม่ได้อยู่ใน BOM การผลิต</span><span class="sxs-lookup"><span data-stu-id="871b7-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="871b7-124">คุณเพิ่มส่วนประกอบเข้าใน BOM การผลิตด้วยตนเอง และรายงานการใช้ส่วนประกอบนั้น</span><span class="sxs-lookup"><span data-stu-id="871b7-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="871b7-125">คุณรายงานการใช้สินค้า แต่ไม่เพิ่มลงใน BOM การผลิตด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="871b7-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="871b7-126">คุณเพิ่มการดำเนินงานลงในกระบวนการผลิตด้วยตนเอง และรายงานการใช้การดำเนินงานนั้น</span><span class="sxs-lookup"><span data-stu-id="871b7-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="871b7-127">เมื่อคุณสร้างใบสั่งผลิต คุณเลือกเวอร์ชัน BOM ซึ่งแตกต่างจากเวอร์ชัน BOM ที่ใช้ในการคำนวณต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="871b7-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="871b7-128">เมื่อคุณสร้างใบสั่งผลิต คุณเลือกเวอร์ชันกระบวนการผลิตที่แตกต่างจากเวอร์ชันกระบวนการผลิตที่ใช้ในการคำนวณต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="871b7-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>




