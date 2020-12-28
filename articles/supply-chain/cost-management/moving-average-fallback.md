---
title: ค่าเฉลี่ยเคลื่อนที่ ลำดับต้นทุนสำรอง
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับลำดับต้นทุนสำรองสำหรับการคำนวณค่าเฉลี่ยเคลื่อนที่ใน Microsoft Dynamics 365 Supply Chain Management
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438670"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="acb08-103">ค่าเฉลี่ยเคลื่อนที่ ลำดับต้นทุนสำรอง</span><span class="sxs-lookup"><span data-stu-id="acb08-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="acb08-104">วิธีการหนึ่งที่คุณสามารถคำนวณต้นทุนของสินค้าคงคลังของคุณคือ โดยการใช้ _ค่าเฉลี่ยเคลื่อนที่_</span><span class="sxs-lookup"><span data-stu-id="acb08-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="acb08-105">คุณสามารถเชื่อมโยงมูลค่าต้นทุนได้สูงสุดสามค่ากับสินค้าในสินค้าคงคลังแต่ละรายการ:</span><span class="sxs-lookup"><span data-stu-id="acb08-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="acb08-106">**การตัดสินค้าล่าสุด** – ต้นทุนการตัดสินค้าล่าสุดที่ถูกกำหนด ก่อนที่สินค้าคงคลังจะเป็นค่าลบ</span><span class="sxs-lookup"><span data-stu-id="acb08-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="acb08-107">**ต้นทุนที่ใช้งานอยู่** – ต้นทุนล่าสุดที่ถูกเรียกใช้ในรุ่นการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="acb08-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="acb08-108">**ราคาสินค้า** – ต้นทุนที่ระบุสำหรับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="acb08-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="acb08-109">เมื่อต้องการกำหนดว่าค่าต้นทุนเหล่านี้ค่าใดควรถูกใช้ในการคำนวณค่าเฉลี่ยเคลื่อนที่ ระบบจะใช้ _ลำดับต้นทุนสำรอง_ เพื่อสร้างใบสั่งของการกำหนดลักษณะสำหรับค่า</span><span class="sxs-lookup"><span data-stu-id="acb08-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="acb08-110">ถ้าค่าต้นทุนที่ต้องการไม่พร้อมใช้งาน ระบบจะใช้ค่าที่ต้องการถัดไป และต่อไป</span><span class="sxs-lookup"><span data-stu-id="acb08-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="acb08-111">ใน Microsoft Dynamics 365 Supply Chain Management รุ่นก่อนหน้านี้ ระบบใช้ลำดับต้นทุนสำรองแบบคงที่ _(การตัดสินค้าล่าสุด – ต้นทุนที่ใช้งานอยู่ – ราคาสินค้า_)</span><span class="sxs-lookup"><span data-stu-id="acb08-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="acb08-112">ในรุ่น 10.0.11 ลำดับนี้ยังคงเป็นลำดับเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="acb08-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="acb08-113">อย่างไรก็ตาม คุณยังสามารถเปิดใช้งานคุณลักษณะที่ช่วยให้คุณสามารถเลือกจากลำดับต้นทุนสำรองที่พร้อมใช้งานสามลำดับนี้</span><span class="sxs-lookup"><span data-stu-id="acb08-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="acb08-114">คุณลักษณะนี้สามารถเป็นประโยชน์ได้ โดยเฉพาะอย่างยิ่งสำหรับองค์กรที่ใช้มูลค่าสินค้าคงคลังค่าลบอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="acb08-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="acb08-115">เมื่อต้องการทำให้ตัวเลือกสำหรับลำดับต้นทุนสำรองพร้อมใช้งาน คุณ (หรือผู้ดูแลระบบ) ต้องใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อเปิดใช้งานคุณลักษณะที่ชื่อ _ลำดับต้นทุนสำรองของค่าเฉลี่ยเคลื่อนที่_</span><span class="sxs-lookup"><span data-stu-id="acb08-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="acb08-116">เมื่อต้องการเลือกลำดับต้นทุนสำรองสำหรับการคำนวณค่าเฉลี่ยเคลื่อนที่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="acb08-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="acb08-117">เปิดหน้า **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="acb08-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="acb08-118">บนแท็บ **การลงบัญชีสินค้าคงคลัง** ในส่วน **ค่าเฉลี่ยเคลื่อนที่** ให้ตั้งค่าฟิลด์ **ลำดับต้นทุนสำรอง** เป็นค่าใดค่าหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="acb08-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="acb08-119">**การตัดสินค้าล่าสุด – ต้นทุนที่ใช้งานอยู่ – ราคาสินค้า** – ลำดับนี้เป็นลำดับเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="acb08-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="acb08-120">ซึ่งเป็นลำดับเดียวกันกับที่ใช้ ถ้าไม่ได้เปิดใช้งานคุณลักษณะ _ลำดับต้นทุนสำรองของค่าเฉลี่ยเคลื่อนที่_</span><span class="sxs-lookup"><span data-stu-id="acb08-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="acb08-121">**ต้นทุนที่ใช้งานอยู่ – การตัดสินค้าล่าสุด**</span><span class="sxs-lookup"><span data-stu-id="acb08-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="acb08-122">**ต้นทุนที่ใช้งานอยู่ – ราคาสินค้า** – องค์กรอาจพบปัญหาประสิทธิภาพการทำงาน ถ้าพวกเขาใช้กระบวนการทางธุรกิจที่ซึ่งสินค้าคงคลังเป็นค่าลบอย่างสม่ำเสมอ และในเวลาเดียวกัน ปริมาณของธุรกรรมนั้นสูง</span><span class="sxs-lookup"><span data-stu-id="acb08-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="acb08-123">การตั้งค่านี้สามารถช่วยลดปัญหาประสิทธิภาพการทำงานเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="acb08-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="acb08-124">![พารามิเตอร์การบัญชีสินค้าคงคลัง](media/inventory-accounting-parameters.png "พารามิเตอร์การบัญชีสินค้าคงคลัง")</span><span class="sxs-lookup"><span data-stu-id="acb08-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
