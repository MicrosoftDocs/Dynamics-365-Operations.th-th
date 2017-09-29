---
title: "จองชุดงานเดียวกันสำหรับใบสั่งขาย"
description: "บทความนี้อธิบายวิธีการตั้งค่าผลิตภัณฑ์เพื่ออนุญาตการจองสินค้าคงคลังโดยเทียบกับชุดงานหนึ่งของสินค้าคงคลัง"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 8e0f8f85609e7c3095f13738d43cdf5734018eaa
ms.contentlocale: th-th
ms.lasthandoff: 07/18/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="2a8a0-103">จองชุดงานเดียวกันสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="2a8a0-103">Reserve the same batch for a sales order</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2a8a0-104">บทความนี้อธิบายวิธีการตั้งค่าผลิตภัณฑ์เพื่ออนุญาตการจองสินค้าคงคลังโดยเทียบกับชุดงานหนึ่งของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2a8a0-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="2a8a0-105">การจองชุดงานเดียวกันช่วยให้คุณจองสินค้าคงคลังสำหรับบรรทัดใบสั่งขายจากชุดงานหนึ่งของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2a8a0-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="2a8a0-106">ตัวอย่างเช่น ลูกค้าที่สั่งพื้นหลังสามารถร้องขอให้ใบสั่งทั้งหมดถูกระบุจากชุดงาน หรือล็อตเดียวกัน เพื่อหลีกเลี่ยงความไม่สอดคล้องกันระหว่างการรวบรวม</span><span class="sxs-lookup"><span data-stu-id="2a8a0-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="2a8a0-107">เพื่อตั้งค่าผลิตภัณฑ์ให้ใช้การจองชุดงานเดียวกัน การตั้งค่าต่อไปนี้ต้องใช้งานอยู่ในกลุ่มแบบจำลองสินค้า กลุ่มมิติการติดตาม และกลุ่มมิติการจัดเก็บที่คุณกำหนดให้กับผลิตภัณฑ์:</span><span class="sxs-lookup"><span data-stu-id="2a8a0-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="2a8a0-108">**กลุ่มแบบจำลองสินค้า** – กลุ่มแบบจำลองสินค้าต้องมีฟิลด์ **การเลือกชุดงานเดียวกัน** และฟิลด์ **รวมความต้องการ** ถูกเลือกในกลุ่มฟิลด์ **การจอง** สำหรับนโยบายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2a8a0-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="2a8a0-109">**กลุ่มมิติการติดตาม** – กลุ่มมิติการติดตามต้องมีฟิลด์ **แผนความครอบคลุมตามมิติ** ที่เลือกไว้สำหรับหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2a8a0-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="2a8a0-110">**กลุ่มมิติการจัดเก็บ** – กลุ่มมิติการจัดเก็บต้องมีฟิลด์ **แผนความครอบคลุมตามมิติ** ที่ถูกเลือกสำหรับ **ไซต์** และ **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="2a8a0-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="2a8a0-111">เมื่อคุณจองสินค้าคงคลังสำหรับผลิตภัณฑ์ในบรรทัดใบสั่งขายที่ตั้งค่าไว้สำหรับการเลือกชุดงานเดียวกัน Microsoft Dynamics 365 for Finance and Operations พยายามจองปริมาณที่สั่งจากชุดงานสินค้าคงคลังเดียว</span><span class="sxs-lookup"><span data-stu-id="2a8a0-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="2a8a0-112">มีข้อกำหนดแอททริบิวต์ของชุดงานเฉพาะใดๆ ถูกพิจารณาด้วย</span><span class="sxs-lookup"><span data-stu-id="2a8a0-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="2a8a0-113">ถ้าไม่สามารถป้อนปริมาณจากชุดงานเดียว หน้า **ความขัดแย้งของการจองสินค้าของชุดงานเดียวกัน** จะปรากฏ</span><span class="sxs-lookup"><span data-stu-id="2a8a0-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="2a8a0-114">หน้านี้อธิบายถึงปัญหา และการดำเนินการที่คุณมาสามารถดำเนินการจองต่อไป</span><span class="sxs-lookup"><span data-stu-id="2a8a0-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="2a8a0-115">เงื่อนไขต่อไปนี้อาจป้องกันชุดงานจากการถูกจอง:</span><span class="sxs-lookup"><span data-stu-id="2a8a0-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="2a8a0-116">รหัสการโอนการครอบครองชุดงานที่ **บล็อคการจองสินค้า** สำหรับการขายที่ติดแฟล็กเป็น **ถูกบล็อค**</span><span class="sxs-lookup"><span data-stu-id="2a8a0-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="2a8a0-117">ชุดงานที่หมดอายุ ขึ้นอยู่กับวันหมดอายุ และวันที่ขายได้ของลูกค้าที่เกี่ยวข้องใดๆ</span><span class="sxs-lookup"><span data-stu-id="2a8a0-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="2a8a0-118">สินค้ายังคงถูกพิจารณาถ้ากลุ่มแบบจำลองสินค้าสำหรับสินค้าถูกควบคุมด้วยที่หมดอายุแรกออกก่อน (FEFO) และถ้าวันที่ควรใช้ก่อนถูกเลือกตามเกณฑ์การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a8a0-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="2a8a0-119">ชุดงานไม่มีอายุการเก็บที่เหลือเพียงพอ ขึ้นอยู่กับวันหมดอายุ และวันที่ควรใช้ก่อน รวมทั้งวันที่ขายได้ของลูกค้าใดๆ</span><span class="sxs-lookup"><span data-stu-id="2a8a0-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





