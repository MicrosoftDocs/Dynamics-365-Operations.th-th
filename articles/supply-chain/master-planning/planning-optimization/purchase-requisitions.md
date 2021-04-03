---
title: ใบขอซื้อ
description: หัวข้อนี้อธิบายวิธีการสนับสนุนใบขอซื้อในการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 20b4012e054a25d7d21c6f017d8ebcf18f6ee28d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501089"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="56521-103">ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="56521-103">Purchase requisitions</span></span>

<span data-ttu-id="56521-104">การวางแผนหลักสามารถเติมสินค้าในใบขอซื้อที่อนุมัติแล้วได้</span><span class="sxs-lookup"><span data-stu-id="56521-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="56521-105">ดังนั้น เพื่อครอบคลุมใบขอซื้อ ผู้ใช้จึงไม่ต้องใช้ลำดับงานเพื่อสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="56521-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="56521-106">แต่การวางแผนหลักอาจครอบคลุมใบขอซื้อได้</span><span class="sxs-lookup"><span data-stu-id="56521-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="56521-107">เนื่องจากฟังก์ชันนี้ ใบขอซื้อจึงสามารถสร้างใบสั่งซื้อ ใบสั่งโอนย้าย หรือใบสั่งผลิต ทั้งนี้ขึ้นอยู่กับค่า **ชนิดแผนการใบสั่ง** ที่ตั้งค่าไว้ให้กับผลิตภัณฑ์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="56521-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="56521-108">เปิดใช้งานแผนหลักเพื่อรวมใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="56521-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="56521-109">เมื่อต้องการรวมใบขอซื้อในระหว่างการคํานวณความครอบคลุมของแผนหลัก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="56521-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="56521-110">ไปที่ **การวางแผนหลัก** \> **การตั้งค่า** \> **แผน** \> **แผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="56521-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="56521-111">สร้างหรือเลือกแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="56521-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="56521-112">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **รวมใบขอซื้อ** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="56521-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="56521-113">ทําซ้ำขั้นตอนที่ 2 และ 3 กับแผนหลักแต่ละแผนที่คุณต้องการรวมใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="56521-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="56521-114">กรอบเวลาคำขอที่อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="56521-114">Approved requisitions time fence</span></span>

<span data-ttu-id="56521-115">*กรอบเวลาใบขอซื้อที่อนุมัติ* จะสร้างว่าความต้องการที่แผนหลักจะรวมย้อนกลับไป (เป็นวัน) เท่าใดจากใบขอซื้อการเติมสินค้าที่อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="56521-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="56521-116">คุณสามารถตั้งค่ากรอบเวลาของใบขอซื้อที่อนุมัติแล้วในระดับกลุ่มความครอบคลุมและระดับแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="56521-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="56521-117">ตั้งค่ากรอบเวลาใบขอซื้อที่อนุมัติแล้วของกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="56521-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="56521-118">ไปยัง **การวางแผนหลัก** \> **การตั้งค่า** \> **ความครอบคลุม** \> **กลุ่มความครอบคลุม**</span><span class="sxs-lookup"><span data-stu-id="56521-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="56521-119">สร้างหรือเลือกกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="56521-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="56521-120">บนแท็บด่วน **อื่น** ให้ตั้งค่าฟิลด์ **กรอบเวลาของใบขอซื้อที่อนุมัติแล้ว (วัน)** เป็นจํานวนวันที่จะรวมไว้ในกรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="56521-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="56521-121">ทําซ้ําขั้นตอนที่ 2 และ 3 ของแต่ละกลุ่มความครอบคลุมเพิ่มเติม ซึ่งคุณต้องการตั้งค่ากรอบเวลาของใบขอซื้อที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="56521-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="56521-122">ตั้งค่ากรอบเวลาใบขอซื้อที่อนุมัติแล้วของแต่ละแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="56521-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="56521-123">เมื่อคุณตั้งค่ากรอบเวลาของใบขอซื้อที่อนุมัติแล้วของแต่ละแผนหลัก การตั้งค่าจะแทนที่การตั้งค่ากรอบเวลาสำหรับกลุ่มความครอบคลุมที่เกี่ยวข้องใด ๆ</span><span class="sxs-lookup"><span data-stu-id="56521-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="56521-124">ไปที่ **การวางแผนหลัก** \> **การตั้งค่า** \> **แผน** \> **แผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="56521-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="56521-125">สร้างหรือเลือกแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="56521-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="56521-126">บนแท็บด่วน **กรอบเวลาเป็นวัน** ให้ตั้งค่าฟิลด์ **กรอบเวลาของใบขอซื้อที่อนุมัติแล้ว (วัน)** เป็นจํานวนวันที่จะรวมไว้ในกรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="56521-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="56521-127">ทําซ้ําขั้นตอนที่ 2 และ 3 ของแต่ละแผนหลักเพิ่มเติม ซึ่งคุณต้องการตั้งค่ากรอบเวลาของใบขอซื้อที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="56521-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56521-128">**เร็ว ๆ นี้:** กรอบเวลาของใบขอซื้อที่อนุมัติแล้วยังไม่ได้รับการสนับสนุนสำหรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="56521-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="56521-129">จนกว่าจะได้รับการสนับสนุน ค่าทั้งหมดที่คุณป้อนในฟิลด์ **กรอบเวลาของใบขอซื้อที่อนุมัติแล้ว (วัน)** จะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="56521-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="56521-130">การจัดหาวัสดุอิสระ โดยไม่พิจารณารหัสความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="56521-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="56521-131">ใบขอซื้อจะครอบคลุมโดยแผนการใบสั่งอิสระเสมอ ไม่ว่ารหัสความครอบคลุมจะเป็นอย่างไรก็ตาม</span><span class="sxs-lookup"><span data-stu-id="56521-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="56521-132">ลักษณะการทำงานนี้ช่วยให้มั่นใจถึงความสามารถในการติดตามและลำดับงานที่ชัดเจนระหว่างใบขอซื้อและใบสั่งการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="56521-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="56521-133">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="56521-133">Example 1</span></span>

<span data-ttu-id="56521-134">ตั้งค่าผลิตภัณฑ์เพื่อให้มีค่า **รหัสความครอบคลุม** เป็น *ต่ำสุด/สูงสุด* สินค้าคงคลังและสถานะใบขอซื้อมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56521-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="56521-135">ปริมาณคงคลังคงเหลือ = 10</span><span class="sxs-lookup"><span data-stu-id="56521-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="56521-136">ปริมาณสินค้าคงคลังขั้นต่ำ = 15</span><span class="sxs-lookup"><span data-stu-id="56521-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="56521-137">ปริมาณสินค้าคงคลังสูงสุด = 20</span><span class="sxs-lookup"><span data-stu-id="56521-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="56521-138">มีใบขอซื้ออยู่หนึ่งชิ้น</span><span class="sxs-lookup"><span data-stu-id="56521-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="56521-139">มีวันที่ร้องขอของวันนี้</span><span class="sxs-lookup"><span data-stu-id="56521-139">It has a requested date of today.</span></span>

<span data-ttu-id="56521-140">เมื่อการวางแผนหลักทำงาน จะมีการสร้างแผนการใบสั่งขึ้นสองแผน โดยแผนหนึ่งแผนคือ 10 ชิ้นเพื่อเติมสินค้าในสินค้าคงคลังในปริมาณสูงสุด และอีกแผนหนึ่งเป็นหนึ่งชิ้นเพื่อเติมสินค้าในใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="56521-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="56521-141">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="56521-141">Example 2</span></span>

<span data-ttu-id="56521-142">ตั้งค่าผลิตภัณฑ์เพื่อให้มีค่า **รหัสความครอบคลุม** เป็น *ต่ำสุด/สูงสุด* สินค้าคงคลังและสถานะใบขอซื้อมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56521-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="56521-143">ปริมาณคงคลังคงเหลือ = 17</span><span class="sxs-lookup"><span data-stu-id="56521-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="56521-144">ปริมาณสินค้าคงคลังขั้นต่ำ = 15</span><span class="sxs-lookup"><span data-stu-id="56521-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="56521-145">ปริมาณสินค้าคงคลังสูงสุด = 20</span><span class="sxs-lookup"><span data-stu-id="56521-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="56521-146">มีใบขอซื้ออยู่หนึ่งชิ้น</span><span class="sxs-lookup"><span data-stu-id="56521-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="56521-147">มีวันที่ร้องขอของวันนี้</span><span class="sxs-lookup"><span data-stu-id="56521-147">It has a requested date of today.</span></span>

<span data-ttu-id="56521-148">เมื่อการวางแผนหลักทำงาน แผนการใบสั่งหนึ่งแผนต่อหนึ่งชิ้นจะถูกสร้างขึ้นเพื่อเติมสินค้าในใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="56521-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="56521-149">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="56521-149">Example 3</span></span>

<span data-ttu-id="56521-150">ตั้งค่าผลิตภัณฑ์เพื่อให้มีค่า **รหัสความครอบคลุม** ของ *รอบระยะเวลา* และความยาวของรอบระยะเวลาเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="56521-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="56521-151">มีสถานะสินค้าคงคลัง ใบสั่งขาย และใบขอซื้อดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56521-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="56521-152">ปริมาณคงคลังคงเหลือ = 0</span><span class="sxs-lookup"><span data-stu-id="56521-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="56521-153">มีใบสั่งขายห้าชิ้นอยู่</span><span class="sxs-lookup"><span data-stu-id="56521-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="56521-154">มีวันที่จัดส่งที่คาดไว้ของวันนี้บวกหนึ่งวัน</span><span class="sxs-lookup"><span data-stu-id="56521-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="56521-155">มีใบขอซื้ออยู่สามชิ้น</span><span class="sxs-lookup"><span data-stu-id="56521-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="56521-156">มีวันที่ร้องขอของวันนี้บวกสามวัน</span><span class="sxs-lookup"><span data-stu-id="56521-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="56521-157">เมื่อการวางแผนหลักทำงาน จะมีการสร้างแผนการใบสั่งขึ้นสองแผน โดยแผนหนึ่งแผนคือ สามชิ้นเพื่อเติมสินค้าในใบขอซื้อ และหนึ่งแผนคือ ห้าชิ้นเพื่อเติมสินค้าในความต้องการของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56521-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="56521-158">หลังจากยืนยันแผนการใบสั่งที่มีการเชื่อมโยงความต้องการกับใบขอซื้อแล้ว กลไกจัดการการวางแผนจะรักษาการเชื่อมโยงความต้องการกับการจัดซื้อกับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="56521-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="56521-159">หากพบใบสั่งที่ยืนยันในภายหลังว่าขาดปริมาณบางอย่างซึ่งต้องใช้เติมใบขอซื้อ ระบบจะสร้างแผนการใบสั่งใหม่ให้กับผลต่าง</span><span class="sxs-lookup"><span data-stu-id="56521-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="56521-160">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับใบขอซื้อ โปรดดูที่ [ภาพรวมใบขอซื้อ](../../procurement/purchase-requisitions-overview.md)</span><span class="sxs-lookup"><span data-stu-id="56521-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]