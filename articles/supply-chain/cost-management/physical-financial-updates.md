---
title: เกี่ยวกับการปรับปรุงข้อมูลทางการเงินตามจริง
description: ในหัวข้อนี้จะแสดงภาพรวมของชนิดธุรกรรมที่เพิ่มหรือลดปริมาณสินค้าคงคลัง
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee65fa43b43bc8b6cbf9763ac4fa8774f30afb98
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263577"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="428b1-103">เกี่ยวกับการปรับปรุงข้อมูลทางการเงินตามจริง</span><span class="sxs-lookup"><span data-stu-id="428b1-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="428b1-104">ในหัวข้อนี้จะแสดงภาพรวมของชนิดธุรกรรมที่เพิ่มหรือลดปริมาณสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="428b1-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="428b1-105">ธุรกรรมสินค้าคงคลังสามารถถูกปรับปรุงทางกายภาพและถูกปรับปรุงทางการเงินได้ใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="428b1-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="428b1-106">ธุรกรรมทางกายภาพ และทางการเงินบางอย่างเพิ่มปริมาณสินค้าคงคลัง ในขณะที่ธุรกรรมบางอย่างจะลดปริมาณสินค้าคงเหลือลง</span><span class="sxs-lookup"><span data-stu-id="428b1-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="428b1-107">การเพิ่มขึ้นทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="428b1-107">Physical increases</span></span>
<span data-ttu-id="428b1-108">เมื่อมีการลงบัญชีธุรกรรมนั้นแล้ว สถานะของบันทึกธุรกรรมจะเป็น **ได้รับแล้ว**</span><span class="sxs-lookup"><span data-stu-id="428b1-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="428b1-109">ธุรกรรมต่อไปนี้จะถือว่าเป็นการเพิ่มขึ้นทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="428b1-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="428b1-110">การรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="428b1-110">Purchase order receipt</span></span>
-   <span data-ttu-id="428b1-111">การส่งคืนบันทึกการจัดส่งของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="428b1-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="428b1-112">รายงานการการผลิตสินค้าที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="428b1-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="428b1-113">ผลผลอยได้ในบันทึกการจัดส่งของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="428b1-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="428b1-114">การเพิ่มขึ้นทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="428b1-114">Financial increases</span></span>
<span data-ttu-id="428b1-115">รายการทางการค้าเกิดขึ้นเมื่อมีการออกใบเสร็จรับเงิน สถานะของบันทึกธุรกรรมที่เพิ่มปริมาณจะเป็น **ซื้อแล้ว**</span><span class="sxs-lookup"><span data-stu-id="428b1-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="428b1-116">ธุรกรรมต่อไปมีผลให้การเงินเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="428b1-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="428b1-117">ใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="428b1-117">Vendor invoice</span></span>
-   <span data-ttu-id="428b1-118">ใบแจ้งหนี้ใบสั่งขายสำหรับการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="428b1-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="428b1-119">การคำนวณต้นทุนใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="428b1-119">Production order costing</span></span>
-   <span data-ttu-id="428b1-120">ยอดของสินค้าคงเหลือในสมุดบันชีรายวัน บอกความเคลื่นไหว กำไรและขาดทุน การนับจำนวน รายการวัสดุและส่วนประกอบ   และการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="428b1-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="428b1-121">ธุรกรรมที่เพิ่มปริมาณ</span><span class="sxs-lookup"><span data-stu-id="428b1-121">Transactions that increase quantity</span></span>
<span data-ttu-id="428b1-122">รายการค้าที่เกิดขึ้นถูกโอนไปที่เป็นต้นทุนโดยวิธีการเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="428b1-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="428b1-123">Dynamics AX ใช้การคำนวณราคาต้นทุนเฉลี่ยเมื่อมีเกิดรายการค้าที่ทำให้สินค้าคงเหลือลดจำนวนลง โดยไม่คำนึงถึงแบบจำลองสินค้าคงคลังที่เกี่ยวข้องกับสินค้าคงคลังนั้น</span><span class="sxs-lookup"><span data-stu-id="428b1-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="428b1-124">สามารถดูข้อมูลเกี่ยวกับราคาต้นทุนเฉลี่ยที่นี่ [ราคาต้นทุนเฉลี่ยปัจจุบัน](running-average-cost-price.md)</span><span class="sxs-lookup"><span data-stu-id="428b1-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="428b1-125">ธุรกรรมที่ลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="428b1-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="428b1-126">ราคาต้นทุนเฉลี่ยที่รันการคำนวณอยู่ถูกใช้เมื่อธุรกรรมลดจำนวนลงรายการลง โดยไม่คำนึงถึงแบบจำลองสินค้าคงคลังที่เกี่ยวข้องกับสินค้าคงคลังนั้น</span><span class="sxs-lookup"><span data-stu-id="428b1-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="428b1-127">รายการค้าที่ลดจำนวนลงจะไม่ถูกลงบัญชีจนกว่ารายการค้าที่เกิดขึ้นก่อนหน้านั้นลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="428b1-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="428b1-128">หากสินค้าคงคลังที่พร้อมใช้งานจริงกลายเป็นติดลบ ต้นทุนสินค้าคงคลังที่ถูกกำหนดสำหรับรายการในหน้า **รายการ** จะถูกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="428b1-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="428b1-129">หากฟังก์ชันหลายไซต์ถูกเปิดใช้งาน ต้นทุนนี้จะเป็นต้นทุนสินค้าคงคลังที่กำหนดสำหรับไซต์ในหน้า **การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="428b1-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="428b1-130">การตัดสินค้าตามจริงเทียบกับการตัดสินค้าทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="428b1-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="428b1-131">เมื่อมีการลงบัญชีธุรกรรมนั้นแล้ว สถานะของบันทึกธุรกรรมนี้เป็น **หักแล้ว**</span><span class="sxs-lookup"><span data-stu-id="428b1-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="428b1-132">ธุรกรรมต่อไปนี้ได้รับพิจารณาว่าเป็นปัญหาทางกายภาพ:</span><span class="sxs-lookup"><span data-stu-id="428b1-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="428b1-133">สมุดรายวันรายการเบิกสินค้าของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="428b1-133">Production order picking list journal</span></span>
-   <span data-ttu-id="428b1-134">บันทึกการจัดส่งของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="428b1-134">Sales order packing slip</span></span>
-   <span data-ttu-id="428b1-135">การส่งคืนบันทึกการจัดส่งของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="428b1-135">Purchase order packing slip return</span></span>

<span data-ttu-id="428b1-136">เมื่อมีการลงบัญชีธุรกรรมนั้นแล้ว สถานะของบันทึกธุรกรรมนี้เป็น **ขายแล้ว**</span><span class="sxs-lookup"><span data-stu-id="428b1-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="428b1-137">ธุรกรรมต่อไปนี้ได้รับพิจารณาว่าเป็นปัญหาทางการเงิน:</span><span class="sxs-lookup"><span data-stu-id="428b1-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="428b1-138">ผลิตสินค้าตามใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="428b1-138">Ending a production order</span></span>
-   <span data-ttu-id="428b1-139">ใบแจ้งหนี้ของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="428b1-139">Sales order invoice</span></span>
-   <span data-ttu-id="428b1-140">ส่งคืนใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="428b1-140">Vendor invoice return</span></span>
-   <span data-ttu-id="428b1-141">ยอดของสินค้าคงเหลือในสมุดบันชีรายวัน บอกความเคลื่นไหว กำไรและขาดทุน การนับจำนวน รายการวัสดุและส่วนประกอบ   และการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="428b1-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="428b1-142">รายการค้าที่ทำให้สินค้าลดลง ถูกโอนไปที่เป็นต้นทุนโดยวิธีการเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="428b1-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="428b1-143">กระบวนการตรวจนับสินค้าคงคลัง คือ จับคู่ธุรกรรมการค้าที่เกิดขึ้นกับใบเสร็จ ขึ้นอยู่กับวิธีการที่ใช่้ในการจัดการสินค้าคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="428b1-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]