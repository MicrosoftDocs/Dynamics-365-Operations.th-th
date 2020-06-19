---
title: ระดับการคำนวณต้นทุน
description: หัวข้อนี้อธิบายระดับของรายการวัสดุและส่วนประกอบ (BOM) ที่มีการตั้งชื่อว่าระดับการคำนวณต้นทุน ระดับ BOM นี้ไม่รวมใบสั่งผลิตและใบสั่งชุดในการคำนวณ
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410987"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="7d837-104">ระดับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7d837-104">Cost calculation level</span></span>

<span data-ttu-id="7d837-105">ระดับของรายการวัสดุและส่วนประกอบ (BOM) ที่ตั้งชื่อเป็น **ระดับการคำนวณต้นทุน** ไม่รวมใบสั่งผลิตและใบสั่งชุดงานในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="7d837-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="7d837-106">ระบบจะใช้ระดับนี้ เมื่อเรียกใช้การคำนวณต้นทุนในเวอร์ชันการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7d837-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="7d837-107">ในกระบวนการ เช่น การคำนวณใหม่ และการปิดบัญชีสินค้าคงคลัง ระบบจะใช้ BOM ระดับ **ระดับการคิดต้นทุน** แทน</span><span class="sxs-lookup"><span data-stu-id="7d837-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="7d837-108">สถานการณ์จำลองอย่างง่ายต่อไปนี้แสดงความแตกต่างระหว่าง BOM ระดับ **ระดับการคำนวณต้นทุน** และ BOM ระดับ **ระดับการคิดต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="7d837-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="7d837-109">คุณมีผลิตภัณฑ์สามผลิตภัณฑ์ได้แก่ A B และ C ผลิตภัณฑ์ C เป็นส่วนประกอบของผลิตภัณฑ์ B และผลิตภัณฑ์ B เป็นส่วนประกอบของผลิตภัณฑ์ A</span><span class="sxs-lookup"><span data-stu-id="7d837-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="7d837-110">**ระดับการคิดต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7d837-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="7d837-111">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="7d837-111">**Product A:** 0</span></span>
    - <span data-ttu-id="7d837-112">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="7d837-112">**Product B:** 1</span></span>
    - <span data-ttu-id="7d837-113">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="7d837-113">**Product C:** 2</span></span>

- <span data-ttu-id="7d837-114">**ระดับการคำนวณต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7d837-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="7d837-115">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="7d837-115">**Product A:** 0</span></span>
    - <span data-ttu-id="7d837-116">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="7d837-116">**Product B:** 1</span></span>
    - <span data-ttu-id="7d837-117">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="7d837-117">**Product C:** 2</span></span>

<span data-ttu-id="7d837-118">ใบสั่งผลิตสำหรับผลิตภัณฑ์ C จะถูกสร้าง และมีการเพิ่มผลิตภัณฑ์ A ที่ BOM ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="7d837-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="7d837-119">หลังจากที่มีการประเมินใบสั่งแล้ว ระดับ BOM จะมีการอัพเดตในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7d837-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="7d837-120">**ระดับการคิดต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7d837-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="7d837-121">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="7d837-121">**Product B:** 1</span></span>
    - <span data-ttu-id="7d837-122">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="7d837-122">**Product C:** 2</span></span>
    - <span data-ttu-id="7d837-123">**ผลิตภัณฑ์ A:** 3</span><span class="sxs-lookup"><span data-stu-id="7d837-123">**Product A:** 3</span></span>

- <span data-ttu-id="7d837-124">**ระดับการคำนวณต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7d837-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="7d837-125">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="7d837-125">**Product A:** 0</span></span>
    - <span data-ttu-id="7d837-126">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="7d837-126">**Product B:** 1</span></span>
    - <span data-ttu-id="7d837-127">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="7d837-127">**Product C:** 2</span></span>

<span data-ttu-id="7d837-128">ลักษณะการทำงานนี้ช่วยให้มั่นใจว่าการเปลี่ยนแปลงใน BOM ของใบสั่งผลิตจะไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7d837-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
