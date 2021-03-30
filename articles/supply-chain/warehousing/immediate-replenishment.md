---
title: การเติมสินค้าทันที
description: หัวข้อนี้อธิบายวิธีการที่คุณสามารถใช้การเติมสินค้าในทันที เพื่อเติมสินค้าในสินค้าคงคลังเมื่อคำสั่งสถานที่ล้มเหลวในการปันส่วนสินค้าคงคลัง
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 3def95ac272a424591ed4382d5cd5841bc663654
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235399"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="beeef-103">การเติมสินค้าทันที</span><span class="sxs-lookup"><span data-stu-id="beeef-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="beeef-104">การเติมสินค้าในทันทีช่วยให้คุณสามารถเติมสินค้าในสินค้าคงคลังได้โดยทันที หลังจากรายการคำสั่งสถานที่ล้มเหลวในการปันส่วนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="beeef-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="beeef-105">การเพิ่มเติมสินค้าเป็นไปตามรายการเดียวในการตั้งค่าคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="beeef-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="beeef-106">ถ้าสินค้าคงคลังไม่ใช่คงคลังคงเหลือในหน่วยการวัดที่ระบุโดยรายการนั้น การเพิ่มเติมสินค้าของหน่วยวัดจะเกิดขึ้นโดยทันที</span><span class="sxs-lookup"><span data-stu-id="beeef-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="beeef-107">การเติมสินค้าในทันทีให้รายการสำรองกับวิธีที่ซึ่งการปันส่วนของสินค้าคงคลังเป็นไปตามรายการเพิ่มเติมในคำสั่งสถานที่ และที่ซึ่งความต้องการจะถูกรวมเข้าด้วยกันที่จุดสิ้นสุดการปันส่วน และถูกเติมสินค้าในหน่วยวัดที่ระบุโดยรายการสุดท้ายในคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="beeef-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="beeef-108">ประโยชน์ของการใช้การเติมสินค้าในทันทีคือ สามารถจำกัดการเพิ่มเติมสินค้าตามหน่วยเฉพาะ และปริมาณสามารถเชื่อมโยงไปยังสถานที่เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="beeef-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="beeef-109">สถานการณ์จำลองทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="beeef-109">Business scenario</span></span>

<span data-ttu-id="beeef-110">ตัวอย่างเช่น คุณมีคลังสินค้าที่มีพื้นที่เบิกสินค้าแยกต่างหากสำหรับ "กล่อง" และ "แต่ละ" หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="beeef-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="beeef-111">คุณต้องการปรับกระบวนการเบิกสินค้าให้เหมาะสมโดยการเบิกสินค้าให้กล่องมากที่สุดที่เป็นไปได้ และจากนั้นเบิกสินค้าปริมาณคงเหลือใดๆ ที่น้อยกว่ากล่องจาก "แต่ละ" พื้นที่</span><span class="sxs-lookup"><span data-stu-id="beeef-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="beeef-112">ในกรณีนี้ คุณสามารถใช้การเติมสินค้าในทันทีได้</span><span class="sxs-lookup"><span data-stu-id="beeef-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="beeef-113">ในคำสั่งสถานที่ คุณสามารถตั้งค่าการเติมสินค้าในทันทีสำหรับกล่องได้ เพื่อให้มีการใช้การเพิ่มเติมสินค้าตามความต้องการทันทีที่มีการขาดแคลนกล่องที่สามารถเบิกสินค้าได้สำหรับปริมาณตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="beeef-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="beeef-114">ด้วยวิธีนี้ คุณปรับกระบวนการเบิกสินค้าให้เกิดประสิทธิภาพสูงสุด เพื่อให้การเบิกสินค้ามีกล่องมากที่สุดที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="beeef-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="beeef-115">การเติมสินค้าในทันทีจะสร้างการเติมสินค้าของกล่อง และความต้องการจะไม่สามารถส่งผ่านได้ เพื่อให้ปริมาณถูกเบิกใน "แต่ละ" หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="beeef-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="beeef-116">กล่าวคือ เฉพาะปริมาณที่ควรถูกเบิกใน "แต่ละ" หน่วยวัด (นั่นคือ ปริมาณที่น้อยกว่ากล่อง) จะถูกเลือกจาก "แต่ละ" พื้นที่</span><span class="sxs-lookup"><span data-stu-id="beeef-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="beeef-117">หากมีการขาดแคลนในพื้นที่ "กล่อง" คุณสามารถเลือกกล่องมากที่สุดที่เป็นไปได้ออกจากความต้องการรวม</span><span class="sxs-lookup"><span data-stu-id="beeef-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="beeef-118">จากนั้น ปริมาณคงเหลือจะถูกเลือกจาก "แต่ละ" พื้นที่</span><span class="sxs-lookup"><span data-stu-id="beeef-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="beeef-119">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="beeef-119">Where it applies</span></span>

<span data-ttu-id="beeef-120">การเติมสินค้าในทันทีถูกใช้ระหว่างการดำเนินการเวฟ หากการปันส่วนล้มเหลวสำหรับรายการคำสั่งสถานที่ที่การตั้งค่ามีเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="beeef-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="beeef-121">ตั้งค่าการเติมสินค้าในทันที</span><span class="sxs-lookup"><span data-stu-id="beeef-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="beeef-122">ไปยัง **การบริหารคลังสินค้า** \> **การตั้งค่า** \> **คำสั่งสถานที่** และจากนั้น บนแท็บ **รายการ** ในรายการ **เท็มเพลตการเพิ่มเติมสินค้าในทันที** เลือกเท็มเพลตการเพิ่มเติมสำหรับความต้องการเวฟ</span><span class="sxs-lookup"><span data-stu-id="beeef-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="beeef-123">มีการใช้เท็มเพลตการเติมสินค้า หากรายการคำสั่งสถานที่ล้มเหลวในการปันส่วนหน่วยวัดที่จัดสรรไว้</span><span class="sxs-lookup"><span data-stu-id="beeef-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="beeef-124">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="beeef-124">Troubleshooting</span></span>

<span data-ttu-id="beeef-125">ถ้ามีการเลือกการเติมสินค้าในทันทีสำหรับรายการคำสั่งสถานที่ แต่ไม่มีสร้างงานการเพิ่มเติมสินค้า เมื่อคุณใช้เท็มเพลตการเติมสินค้าความต้องการสำหรับรายการคำสั่งของสถานที่นั้น ต้องมีการตรวจสอบสองสาเหตุหลัก:</span><span class="sxs-lookup"><span data-stu-id="beeef-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="beeef-126">ให้แน่ใจว่า เท็มเพลตการเติมสินค้าตามความต้องการที่จะใช้ ถูกตั้งค่าเพื่อใช้เท็มเพลตสถานที่ที่ถูกต้อง และเท็มเพลตของงานของชนิด **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="beeef-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="beeef-127">ตรวจสอบให้แน่ใจว่า มีปริมาณคงคลังคงเหลือเพียงพอที่สถานที่ที่เท็มเพลตการเติมสินค้าความต้องการค้นหาสินค้าคงคลังคงเหลือสำหรับการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="beeef-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]