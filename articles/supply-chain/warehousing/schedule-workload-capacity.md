---
title: จัดกำหนดการกำลังการผลิตปริมาณงาน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและการจัดกำหนดการกำลังการผลิตปริมาณงาน สำหรับผู้ปฏิบัติงานในคลังสินค้า หรือสำหรับคลังสินค้าทั้งหมด
author: MarkusFogelberg
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2458009dabd71e6c8423e8e607a0cedb4765b88
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817352"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="7d107-103">จัดกำหนดการกำลังการผลิตปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="7d107-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7d107-104">คุณสามารถจัดกำหนดการกำลังการผลิตปริมาณงานสำหรับคลังสินค้า และคุณยังสามารถคาดปริมาณงานปัจจุบันและในอนาคต สำหรับผู้ปฏิบัติงานในคลังสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="7d107-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="7d107-105">คุณสามารถคาดปริมาณงานสำหรับคลังสินค้าทั้งหมด หรือคุณสามารถคาดปริมาณงานแบบแยกต่างหากได้ สำหรับปริมาณงานขาเข้าและขาออก</span><span class="sxs-lookup"><span data-stu-id="7d107-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="7d107-106">เมื่อต้องการคาดการณ์ผลผลิตปริมาณงานสำหรับคลังสินค้าที่เลือก ข้อมูลการจัดกำหนดการหลักต้องพร้อมใช้งานสำหรับคลังสินค้าเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="7d107-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="7d107-107">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมแผนหลัก](../master-planning/master-plans.md)</span><span class="sxs-lookup"><span data-stu-id="7d107-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="7d107-108">กำหนดการและดูปริมาณงานสำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7d107-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="7d107-109">ในการจัดกำหนดการกำลังการผลิตปริมาณงานสำหรับคลังสินค้า คุณสร้างการตั้งค่าปริมาณงานสำหรับคลังสินค้าหนึ่งรายการขึ้นไป และจากนั้น เชื่อมโยงการตั้งค่าปริมาณงานกับแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="7d107-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="7d107-110">ในการตั้งค่ากำลังการผลิตปริมาณงาน คุณสามารถกำหนดขีดจำกัดสำหรับน้ำหนักหรือปริมาตร สำหรับธุรกรรมขาเข้าและขาออก</span><span class="sxs-lookup"><span data-stu-id="7d107-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="7d107-111">คุณยังสามารถสร้างการตั้งค่ามากกว่าหนึ่งรายการได้สำหรับคลังสินค้าแต่ละรายการ และจากนั้น เชื่อมโยงการตั้งค่าด้วยแต่ละแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="7d107-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="7d107-112">ตัวอย่างเช่น คุณอาจใช้วิธีการนี้เพื่อรองรับการเปลี่ยนแปลงตามฤดูกาลในบุคลากร</span><span class="sxs-lookup"><span data-stu-id="7d107-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="7d107-113">ถ้าผู้ปฏิบัติงานสำหรับงานคลังสินค้าที่มีธุรกรรมสำหรับทั้งปริมาณงานขาเข้าและขาออก คุณสามารถตั้งค่าคอนฟิกการตั้งค่ากำลังการผลิตของคลังสินค้าได้ เพื่อให้มีการคาดปริมาณงานในมุมมองแบบรวม</span><span class="sxs-lookup"><span data-stu-id="7d107-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="7d107-114">เมื่อต้องการจัดกำหนดการ และดูปริมาณงานสำหรับคลังสินค้า คุณต้องทำงานต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="7d107-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="7d107-115">สร้างการตั้งค่ากำลังการผลิตปริมาณงาน และกำหนดขีดจำกัดกำลังการผลิตปริมาณงานสำหรับคลังสินค้าหนึ่งรายการ ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="7d107-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="7d107-116">เชื่อมโยงการตั้งค่ากำลังการผลิตปริมาณงานกับแผนหลัก เพื่อสร้างการคาดการณ์ปริมาณงาน และระบุระยะเวลาการคาดการณ์เหล่านั้นที่จะนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="7d107-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="7d107-117">สร้างการตั้งค่ากำลังการผลิตปริมาณงานสำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7d107-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="7d107-118">เลือก **การบริหารสินค้าคงคลัง** \> **ตั้งค่า** \> **การตรวจสอบคลังสินค้า** \> **กำลังการผลิตปริมาณงาน**</span><span class="sxs-lookup"><span data-stu-id="7d107-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="7d107-119">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างการตั้งค่ากำลังการผลิตปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="7d107-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="7d107-120">บน FastTab **คลังสินค้า** เลือก **สร้าง** และจากนั้น ป้อนค่าในรายการเพื่อเชื่อมโยงคลังสินค้ากับการตั้งค่ากำลังการผลิตปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="7d107-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="7d107-121">เลือกกล่องกาเครื่องหมาย **ปริมาณงานขาเข้าและขาออกแบบรวม** ถ้ารายงาน **กำลังการผลิตปริมาณงาน** ควรแสดงปริมาณงานรวมสำหรับธุรกรรมขาเข้าและขาออกในมุมมองเดียว</span><span class="sxs-lookup"><span data-stu-id="7d107-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="7d107-122">บน FastTab **ชนิดธุรกรรม** เลือกชนิดของธุรกรรมขาเข้าและขาออกที่มีการนำขีดจำกัดปริมาณงานไปใช้</span><span class="sxs-lookup"><span data-stu-id="7d107-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d107-123">คุณต้องเลือกชนิดธุรกรรมอย่างน้อยหนึ่งชนิด สำหรับทั้งปริมาณงานขาเข้าและปริมาณงานขาออก</span><span class="sxs-lookup"><span data-stu-id="7d107-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="7d107-124">กำหนดขีดจำกัดสำหรับน้ำหนักหรือปริมาตร</span><span class="sxs-lookup"><span data-stu-id="7d107-124">Define limits for volume or weight</span></span>

<span data-ttu-id="7d107-125">คุณสามารถตั้งค่าขีดจำกัดสำหรับน้ำหนักหรือปริมาตรได้ โดยขึ้นอยู่กับการจำกัดที่เกี่ยวข้องสำหรับปริมาณงานสำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7d107-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="7d107-126">ขีดจำกัดที่คุณระบุถูกรวมอยู่ในการวางแผนกำลังการผลิตปริมาณงานที่คุณสามารถดูได้บนรายงาน **กำลังการผลิตปริมาณงาน**</span><span class="sxs-lookup"><span data-stu-id="7d107-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="7d107-127">เพื่อคาดการณ์ข้อมูลเกี่ยวกับปริมาตรและน้ำหนักสำหรับสินค้า ปริมาณมาตรฐานของสินค้าคงคลังหนึ่งรายการและน้ำหนักของสินค้าคงคลังหนึ่งรายการ ต้องถูกระบุสำหรับผลิตภัณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7d107-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="7d107-128">ฟิลด์ที่จำเป็นมีอยู่ในกลุ่มฟิลด์ต่อไปนี้ใน FastTab **จัดการสินค้าคงคลัง** ของหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้** :</span><span class="sxs-lookup"><span data-stu-id="7d107-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="7d107-129">การจัดการ</span><span class="sxs-lookup"><span data-stu-id="7d107-129">Handling</span></span>
- <span data-ttu-id="7d107-130">มิติทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="7d107-130">Physical dimensions</span></span>
- <span data-ttu-id="7d107-131">การวัดน้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="7d107-131">Weight measurements</span></span>

<span data-ttu-id="7d107-132">ถ้าข้อมูลนี้ไม่ได้ถูกระบุอย่างถูกต้อง คุณจะได้รับข้อความ เมื่อคุณสร้างรายงาน **กำลังการผลิตปริมาณงาน**</span><span class="sxs-lookup"><span data-stu-id="7d107-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="7d107-133">จากรายงาน คุณจึงสามารถดูรายละเอียดแนวลึกเพื่อระบุข้อมูลที่ขาดหายไปที่จำเป็นได้ เพื่อที่จะคาดการณ์ปริมาณงานในอนาคต</span><span class="sxs-lookup"><span data-stu-id="7d107-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="7d107-134">เชื่อมโยงการตั้งค่ากำลังการผลิตปริมาณงานกับแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="7d107-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="7d107-135">เลือก **การบริหารสินค้าคงคลัง** \> **งานประจำงวด** \> **จัดกำหนดการปริมาณงาน**</span><span class="sxs-lookup"><span data-stu-id="7d107-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="7d107-136">ในฟิลด์ **แผนหลัก** เลือกแผนหลักที่จะใช้สำหรับการคาดการณ์ปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="7d107-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="7d107-137">ในฟิลด์ **จำนวนวัน** ระบุจำนวนวันที่การคาดการณ์ปริมาณงานครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="7d107-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="7d107-138">ในฟิลด์ **ปริมาณงาน** เลือกการตั้งค่าปริมาณงานเพื่อเชื่อมโยงกับแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="7d107-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="7d107-139">ดูกำลังการผลิตปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="7d107-139">View workload capacity</span></span>

1. <span data-ttu-id="7d107-140">เลือก **การบริหารสินค้าคงคลัง** \> **การสอบถามและรายงาน** \> **รายงานสินค้าคงคลังทางกายภาพ** \> **กำลังการผลิตปริมาณงาน**</span><span class="sxs-lookup"><span data-stu-id="7d107-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="7d107-141">ในฟิลด์ **จำนวนของคอลัมน์** ระบุจำนวนของคอลัมน์ที่จะแสดงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="7d107-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="7d107-142">ในฟิลด์ **ชนิดใบสั่ง** เลือก **วางแผนและยืนยันแล้ว** **วางแผนแล้ว** หรือ **ยืนยันแล้ว** เพื่อบ่งชี้ชนิดของใบสั่งให้กับโครงการในรายงาน</span><span class="sxs-lookup"><span data-stu-id="7d107-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="7d107-143">ในฟิลด์ **ชนิดการวางสินค้า** เลือกชนิดการวางสินค้าเพื่อบ่งชี้ว่า ควรคาดการณ์กำลังการผลิตปริมาณงานสำหรับปริมาตรหรือน้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="7d107-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="7d107-144">ในฟิลด์ **กำลังการผลิตปริมาณงาน** เลือกการตั้งค่ากำลังการผลิตปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="7d107-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]