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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438394"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="c6b67-104">ระดับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6b67-104">Cost calculation level</span></span>

<span data-ttu-id="c6b67-105">ระดับของรายการวัสดุและส่วนประกอบ (BOM) ที่ตั้งชื่อเป็น **ระดับการคำนวณต้นทุน** ไม่รวมใบสั่งผลิตและใบสั่งชุดงานในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="c6b67-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="c6b67-106">ระบบจะใช้ระดับนี้ เมื่อเรียกใช้การคำนวณต้นทุนในเวอร์ชันการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6b67-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="c6b67-107">ในกระบวนการ เช่น การคำนวณใหม่ และการปิดบัญชีสินค้าคงคลัง ระบบจะใช้ BOM ระดับ **ระดับการคิดต้นทุน** แทน</span><span class="sxs-lookup"><span data-stu-id="c6b67-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="c6b67-108">สถานการณ์จำลองอย่างง่ายต่อไปนี้แสดงความแตกต่างระหว่าง BOM ระดับ **ระดับการคำนวณต้นทุน** และ BOM ระดับ **ระดับการคิดต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="c6b67-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="c6b67-109">คุณมีผลิตภัณฑ์สามผลิตภัณฑ์ได้แก่ A B และ C ผลิตภัณฑ์ C เป็นส่วนประกอบของผลิตภัณฑ์ B และผลิตภัณฑ์ B เป็นส่วนประกอบของผลิตภัณฑ์ A</span><span class="sxs-lookup"><span data-stu-id="c6b67-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="c6b67-110">**ระดับการคิดต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6b67-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="c6b67-111">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="c6b67-111">**Product A:** 0</span></span>
    - <span data-ttu-id="c6b67-112">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="c6b67-112">**Product B:** 1</span></span>
    - <span data-ttu-id="c6b67-113">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="c6b67-113">**Product C:** 2</span></span>

- <span data-ttu-id="c6b67-114">**ระดับการคำนวณต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6b67-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="c6b67-115">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="c6b67-115">**Product A:** 0</span></span>
    - <span data-ttu-id="c6b67-116">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="c6b67-116">**Product B:** 1</span></span>
    - <span data-ttu-id="c6b67-117">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="c6b67-117">**Product C:** 2</span></span>

<span data-ttu-id="c6b67-118">ใบสั่งผลิตสำหรับผลิตภัณฑ์ C จะถูกสร้าง และมีการเพิ่มผลิตภัณฑ์ A ที่ BOM ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="c6b67-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="c6b67-119">หลังจากที่มีการประเมินใบสั่งแล้ว ระดับ BOM จะมีการอัพเดตในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6b67-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="c6b67-120">**ระดับการคิดต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6b67-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="c6b67-121">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="c6b67-121">**Product B:** 1</span></span>
    - <span data-ttu-id="c6b67-122">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="c6b67-122">**Product C:** 2</span></span>
    - <span data-ttu-id="c6b67-123">**ผลิตภัณฑ์ A:** 3</span><span class="sxs-lookup"><span data-stu-id="c6b67-123">**Product A:** 3</span></span>

- <span data-ttu-id="c6b67-124">**ระดับการคำนวณต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6b67-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="c6b67-125">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="c6b67-125">**Product A:** 0</span></span>
    - <span data-ttu-id="c6b67-126">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="c6b67-126">**Product B:** 1</span></span>
    - <span data-ttu-id="c6b67-127">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="c6b67-127">**Product C:** 2</span></span>

<span data-ttu-id="c6b67-128">ลักษณะการทำงานนี้ช่วยให้มั่นใจว่าการเปลี่ยนแปลงใน BOM ของใบสั่งผลิตจะไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6b67-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
