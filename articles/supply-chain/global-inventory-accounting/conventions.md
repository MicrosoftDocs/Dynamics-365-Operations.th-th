---
title: แบบแผน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าแบบแผนการกําหนดวิธีการลงบัญชีต้นทุนในการบัญชีสินค้าคงคลังส่วนกลาง
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273234"
---
# <a name="conventions"></a><span data-ttu-id="12247-103">แบบแผน</span><span class="sxs-lookup"><span data-stu-id="12247-103">Conventions</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="12247-104">แบบแผนเป็นคอนเทนเนอร์สำหรับชุดนโยบายที่มีผลกระทบต่อลักษณะการทำงานของระบบ</span><span class="sxs-lookup"><span data-stu-id="12247-104">A convention is a container for a set of policies that affect system behavior.</span></span> <span data-ttu-id="12247-105">ตามข้อกําหนดทางธุรกิจของคุณ คุณต้องกําหนดแบบแผนโดยใช้ชุดของนโยบายต่างๆ ที่กําหนดวิธีการลงบัญชีต้นทุนในการบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="12247-105">Based on your business requirements, you must define conventions by using a combination of the various policies that establish how costs should be accounted in Global Inventory Accounting.</span></span> <span data-ttu-id="12247-106">คุณสามารถเชื่อมโยงแบบแผนแต่ละแบบกับบัญชีแยกประเภทหนึ่งรายการหรือมากกว่าเพื่อให้แน่ใจว่าจะมีความสอดคล้องกันในนโยบายการบัญชีที่ใช้ระหว่างบัญชีแยกประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="12247-106">You can associate each convention with one or more ledgers to ensure consistency in accounting policies that are applied across ledgers.</span></span>

<span data-ttu-id="12247-107">เมื่อต้องการตั้งค่าแบบแผนของคุณ ให้ไปที่ **การบัญชีสินค้าคงคลังส่วนกลาง \> การตั้งค่า \> แบบแผน**</span><span class="sxs-lookup"><span data-stu-id="12247-107">To set up your conventions, go to **Global inventory accounting \> Setup \> Conventions**.</span></span> <span data-ttu-id="12247-108">สำหรับแต่ละแบบแผน ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="12247-108">For each convention, set the following fields:</span></span>

- <span data-ttu-id="12247-109">**ชื่อ** – ป้อนชื่อของแบบแผน</span><span class="sxs-lookup"><span data-stu-id="12247-109">**Name** – Enter the name of the convention.</span></span>
- <span data-ttu-id="12247-110">**คำอธิบาย** – ป้อนคำอธิบายเกี่ยวกับแบบแผน</span><span class="sxs-lookup"><span data-stu-id="12247-110">**Description** – Enter a description of the convention.</span></span>
- <span data-ttu-id="12247-111">**นโยบายออบเจ็กต์ต้นทุน** – เลือกนโยบายออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="12247-111">**Cost Object policy** – Select a cost object policy.</span></span> <span data-ttu-id="12247-112">นโยบายเหล่านี้จะระบุระดับของความละเอียดที่ระบบจะใช้ในการคํานวณและรักษาค่าของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="12247-112">These policies determine the level of granularity that the system applies to calculate and maintain the inventory value.</span></span> <span data-ttu-id="12247-113">มีตัวเลือกที่กำหนดไว้ล่วงหน้าต่อไปนี้ที่พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="12247-113">The following predefined options are available:</span></span>

    - <span data-ttu-id="12247-114">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="12247-114">Product</span></span>
    - <span data-ttu-id="12247-115">ผลิตภัณฑ์ – ไซต์</span><span class="sxs-lookup"><span data-stu-id="12247-115">Product – Site</span></span>
    - <span data-ttu-id="12247-116">ผลิตภัณฑ์ – ไซต์ – คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="12247-116">Product – Site – Warehouse</span></span>

    <span data-ttu-id="12247-117">ตัวอย่างเช่น ถ้าคุณเลือก *ผลิตภัณฑ์ – ไซต์* ให้กับทุกความเคลื่อนไหวของสินค้าคงคลัง (โฟลว์เข้าหรือโฟลว์ออก) ระบบจะคํานวณและรักษาต้นทุนสินค้าคงคลังของแต่ละผลิตภัณฑ์ในระดับไซต์</span><span class="sxs-lookup"><span data-stu-id="12247-117">For example, if you select *Product – Site*, for every inventory movement (inflow or outflow), the system calculates and maintains the inventory cost of each product at the site level.</span></span> <span data-ttu-id="12247-118">ดังนั้นความเคลื่อนไหวของสินค้าคงคลังในระดับที่ต่ำกว่า เช่น ระดับคลังสินค้าจึงไม่มีผลกระทบต่อมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="12247-118">Therefore, inventory movements at lower levels, such as the warehouse level, don't affect the inventory value.</span></span> <span data-ttu-id="12247-119">(ตัวอย่างของการโอนย้ายระดับคลังสินค้าคือการโอนย้ายสินค้าระหว่างคลังสินค้าสองแห่งในไซต์เดียว) และคุณไม่สามารถดูต้นทุนสินค้าคงคลังที่ระดับต่ำกว่าได้ เช่น ระดับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="12247-119">(An example of a warehouse-level transfer is an item transfer between two warehouses in one site.) Likewise, you can't view the inventory cost at a lower level, such as the warehouse level.</span></span>

- <span data-ttu-id="12247-120">**นโยบายพื้นฐานการป้อนข้อมูลการวัด** – เลือกนโยบายพื้นฐานการป้อนข้อมูลการวัด</span><span class="sxs-lookup"><span data-stu-id="12247-120">**Input measurement basis policy** – Select an input measurement basis policy.</span></span> <span data-ttu-id="12247-121">นโยบายเหล่านี้จะระบุต้นทุนที่ควรไหลเข้าบัญชีสินค้าคงคลังและต้นทุนที่ควรเรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="12247-121">These policies determine the costs that should flow into the inventory account and the costs that should be charged.</span></span> <span data-ttu-id="12247-122">ตัวเลือกต่อไปนี้เกี่ยวข้องกับบริษัทการค้า</span><span class="sxs-lookup"><span data-stu-id="12247-122">The following options are relevant for trading companies:</span></span>

    - <span data-ttu-id="12247-123">**ประวัติปกติ** – ส่วนประกอบต้นทุนทั้งหมดไหลเข้าสู่บัญชีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="12247-123">**Normal historical** – All the cost components flow into the inventory account.</span></span>
    - <span data-ttu-id="12247-124">**มาตรฐาน** – โฟลว์ต้นทุนมาตรฐานในบัญชีสินค้าคงคลัง และผลต่างระหว่างต้นทุนที่ใช้และต้นทุนจริงจะถูกเรียกเก็บกับบัญชีผลต่าง</span><span class="sxs-lookup"><span data-stu-id="12247-124">**Standard** – Standard cost flows into the inventory accounts, and the difference between the applied cost and the actual costs is charged to variance accounts.</span></span> <span data-ttu-id="12247-125">ถ้าคุณต้องการสร้างนโยบายพื้นฐานการป้อนข้อมูลการวัด *มาตรฐาน* คุณต้องสร้างรายการราคาที่นโยบายสามารถค้นหาต้นทุนมาตรฐานของสินค้าก่อน</span><span class="sxs-lookup"><span data-stu-id="12247-125">If you want to create a *Standard* input measurement basis policy, you must first create a price list where the policy can look up the item's standard cost.</span></span>
    - <span data-ttu-id="12247-126">**รายการราคา** – การบัญชีสินค้าคงคลังส่วนกลางสนับสนุนการดึงข้อมูลราคาสินค้าจากนิติบุคคลหลายบริษัทมาใช้</span><span class="sxs-lookup"><span data-stu-id="12247-126">**Price lists** – Global Inventory Accounting supports fetching item prices from multiple legal entities.</span></span> <span data-ttu-id="12247-127">คุณสามารถกําหนดรายการราคาที่จะใช้นโยบายพื้นฐานการป้อนข้อมูลการวัด</span><span class="sxs-lookup"><span data-stu-id="12247-127">You can define a price list that the input measurement basis policy will use.</span></span> <span data-ttu-id="12247-128">ด้วยวิธีนี้ ระบบจะทราบว่าจะค้นหาราคาสินค้าจากที่ใด</span><span class="sxs-lookup"><span data-stu-id="12247-128">In this way, the system will know where to look up the item price.</span></span> <span data-ttu-id="12247-129">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่ารายการราคา:</span><span class="sxs-lookup"><span data-stu-id="12247-129">Follow these steps to set up price lists:</span></span>

        1. <span data-ttu-id="12247-130">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="12247-130">In the **Name** field, enter a name.</span></span>
        1. <span data-ttu-id="12247-131">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="12247-131">In the **Description** field, enter a description.</span></span>
        1. <span data-ttu-id="12247-132">ในฟิลด์ **ชนิดการคำนวณต้นทุน** ให้เลือกชนิดการคำนวณต้นทุน (*ต้นทุนมาตรฐาน* หรือ *ต้นทุนที่วางแผนไว้*)</span><span class="sxs-lookup"><span data-stu-id="12247-132">In the **Costing type** field, select a costing type (*Standard cost* or *Planned cost*).</span></span>
        1. <span data-ttu-id="12247-133">ในฟิลด์ **ชนิดราคา** ให้เลือกชนิดราคา ( *ต้นทุน* *การซื้อ* หรือ *ราคาขาย*)</span><span class="sxs-lookup"><span data-stu-id="12247-133">In the **Price type** field, select a price type (*Cost*, *Purchase*, or *Sales price*).</span></span>
        1. <span data-ttu-id="12247-134">เพิ่มรุ่นการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="12247-134">Add a costing version.</span></span>
        1. <span data-ttu-id="12247-135">ในบานหน้าต่างการดำเนินการ เลือก **ราคา** เพื่อตรวจสอบความถูกต้องของราคาสินค้าในรายการราคา</span><span class="sxs-lookup"><span data-stu-id="12247-135">On the Action Pane, select **Price** to validate the item prices on the price list.</span></span>

- <span data-ttu-id="12247-136">**นโยบายสมมติฐานของกระแสต้นทุน** – เลือกนโยบายสมมติฐานของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="12247-136">**Cost flow assumption policy** – Select a cost flow assumption policy.</span></span> <span data-ttu-id="12247-137">นโยบายเหล่านี้จะระบุวิธีการลบต้นทุนออกจากสินค้าคงคลังและรายงานเป็นต้นทุนขาย</span><span class="sxs-lookup"><span data-stu-id="12247-137">These policies determine how costs are removed from inventory and reported as the cost of goods sold.</span></span> <span data-ttu-id="12247-138">มีตัวเลือกที่กำหนดไว้ล่วงหน้าต่อไปนี้ที่พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="12247-138">The following predefined options are available:</span></span>

    - <span data-ttu-id="12247-139">ค่าเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="12247-139">Average</span></span>
    - <span data-ttu-id="12247-140">เฉพาะ – ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="12247-140">Specific – Batch</span></span>

    > [!NOTE]
    > <span data-ttu-id="12247-141">การบัญชีสินค้าคงคลังส่วนกลางเป็นระบบสินค้าคงคลังแบบถาวร</span><span class="sxs-lookup"><span data-stu-id="12247-141">Global Inventory Accounting is a perpetual inventory system.</span></span> <span data-ttu-id="12247-142">ดังนั้น ระบบจะติดตามมูลค่าสินค้าคงคลังตามพื้นฐานของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="12247-142">Therefore, the system tracks the inventory value on a transaction-by-transaction basis.</span></span>

- <span data-ttu-id="12247-143">**นโยบายองค์ประกอบต้นทุน** – คุณสามารถกําหนดนโยบายองค์ประกอบต้นทุนและเชื่อมโยงนโยบายดังกล่าวไปยังฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="12247-143">**Cost element policy** – You can define cost element policies and link them to this field.</span></span> <span data-ttu-id="12247-144">*องค์ประกอบต้นทุน* คือต้นทุนของทรัพยากรที่ใช้โดยเหตุการณ์หนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="12247-144">A *cost element* is the cost of a resource that is consumed by an event.</span></span> <span data-ttu-id="12247-145">คุณสามารถใช้องค์ประกอบต้นทุนเพื่อติดตามและจัดประเภทต้นทุน</span><span class="sxs-lookup"><span data-stu-id="12247-145">You can use cost elements to track and categorize costs.</span></span> <span data-ttu-id="12247-146">หากต้องการสร้างนโยบายองค์ประกอบต้นทุน ให้ป้อนข้อมูลในที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="12247-146">To create cost element policies, enter information in the following places:</span></span>

    - <span data-ttu-id="12247-147">ฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="12247-147">**Name** field</span></span>
    - <span data-ttu-id="12247-148">ฟิลด์ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="12247-148">**Description** field</span></span>
    - <span data-ttu-id="12247-149">รายการ **องค์ประกอบต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="12247-149">**Cost element** list</span></span>
    - <span data-ttu-id="12247-150">กริด **กฎ**</span><span class="sxs-lookup"><span data-stu-id="12247-150">**Rules** grid</span></span>

    <span data-ttu-id="12247-151">ถ้าคุณไม่ต้องการแบ่งค่าสินค้าคงคลังเพิ่มเติม คุณยังต้องสร้างรายการองค์ประกอบต้นทุนที่มีองค์ประกอบต้นทุนเดียว</span><span class="sxs-lookup"><span data-stu-id="12247-151">If you don't want to break down the inventory value further, you must still create a cost element list that has a single cost element.</span></span> <span data-ttu-id="12247-152">จากนั้นคุณต้องสร้างนโยบายองค์ประกอบต้นทุนเพื่อแม็ปชนิดของการประเมินที่เกี่ยวข้องทั้งหมด (ส่วนประกอบต้นทุน) กับองค์ประกอบต้นทุนนั้น</span><span class="sxs-lookup"><span data-stu-id="12247-152">You must then create a cost element policy to map all the relevant measurement types (cost components) to that cost element.</span></span>
