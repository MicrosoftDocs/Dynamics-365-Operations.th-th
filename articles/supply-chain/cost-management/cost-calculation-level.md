---
title: ระดับการคำนวณต้นทุน
description: หัวข้อนี้อธิบายระดับของรายการวัสดุและส่วนประกอบ (BOM) ที่มีการตั้งชื่อว่าระดับการคำนวณต้นทุน ระดับ BOM นี้ไม่รวมใบสั่งผลิตและใบสั่งชุดในการคำนวณ
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839498"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="9cd23-104">ระดับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cd23-104">Cost calculation level</span></span>

<span data-ttu-id="9cd23-105">ระดับของรายการวัสดุและส่วนประกอบ (BOM) ที่ตั้งชื่อเป็น **ระดับการคำนวณต้นทุน** ไม่รวมใบสั่งผลิตและใบสั่งชุดงานในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="9cd23-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="9cd23-106">ระบบจะใช้ระดับนี้ เมื่อเรียกใช้การคำนวณต้นทุนในเวอร์ชันการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cd23-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="9cd23-107">ในกระบวนการ เช่น การคำนวณใหม่ และการปิดบัญชีสินค้าคงคลัง ระบบจะใช้ BOM ระดับ **ระดับการคิดต้นทุน** แทน</span><span class="sxs-lookup"><span data-stu-id="9cd23-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="9cd23-108">สถานการณ์จำลองอย่างง่ายต่อไปนี้แสดงความแตกต่างระหว่าง BOM ระดับ **ระดับการคำนวณต้นทุน** และ BOM ระดับ **ระดับการคิดต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="9cd23-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="9cd23-109">คุณมีผลิตภัณฑ์สามผลิตภัณฑ์ได้แก่ A B และ C ผลิตภัณฑ์ C เป็นส่วนประกอบของผลิตภัณฑ์ B และผลิตภัณฑ์ B เป็นส่วนประกอบของผลิตภัณฑ์ A</span><span class="sxs-lookup"><span data-stu-id="9cd23-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="9cd23-110">**ระดับการคิดต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd23-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="9cd23-111">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="9cd23-111">**Product A:** 0</span></span>
    - <span data-ttu-id="9cd23-112">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="9cd23-112">**Product B:** 1</span></span>
    - <span data-ttu-id="9cd23-113">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="9cd23-113">**Product C:** 2</span></span>

- <span data-ttu-id="9cd23-114">**ระดับการคำนวณต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd23-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="9cd23-115">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="9cd23-115">**Product A:** 0</span></span>
    - <span data-ttu-id="9cd23-116">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="9cd23-116">**Product B:** 1</span></span>
    - <span data-ttu-id="9cd23-117">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="9cd23-117">**Product C:** 2</span></span>

<span data-ttu-id="9cd23-118">ใบสั่งผลิตสำหรับผลิตภัณฑ์ C จะถูกสร้าง และมีการเพิ่มผลิตภัณฑ์ A ที่ BOM ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9cd23-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="9cd23-119">หลังจากที่มีการประเมินใบสั่งแล้ว ระดับ BOM จะมีการอัพเดตในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd23-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="9cd23-120">**ระดับการคิดต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd23-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="9cd23-121">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="9cd23-121">**Product B:** 1</span></span>
    - <span data-ttu-id="9cd23-122">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="9cd23-122">**Product C:** 2</span></span>
    - <span data-ttu-id="9cd23-123">**ผลิตภัณฑ์ A:** 3</span><span class="sxs-lookup"><span data-stu-id="9cd23-123">**Product A:** 3</span></span>

- <span data-ttu-id="9cd23-124">**ระดับการคำนวณต้นทุน** กำหนดระดับ BOM ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd23-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="9cd23-125">**ผลิตภัณฑ์ A:** 0</span><span class="sxs-lookup"><span data-stu-id="9cd23-125">**Product A:** 0</span></span>
    - <span data-ttu-id="9cd23-126">**ผลิตภัณฑ์ B:** 1</span><span class="sxs-lookup"><span data-stu-id="9cd23-126">**Product B:** 1</span></span>
    - <span data-ttu-id="9cd23-127">**ผลิตภัณฑ์ C:** 2</span><span class="sxs-lookup"><span data-stu-id="9cd23-127">**Product C:** 2</span></span>

<span data-ttu-id="9cd23-128">ลักษณะการทำงานนี้ช่วยให้มั่นใจว่าการเปลี่ยนแปลงใน BOM ของใบสั่งผลิตจะไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cd23-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]