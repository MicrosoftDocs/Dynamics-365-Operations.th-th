---
title: จองชุดงานเดียวกันสำหรับใบสั่งขาย
description: บทความนี้อธิบายวิธีการตั้งค่าผลิตภัณฑ์เพื่ออนุญาตการจองสินค้าคงคลังโดยเทียบกับชุดงานหนึ่งของสินค้าคงคลัง
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e101473c5b6958c7e0fb5c5fa80dccd3d9b467
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216033"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="8e915-103">จองชุดงานเดียวกันสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="8e915-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e915-104">บทความนี้อธิบายวิธีการตั้งค่าผลิตภัณฑ์เพื่ออนุญาตการจองสินค้าคงคลังโดยเทียบกับชุดงานหนึ่งของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e915-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="8e915-105">การจองชุดงานเดียวกันช่วยให้คุณจองสินค้าคงคลังสำหรับบรรทัดใบสั่งขายจากชุดงานหนึ่งของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e915-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="8e915-106">ตัวอย่างเช่น ลูกค้าที่สั่งพื้นหลังสามารถร้องขอให้ใบสั่งทั้งหมดถูกระบุจากชุดงาน หรือล็อตเดียวกัน เพื่อหลีกเลี่ยงความไม่สอดคล้องกันระหว่างการรวบรวม</span><span class="sxs-lookup"><span data-stu-id="8e915-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="8e915-107">เพื่อตั้งค่าผลิตภัณฑ์ให้ใช้การจองชุดงานเดียวกัน การตั้งค่าต่อไปนี้ต้องใช้งานอยู่ในกลุ่มแบบจำลองสินค้า กลุ่มมิติการติดตาม และกลุ่มมิติการจัดเก็บที่คุณกำหนดให้กับผลิตภัณฑ์:</span><span class="sxs-lookup"><span data-stu-id="8e915-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="8e915-108">**กลุ่มแบบจำลองสินค้า** – กลุ่มแบบจำลองสินค้าต้องมีฟิลด์ **การเลือกชุดงานเดียวกัน** และฟิลด์ **รวมความต้องการ** ถูกเลือกในกลุ่มฟิลด์ **การจอง** สำหรับนโยบายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8e915-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="8e915-109">**กลุ่มมิติการติดตาม** – กลุ่มมิติการติดตามต้องมีฟิลด์ **แผนความครอบคลุมตามมิติ** ที่เลือกไว้สำหรับหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="8e915-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="8e915-110">**กลุ่มมิติการจัดเก็บ** – กลุ่มมิติการจัดเก็บต้องมีฟิลด์ **แผนความครอบคลุมตามมิติ** ที่ถูกเลือกสำหรับ **ไซต์** และ **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="8e915-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="8e915-111">เมื่อคุณสำรองสินค้าคงคลังสำหรับผลิตภัณฑ์ในรายการใบสั่งขายที่ถูกตั้งค่าสำหรับการเลือกชุดงานเดียวกัน ระบบพยายามที่จะสำรองปริมาณที่สั่งจากชุดงานสินค้าคงคลังเดียว</span><span class="sxs-lookup"><span data-stu-id="8e915-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="8e915-112">มีข้อกำหนดแอททริบิวต์ของชุดงานเฉพาะใดๆ ถูกพิจารณาด้วย</span><span class="sxs-lookup"><span data-stu-id="8e915-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="8e915-113">ถ้าไม่สามารถป้อนปริมาณจากชุดงานเดียว หน้า **ความขัดแย้งของการจองสินค้าของชุดงานเดียวกัน** จะปรากฏ</span><span class="sxs-lookup"><span data-stu-id="8e915-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="8e915-114">หน้านี้อธิบายถึงปัญหา และการดำเนินการที่คุณมาสามารถดำเนินการจองต่อไป</span><span class="sxs-lookup"><span data-stu-id="8e915-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="8e915-115">เงื่อนไขต่อไปนี้อาจป้องกันชุดงานจากการถูกจอง:</span><span class="sxs-lookup"><span data-stu-id="8e915-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="8e915-116">รหัสการโอนการครอบครองชุดงานที่ **บล็อคการจองสินค้า** สำหรับการขายที่ติดแฟล็กเป็น **ถูกบล็อค**</span><span class="sxs-lookup"><span data-stu-id="8e915-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="8e915-117">ชุดงานที่หมดอายุ ขึ้นอยู่กับวันหมดอายุ และวันที่ขายได้ของลูกค้าที่เกี่ยวข้องใดๆ</span><span class="sxs-lookup"><span data-stu-id="8e915-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="8e915-118">สินค้ายังคงถูกพิจารณาถ้ากลุ่มแบบจำลองสินค้าสำหรับสินค้าถูกควบคุมด้วยที่หมดอายุแรกออกก่อน (FEFO) และถ้าวันที่ควรใช้ก่อนถูกเลือกตามเกณฑ์การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="8e915-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="8e915-119">ชุดงานไม่มีอายุการเก็บที่เหลือเพียงพอ ขึ้นอยู่กับวันหมดอายุ และวันที่ควรใช้ก่อน รวมทั้งวันที่ขายได้ของลูกค้าใดๆ</span><span class="sxs-lookup"><span data-stu-id="8e915-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="8e915-120">สำหรับสินค้าที่เชื่อมโยงกับกลุ่มมิติการจัดเก็บที่เปิดใช้งาน **ใช้กระบวนการจัดการคลังสินค้า** คุณสามารถจองหมายเลขชุดงานเฉพาะได้โดยใช้ลำดับชั้นการจองที่มีมิติสินค้าคงคลังของหมายเลขชุดงานที่กำหนดไว้ด้านบนของมิติสถานที่</span><span class="sxs-lookup"><span data-stu-id="8e915-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="8e915-121">นอกจากนี้ หน้า **การจองชุดงาน** สำหรับรายการใบสั่งขายและใบสั่งโอนย้ายจะช่วยให้คุณสามารถเลือกและจองรายการหลายรายการได้ตามหมายเลขชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8e915-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="8e915-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิ่งที่ต้องทำเมื่อคุณใช้ลำดับชั้นการจองที่มีมิติหมายเลขชุดงานที่อยู่ด้านล่างของสถานที่ โปรดดู [นโยบายการจองมิติในระดับคลังสินค้าแบบยืดหยุ่น](../warehousing/flexible-warehouse-level-dimension-reservation.md)</span><span class="sxs-lookup"><span data-stu-id="8e915-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>
