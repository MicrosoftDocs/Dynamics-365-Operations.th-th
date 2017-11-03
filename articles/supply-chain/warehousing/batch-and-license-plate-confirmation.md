---
title: "การยืนยันชุดงานและป้ายทะเบียน"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าและใช้การยืนยันชุดงานและป้ายทะเบียนจากอุปกรณ์เคลื่อนที่"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0444caa0f1cc176153c322b8619db65bd377ddd0
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="2c99d-103">การยืนยันชุดงานและป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="2c99d-103">Batch and license plate confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2c99d-104">การยืนยันชุดงานช่วยให้คุณสามารถยืนยันว่ามีการเบิกชุดงานที่ถูกต้องจากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2c99d-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="2c99d-105">ในการเบิกสินค้าเริ่มต้นของงานสำหรับชุดงานที่อยู่เหนือสินค้าเท่านั้น โดยที่ ชุดงานข้างต้น บ่งชี้ว่า ชุดงานมีช่วงที่สูงกว่าที่ตั้งในลำดับชั้นการค้นหา คุณต้องตรวจสอบว่าชุดงานที่มีการเบิกสินค้าตรงกับชุดงานในรายการงาน</span><span class="sxs-lookup"><span data-stu-id="2c99d-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="2c99d-106">การยืนยันป้ายทะเบียนช่วยให้คุณสามารถยืนยันว่ามีการเบิกป้ายทะเบียนที่ถูกต้องจากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2c99d-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="2c99d-107">เมื่อมีการเบิกสินค้าของงานจากที่ตั้งระยะ คุณต้องตรวจสอบว่าป้ายทะเบียนที่มีการเบิกสินค้าตรงกับป้ายทะเบียนที่เชื่อมโยงกับงาน</span><span class="sxs-lookup"><span data-stu-id="2c99d-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="2c99d-108">ถ้างานเริ่มต้นด้วยการสแกนป้ายทะเบียน ขั้นตอนการยืนยันนี้จะถูกข้ามไป</span><span class="sxs-lookup"><span data-stu-id="2c99d-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="2c99d-109">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="2c99d-109">Where it applies</span></span>
<span data-ttu-id="2c99d-110">การยืนยันใช้ในสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c99d-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="2c99d-111">การยืนยันชุดงานใช้กับการเบิกสินค้าเริ่มต้นของงานสำหรับชุดงานที่อยู่เหนือสินค้า</span><span class="sxs-lookup"><span data-stu-id="2c99d-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="2c99d-112">การยืนยันป้ายทะเบียนใช้กับการเบิกสินค้าจากที่ตั้งระยะ</span><span class="sxs-lookup"><span data-stu-id="2c99d-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="2c99d-113">ตั้งค่าการยืนยันชุดงานและป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="2c99d-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="2c99d-114">คุณสามารถตั้งค่าคอนฟิกการยืนยันชุดงานและป้ายทะเบียนจากรายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2c99d-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="2c99d-115">จากรายการเมนูบนอุปกรณ์เคลื่อนที่ ป้อนการตั้งค่าการยืนยันงาน</span><span class="sxs-lookup"><span data-stu-id="2c99d-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="2c99d-116">เลือกตัวเลือกสำหรับการยืนยันชุดงานหรือป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="2c99d-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="2c99d-117">ตัวเลือกทั้งสองจะพร้อมใช้งานสำหรับการเบิกสินค้าของชนิดงานที่ไม่มีการเปิดใช้งานการยืนยันอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2c99d-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

