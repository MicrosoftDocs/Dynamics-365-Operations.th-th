---
title: การยืนยันการเบิกสินค้าเป็นรายชิ้น
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและใช้การยืนยันการเบิกสินค้าเป็นรายชิ้นจากอุปกรณ์เคลื่อนที่
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed63245066799d7d8f14362ab6c9193c0cda7c4a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438362"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="f08c3-103">การยืนยันการเบิกสินค้าเป็นรายชิ้น</span><span class="sxs-lookup"><span data-stu-id="f08c3-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f08c3-104">การเบิกสินค้าเป็นรายชิ้นช่วยให้คุณยืนยันสินค้าคงคลังแต่ละชิ้นโดยใช้การเบิกสินค้าหรืองานการตรวจนับบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f08c3-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="f08c3-105">สำหรับการเบิกสินค้า คุณสามารถยืนยันปริมาณของงานที่จะประมวลผลเท่ากับปริมาณที่ระบุในงานที่จะเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="f08c3-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="f08c3-106">สำหรับงานการตรวจนับ คุณสามารถสแกนสินค้าคงคลังที่คุณกำลังทำการตรวจนับและติดตามยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="f08c3-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="f08c3-107">เมื่อคุณเปิดใช้งานการเบิกสินค้าเป็นรายชิ้น จะมีการเลือการยืนยันผลิตภัณฑ์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f08c3-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="f08c3-108">สำหรับการเบิกสินค้าตามชนิดงาน จะเปิดใช้งานหมายเลขสูงสุดของสินค้าชิ้นนั้น</span><span class="sxs-lookup"><span data-stu-id="f08c3-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="f08c3-109">ซึ่งช่วยให้คุณสามารถตั้งค่าจำนวนสูงสุดเป็นจำนวนชิ้นที่ต้องได้รับการยืนยันในระหว่างกระบวนการงาน</span><span class="sxs-lookup"><span data-stu-id="f08c3-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="f08c3-110">ปริมาณสูงสุดจะขึ้นอยู่กับหน่วยงานปัจจุบันที่กำลังประมวลผลอยู่</span><span class="sxs-lookup"><span data-stu-id="f08c3-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="f08c3-111">ชนิดของงานการตรวจนับไม่อนุญาตให้มีการค่าสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f08c3-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="f08c3-112">คุณยังสามารถใช้ปริมาณและหน่วยวัด (UOM) ที่เชื่อมโยงกับสแกนบาร์โค้ดได้</span><span class="sxs-lookup"><span data-stu-id="f08c3-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="f08c3-113">ซึ่งจะทำงานสำหรับการรับสินค้ากระแสในขั้นตอนขาเข้า รวมทั้งการรับการรับป้ายทะเบียนแบบผสม สินค้าในใบสั่งซื้อ สินค้าในใบสั่งโอนย้าย และสินค้าของจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="f08c3-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="f08c3-114">ซึ่งทำงานสำหรับการเบิกชิ้นเป็นรายชิ้นที่สแกนบาร์โค้ดจะเพิ่มปริมาณไปยังจำนวนรวมของชิ้นส่วนที่มีการแปลงหน่วยระหว่างหน่วยวัดบนบาร์โค้ดและหน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="f08c3-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="f08c3-115">ถ้าเมื่อตรวจนับหน่วยวัดบนบาร์โคด จะยืนยันได้ว่าปริมาณที่อนุญาตสำหรับการตรวจนับในกลุ่มลำดับ ปริมาณจะถูกเพิ่มเข้าไปกับจำนวนรวม</span><span class="sxs-lookup"><span data-stu-id="f08c3-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f08c3-116">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="f08c3-116">Where it applies</span></span>

<span data-ttu-id="f08c3-117">งานการเบิกสินค้าเป็นรายชิ้นสำหรับงานการตรวจนับทั้งหมด และสำหรับการเบิกสินค้าเริ่มต้นสำหรับงานชนิดใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="f08c3-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="f08c3-118">จะไม่สามารถใช้การเบิกสินค้าเป็นรายชิ้น ถ้าสินค้าถูกควบคุมโดยเรียงตามหมายเลขลำดับประจำสินค้า หรือถ้ามีการผลิตหรือการเบิกสินค้าคัมบังจากสถานที่เก็บป้ายทะเบียน (ป้ายทะเบียน) และมีการตั้งค่าสินค้าเป็นระยะ</span><span class="sxs-lookup"><span data-stu-id="f08c3-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="f08c3-119">ตั้งค่าการเบิกสินค้าเป็นรายชิ้น</span><span class="sxs-lookup"><span data-stu-id="f08c3-119">Set up piece picking</span></span>

1.  <span data-ttu-id="f08c3-120">บนรายการเมนูบนอุปกรณ์เคลื่อนที่ เปิดแบบฟอร์มการตั้งการสำรหับการยืนยันงาน: > **การบริหารคลังสินค้า** > **ตั้งค่า** > **อุปกรณ์เคลื่อนที่** > **รายการเมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="f08c3-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="f08c3-121">จากรายการเมนูบนอุปกรณ์เคลื่อนที่ เปิดการตั้งค่าการยืนยันงาน</span><span class="sxs-lookup"><span data-stu-id="f08c3-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="f08c3-122">ตัวเลือกต่อไปนี้เปลี่ยนเป็นพร้อมใช้งานสำหรับการเลือก เมื่อชนิดงานเป็นการเบิกสินค้าหรือการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="f08c3-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="f08c3-123">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f08c3-123">Option</span></span>           |                                                                            <span data-ttu-id="f08c3-124">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f08c3-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08c3-125">การยืนยันการเบิกสินค้าเป็นรายชิ้น</span><span class="sxs-lookup"><span data-stu-id="f08c3-125">Piece picking confirmation</span></span> | <span data-ttu-id="f08c3-126">พร้อมใช้งานสำหรับชนิดของงานการตรวจนับและการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="f08c3-126">Available for pick and counting work types.</span></span> <span data-ttu-id="f08c3-127">จะมีการเลือกการยืนยันผลิตภัณฑ์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f08c3-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="f08c3-128">ช่วยให้คุณสามารถยืนยันสินค้าคงคลังแต่ละรายการได้จากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f08c3-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="f08c3-129">จำนวนชิ้นสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f08c3-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="f08c3-130">พร้อมใช้งานสำหรับงานการเบิกสินค้า ถ้าเปิดใช้งานการยืนยันการเบิกสินค้าเป็นรายชิ้น</span><span class="sxs-lookup"><span data-stu-id="f08c3-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="f08c3-131">ตั้งค่าขีดจำกัดจำนวนชิ้นที่คุณต้องยืนยัน</span><span class="sxs-lookup"><span data-stu-id="f08c3-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |

