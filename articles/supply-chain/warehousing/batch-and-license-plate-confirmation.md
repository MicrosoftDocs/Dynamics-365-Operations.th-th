---
title: การยืนยันชุดงานและป้ายทะเบียน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและใช้การยืนยันชุดงานและป้ายทะเบียนจากอุปกรณ์เคลื่อนที่
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c588e6ed11d275b75133e2824f3d385048050426
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837548"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="07601-103">การยืนยันชุดงานและป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="07601-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07601-104">การยืนยันชุดงานช่วยให้คุณสามารถยืนยันว่ามีการเบิกชุดงานที่ถูกต้องจากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="07601-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="07601-105">ในการเบิกสินค้าเริ่มต้นของงานสำหรับสินค้า *ชุดงานที่อยู่เหนือ\[ที่ตั้ง\]* เท่านั้น โดยที่ ชุดงานข้างต้น บ่งชี้ว่า ชุดงานมีช่วงที่สูงกว่าที่ตั้งในลำดับชั้นการค้นหา คุณต้องตรวจสอบว่าชุดงานที่มีการเบิกสินค้าตรงกับชุดงานในรายการงาน</span><span class="sxs-lookup"><span data-stu-id="07601-105">On the initial pick of work for *Batch-above\[location\]* items only, where batch-above indicates that batch is placed higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="07601-106">การยืนยันป้ายทะเบียนช่วยให้คุณสามารถยืนยันว่ามีการเบิกป้ายทะเบียนที่ถูกต้องจากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="07601-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="07601-107">เมื่อมีการเบิกสินค้าของงานจากที่ตั้งระยะ คุณต้องตรวจสอบว่าป้ายทะเบียนที่มีการเบิกสินค้าตรงกับป้ายทะเบียนที่เชื่อมโยงกับงาน</span><span class="sxs-lookup"><span data-stu-id="07601-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="07601-108">ถ้างานเริ่มต้นด้วยการสแกนป้ายทะเบียน ขั้นตอนการยืนยันนี้จะถูกข้ามไป</span><span class="sxs-lookup"><span data-stu-id="07601-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="07601-109">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="07601-109">Where it applies</span></span>

<span data-ttu-id="07601-110">การยืนยันใช้ในสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="07601-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="07601-111">การยืนยันชุดงานใช้กับการเบิกสินค้าเริ่มต้นของงานสำหรับชุดงานที่อยู่เหนือสินค้า</span><span class="sxs-lookup"><span data-stu-id="07601-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="07601-112">การยืนยันป้ายทะเบียนใช้กับการเบิกสินค้าจากที่ตั้งระยะ</span><span class="sxs-lookup"><span data-stu-id="07601-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07601-113">การเติมสินค้าไม่ได้รับการสนับสนุนสำหรับการยืนยันป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="07601-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="07601-114">เมื่อดำเนินงานการเติมสินค้า จะไม่มีการสร้างขั้นตอนการยืนยันป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="07601-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="07601-115">ตั้งค่าการยืนยันชุดงานและป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="07601-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="07601-116">คุณสามารถตั้งค่าคอนฟิกการยืนยันชุดงานและป้ายทะเบียนจากรายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="07601-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="07601-117">จากรายการเมนูบนอุปกรณ์เคลื่อนที่ ป้อนการตั้งค่าการยืนยันงาน</span><span class="sxs-lookup"><span data-stu-id="07601-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="07601-118">เลือกตัวเลือกสำหรับการยืนยันชุดงานหรือป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="07601-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="07601-119">ตัวเลือกทั้งสองจะพร้อมใช้งานสำหรับการเบิกสินค้าของชนิดงานที่ไม่มีการเปิดใช้งานการยืนยันอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="07601-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
