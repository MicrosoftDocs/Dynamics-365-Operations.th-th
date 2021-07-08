---
title: การปรับปรุงสินค้าคงคลังของคลังสินค้า
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับสมุดรายวันการปรับปรุงสินค้าคงคลังของคลังสินค้า และการประมวลผลเมื่อคุณใช้ scale unit
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1bf147ce430d84980516d8d4824081ee2a9321a2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271243"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="4a822-103">การปรับปรุงสินค้าคงคลังของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4a822-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a822-104">จะมีการใช้คุณลักษณะการปรับปรุงสินค้าคงคลังของคลังสินค้า เมื่อรัน scale unit ของระบบคลาวด์และ edge สำหรับ [ปริมาณงานการผลิต](cloud-edge-workload-manufacturing.md) และ [ปริมาณงานการจัดการคลังสินค้า](cloud-edge-workload-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="4a822-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="4a822-105">เมื่อผู้ปฏิบัติงานทำการปรับปรุงสินค้าคงคลังโดยใช้แอปคลังสินค้ากับปริมาณงานการจัดการคลังสินค้าของ scale unit การอัพเดตปริมาณคงคลังคงเหลือที่มีอยู่จริงต้องได้รับการประมวลผลโดยชุดงาน **สมุดรายวันการปรับปรุงสินค้าคงคลังในคลังสินค้า** ซึ่งคุณรันและจัดกำหนดการโดยไปที่ **การจัดการคลังสินค้า > งานประจำงวด > สมุดรายวันการปรับปรุงสินค้าคงคลังในคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4a822-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="4a822-106">กระบวนการงานของแอปคลังสินค้าต่อไปนี้ใช้ **สมุดรายวันการปรับปรุงสินค้าคงคลังของคลังสินค้า** ในปริมาณงานของ scale unit ในปัจจุบัน:</span><span class="sxs-lookup"><span data-stu-id="4a822-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="4a822-107">การปรับปรุงเข้า/ออก</span><span class="sxs-lookup"><span data-stu-id="4a822-107">Adjustment in/out</span></span>
- <span data-ttu-id="4a822-108">การตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="4a822-108">Cycle counting</span></span>
- <span data-ttu-id="4a822-109">กำลังโหลดป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="4a822-109">License plate loading</span></span>

<span data-ttu-id="4a822-110">ธุรกรรมของสินค้าคงคลังหลายรายการถูกสร้างขึ้นเป็นส่วนหนึ่งของกระบวนการปรับปรุงสินค้าคงคลังแต่ละกระบวนการ เนื่องจากการปรับใช้ฮับและ scale unit ใช้เรกคอร์ดสินค้าคงคลังร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="4a822-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="4a822-111">ตัวอย่างการปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4a822-111">Inventory adjustment example</span></span>

<span data-ttu-id="4a822-112">ในตัวอย่างนี้ ผู้ปฏิบัติงานคลังสินค้าใช้แอปคลังสินค้าเพื่อลงทะเบียนการเพิ่มปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="4a822-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="4a822-113">ขั้นแรก ปริมาณงานของ scale unit จะสร้างธุรกรรมการปรับปรุงสินค้าคงคลังของคลังสินค้าเพื่อการปรับปรุงทางกายภาพที่เป็นค่าบวก ซึ่งจากนั้นจะถูกซิงโครไนส์กับฮับและส่งผลให้ปริมาณคงคลังคงเหลือเพิ่มขึ้นบนฮับ</span><span class="sxs-lookup"><span data-stu-id="4a822-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="4a822-114">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4a822-114">Type</span></span>                                    | <span data-ttu-id="4a822-115">สเกลยูนิต</span><span class="sxs-lookup"><span data-stu-id="4a822-115">Scale unit</span></span> | <span data-ttu-id="4a822-116">ทิศทาง</span><span class="sxs-lookup"><span data-stu-id="4a822-116">Direction</span></span> | <span data-ttu-id="4a822-117">ฮับ</span><span class="sxs-lookup"><span data-stu-id="4a822-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="4a822-118">การปรับปรุงสินค้าคงคลังของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4a822-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="4a822-119">+1</span><span class="sxs-lookup"><span data-stu-id="4a822-119">+1</span></span>         | ->        | <span data-ttu-id="4a822-120">+1</span><span class="sxs-lookup"><span data-stu-id="4a822-120">+1</span></span>  |

<span data-ttu-id="4a822-121">จากนั้น ฮับจะประมวลผลการลงรายการบัญชีสมุดรายวันการตรวจนับ ซึ่งได้รับผ่าน [ข้อความตัวประมวลผลของข้อความ](cloud-edge-message-processor-messages.md)</span><span class="sxs-lookup"><span data-stu-id="4a822-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="4a822-122">นี่จะอัพเดตปริมาณคงคลังคงเหลือเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4a822-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="4a822-123">เพื่อป้องกันไม่ให้มีสินค้าคงคลังคงเหลือสองเท่า ฮับจะสร้างธุรกรรมออฟเซ็ตที่เป็นส่วนหนึ่งของกระบวนการนี้ และลบปริมาณคงคลังคงเหลือที่บันทึกไว้ก่อนหน้านี้ซึ่งเกี่ยวข้องกับการปรับปรุงสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4a822-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="4a822-124">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4a822-124">Type</span></span>                                    | <span data-ttu-id="4a822-125">สเกลยูนิต</span><span class="sxs-lookup"><span data-stu-id="4a822-125">Scale unit</span></span> | <span data-ttu-id="4a822-126">ทิศทาง</span><span class="sxs-lookup"><span data-stu-id="4a822-126">Direction</span></span> | <span data-ttu-id="4a822-127">ฮับ</span><span class="sxs-lookup"><span data-stu-id="4a822-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="4a822-128">การตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="4a822-128">Counting</span></span>                                | <span data-ttu-id="4a822-129">+1</span><span class="sxs-lookup"><span data-stu-id="4a822-129">+1</span></span>         | <-        | <span data-ttu-id="4a822-130">+1</span><span class="sxs-lookup"><span data-stu-id="4a822-130">+1</span></span>  |
| <span data-ttu-id="4a822-131">การปรับปรุงสินค้าคงคลังของคลังสินค้า (ออฟเซ็ต)</span><span class="sxs-lookup"><span data-stu-id="4a822-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="4a822-132">-1</span><span class="sxs-lookup"><span data-stu-id="4a822-132">-1</span></span>         | <-        | <span data-ttu-id="4a822-133">-1</span><span class="sxs-lookup"><span data-stu-id="4a822-133">-1</span></span>  |

<span data-ttu-id="4a822-134">เมื่อ scale unit สร้าง **สมุดรายวันการปรับปรุงสินค้าคงคลังของคลังสินค้า** บนฮับแล้ว คุณสามารถทบทวนทั้ง **สมุดรายวันการตรวจนับ** และ **สมุดรายวันออฟเซ็ต** ซึ่งสร้างขึ้นโดยฮับเป็นส่วนหนึ่งของกระบวนการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="4a822-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="4a822-135">คุณสามารถทบทวนรายการสมุดรายวันและธุรกรรมต่างๆ เหล่านี้ใน Supply Chain Management ได้โดยปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4a822-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="4a822-136">ลงชื่อเข้าใช้ใน scale unit</span><span class="sxs-lookup"><span data-stu-id="4a822-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="4a822-137">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> สมุดรายวันการปรับปรุงสินค้าคงคลังของคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4a822-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="4a822-138">บนหน้า **สมุดรายวันการปรับปรุงสินค้าคงคลังของคลังสินค้า** ให้ค้นหาและเปิดสมุดรายวันที่บันทึกการเปลี่ยนแปลงปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="4a822-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="4a822-139">ส่วน **บรรทัดสมุดรายวัน** แสดงการปรับปรุงแต่ละรายการที่บันทึกโดยสมุดรายวันนี้</span><span class="sxs-lookup"><span data-stu-id="4a822-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="4a822-140">ลงชื่อเข้าใช้ในฮับ</span><span class="sxs-lookup"><span data-stu-id="4a822-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="4a822-141">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> สมุดรายวันการปรับปรุงสินค้าคงคลังของคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4a822-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="4a822-142">บนหน้า **สมุดรายวันการปรับปรุงสินค้าคงคลังของคลังสินค้า** คุณควรจะเห็นสมุดรายวันเดียวกันที่แสดงรายการ หากฮับและ scale unit ซิงค์กัน</span><span class="sxs-lookup"><span data-stu-id="4a822-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="4a822-143">เปิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="4a822-143">Open the journal.</span></span> <span data-ttu-id="4a822-144">ถ้า [ข้อความตัวประมวลผลของข้อความ](cloud-edge-message-processor-messages.md) ถูกประมวลผลแล้ว คุณจะเห็นลิงค์ไปที่ **สมุดรายวันการตรวจนับ** และ **สมุดรายวันออฟเซ็ต** ในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="4a822-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="4a822-145">**สมุดรายวันการตรวจนับ** ควรแสดงค่ามิติเดียวกันกับบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="4a822-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="4a822-146">**สมุดรายวันออฟเซ็ต** ควรแสดงออฟเซ็ต ซึ่งจะลบการปรับปรุงสินค้าคงคลังสองเท่า</span><span class="sxs-lookup"><span data-stu-id="4a822-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="4a822-147">เมื่อการซิงค์และการประมวลผลทั้งหมดเสร็จสมบูรณ์ **สมุดรายวันการตรวจนับ** และ **สมุดรายวันออฟเซ็ต** จะถูกซิงค์กลับไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="4a822-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="4a822-148">นอกจากนี้ คุณยังสามารถดูรายการเหล่านี้ได้จากหน้า **สมุดรายวันการปรับปรุงสินค้าคงคลังของคลังสินค้า** ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4a822-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
