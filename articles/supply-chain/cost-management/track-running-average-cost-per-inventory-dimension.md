---
title: "การติดตามต้นทุนถัวเฉลี่ยต่อมิติสินค้าคงคลัง"
description: "กลุ่มมิติสินค้าคงคลังถูกแนบกับทุกๆสินค้าในสินค้าคงคลัง ดังนั้นระบบจะคำนวณราคาต้นทุนเฉลี่ยสืบเนื่องโดยยึดตามมิติสินค้าคงคลังที่เลือกไว้และมีการติดตามการเปลี่ยนแปลงข้อมูลทางการเงิน"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bb2a3a193585944810c5dfac1eb3c019e074008f
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="a86eb-104">การติดตามต้นทุนถัวเฉลี่ยต่อมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a86eb-104">Tracking running average cost per inventory dimension</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="a86eb-105">กลุ่มมิติสินค้าคงคลังถูกแนบกับทุกๆสินค้าในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a86eb-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="a86eb-106">ดังนั้นระบบจะคำนวณราคาต้นทุนเฉลี่ยสืบเนื่องโดยยึดตามมิติสินค้าคงคลังที่เลือกไว้และมีการติดตามการเปลี่ยนแปลงข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a86eb-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="a86eb-107">มีมิติสินค้าคงคลังอยู่สามชนิด ได้แก่ ผลิตภัณฑ์ การจัดเก็บและการติดตาม</span><span class="sxs-lookup"><span data-stu-id="a86eb-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="a86eb-108">มิติของผลิตภัณฑ์รวมการตั้งค่าคอนฟิก ขนาด และสี</span><span class="sxs-lookup"><span data-stu-id="a86eb-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="a86eb-109">มิติสินค้าจะถูกติดตามทางการเงินเสมอ</span><span class="sxs-lookup"><span data-stu-id="a86eb-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="a86eb-110">การจัดเก็บและการติดตามมิติรวมไซต์ คลังสินค้า ที่ตั้ง สถานะสินค้าคงคลัง ป้ายทะเบียน หมายเลขชุดงาน และหมายเลขลำดับประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="a86eb-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="a86eb-111">คุณสามารถกำหนดได้ถึงการจัดเก็บและการติดตามมิติจะถูกติดตามข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a86eb-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="a86eb-112">**ตัวอย่างที่ 1**</span><span class="sxs-lookup"><span data-stu-id="a86eb-112">**Example 1**</span></span> 

<span data-ttu-id="a86eb-113">หากกลุ่มมิติการจัดเก็บเชื่อมโยงอยู่กับสินค้านั้นมีการติดตามข้อมูลทางการเงินตามคลังสินค้า ระบบจะคำนวณราคาต้นทุนเฉลี่ยสืบเนื่องสำหรับคลังสินค้าแต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="a86eb-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="a86eb-114">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a86eb-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="a86eb-115">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 2 หน่วย ที่ราคาต่อหน่วย USD 10.00 สำหรับคลังสินค้า GW</span><span class="sxs-lookup"><span data-stu-id="a86eb-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="a86eb-116">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 3 หน่วย ที่ราคาต่อหน่วย USD 12.00 สำหรับคลังสินค้า GW</span><span class="sxs-lookup"><span data-stu-id="a86eb-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="a86eb-117">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 5 หน่วย ที่ราคาต่อหน่วย USD 15.00 สำหรับคลังสินค้า MW</span><span class="sxs-lookup"><span data-stu-id="a86eb-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="a86eb-118">ราคาต้นทุนเฉลี่ยสืบเนื่องสำหรับคลังสินค้า GW คือ USD 11.20 และราคาต้นทุนเฉลี่ยสืบเนื่องสำหรับคลังสินค้า MW คือ USD 15.00</span><span class="sxs-lookup"><span data-stu-id="a86eb-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="a86eb-119">ใบแจ้งหนี้ของใบสั่งขายจะถูกลงรายการบัญชีสำหรับคลังสินค้า GW</span><span class="sxs-lookup"><span data-stu-id="a86eb-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="a86eb-120">มูลค่าของสินค้าคงคลังและต้นทุนของสินค้าที่ขาย (ก่อนการปิดสินค้าคงคลังมีการถูกรัน และไม่มีการทำเครื่องหมาย) คือ USD 11.20</span><span class="sxs-lookup"><span data-stu-id="a86eb-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="a86eb-121">ใบแจ้งหนี้ของใบสั่งขายอื่นจะถูกลงรายการบัญชีสำหรับคลังสินค้า MW</span><span class="sxs-lookup"><span data-stu-id="a86eb-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="a86eb-122">มูลค่าของสินค้าคงคลังและต้นทุนของสินค้าที่ขาย (ก่อนการปิดสินค้าคงคลังมีการถูกรัน และไม่มีการทำเครื่องหมาย) คือ USD 15.00</span><span class="sxs-lookup"><span data-stu-id="a86eb-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="a86eb-123">**ตัวอย่างที่ 2** ถ้ากลุ่มมิติการจัดเก็บที่ถูกแนบอยู่กับสินค้าที่มีการติดตามข้อมูลทางการเงินตามคลังสินค้าและการติดตามกลุ่มมิติมีการติดตามข้อมูลทางการเงินโดยเรียงตามหมายเลขชุดงาน ราคาต้นทุนเฉลี่ยสืบเนื่องจะถูกคำนวณสำหรับแต่ละชุดงาน</span><span class="sxs-lookup"><span data-stu-id="a86eb-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="a86eb-124">**หมายเหตุ:** เราขอแนะนำให้คุณดูราคาต้นทุนที่ถูกติดตามข้อมูลของมิติทางการเงินทั้งหมดเสมอ</span><span class="sxs-lookup"><span data-stu-id="a86eb-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="a86eb-125">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a86eb-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="a86eb-126">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 2 หน่วย ที่ราคาต่อหน่วย USD 10.00 ออกใบแจ้งหนี้สำหรับคลังสินค้า GW และชุดงาน AAA</span><span class="sxs-lookup"><span data-stu-id="a86eb-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="a86eb-127">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 3 หน่วย ที่ราคาต่อหน่วย USD 12.00 ออกใบแจ้งหนี้สำหรับคลังสินค้า GW และชุดงาน AAA</span><span class="sxs-lookup"><span data-stu-id="a86eb-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="a86eb-128">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 2 หน่วย ที่ราคาต่อหน่วย USD 15.00 ออกใบแจ้งหนี้สำหรับคลังสินค้า GW และชุดงาน BBB</span><span class="sxs-lookup"><span data-stu-id="a86eb-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="a86eb-129">ราคาต้นทุนเฉลี่ยสืบเนื่องสำหรับคลังสินค้า GW และชุดงาน AAA คือ USD 11.20 และราคาต้นทุนเฉลี่ยสืบเนื่องสำหรับคลังสินค้า GW และชุดงาน BBB คือ USD 15.00</span><span class="sxs-lookup"><span data-stu-id="a86eb-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




