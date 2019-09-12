---
title: กลุ่มใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการทำงานกับกลุ่มใบสั่งงานในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875925"
---
# <a name="work-order-pools"></a><span data-ttu-id="f0cfc-103">กลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f0cfc-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="f0cfc-104">คุณสามารถใช้กลุ่มใบสั่งงานเพื่อจัดกลุ่มใบสั่งงานที่มีบางอย่างร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="f0cfc-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="f0cfc-105">ตัวอย่างเช่น คุณสามารถสร้างกลุ่มใบสั่งงานสำหรับ</span><span class="sxs-lookup"><span data-stu-id="f0cfc-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="f0cfc-106">ทีมผู้ปฏิบัติงาน ตัวอย่างเช่น ทีมงานบำรุงรักษา A ทีมงานบำรุงรักษา B</span><span class="sxs-lookup"><span data-stu-id="f0cfc-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="f0cfc-107">ทักษะวิชาชีพ ตัวอย่างเช่น ช่างไฟฟ้า หรือช่างประปา</span><span class="sxs-lookup"><span data-stu-id="f0cfc-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="f0cfc-108">ที่ตั้งทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="f0cfc-108">physical locations</span></span>  

- <span data-ttu-id="f0cfc-109">กำหนดการเวลา ตัวอย่างเช่น สัปดาห์ หรือรอบระยะเวลาอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f0cfc-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="f0cfc-110">ถ้าจำเป็น คุณสามารถวางใบสั่งงานหนึ่งใบในกลุ่มใบสั่งงานหลายกลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="f0cfc-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="f0cfc-111">สร้างกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f0cfc-111">Create work order pool</span></span>

<span data-ttu-id="f0cfc-112">ใน **กลุ่มใบสั่งงานทั้งหมด** หรือ **กลุ่มใบสั่งงานที่ใช้งานอยู่** คุณสามารถดูภาพรวมของกลุ่มใบสั่งงานของคุณและสร้างกลุ่มใหม่</span><span class="sxs-lookup"><span data-stu-id="f0cfc-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="f0cfc-113">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **กลุ่มใบสั่งงาน** > **กลุ่มใบสั่งงานทั้งหมด** หรือ **กลุ่มใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="f0cfc-114">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-114">Click **New**.</span></span>

3. <span data-ttu-id="f0cfc-115">ใส่รหัสกลุ่มใบสั่งงานลงในฟิลด์ **กลุ่ม** และตั้งชื่อในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="f0cfc-116">เลือก "ใช่" บนปุ่มสลับ **กำลังใช้งานอยู่** เพื่อระบุว่ากลุ่มใบสั่งงานเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="f0cfc-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="f0cfc-117">เลือก "ใช่" บนปุ่มสลับ **ลบความสัมพันธ์ของใบสั่งงาน** ถ้าคุณต้องการให้ลบใบสั่งงานออกจากกลุ่มใบสั่งทำงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f0cfc-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="f0cfc-118">ในฟิลด์ **ลบสถานะการใช้** ให้เลือกสถานะการใช้ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f0cfc-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="f0cfc-119">ตัวอย่างเช่น สถานะการใช้ใบสั่งงานสำหรับการทำให้ใบสั่งงานเสร็จสมบูรณ์อาจถูกตั้งค่าให้ลบความสัมพันธ์กับกลุ่มใบสั่งงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f0cfc-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="f0cfc-120">คุณสามารถเริ่มต้นการเพิ่มใบสั่งงานให้กับกลุ่มใบสั่งงานของคุณได้ทันที</span><span class="sxs-lookup"><span data-stu-id="f0cfc-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="f0cfc-121">ในแท็บด่วน **ใบสั่งงาน** ให้คลิก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="f0cfc-122">เลือกใบสั่งงานในฟิลด์ **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="f0cfc-123">ฟิลด์ที่เกี่ยวข้องจะมีการอัพเดตโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f0cfc-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="f0cfc-124">ทำซ้ำขั้นตอนที่ 7-8 ถ้าคุณต้องการเพิ่มใบสั่งงานเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f0cfc-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="f0cfc-125">ในฟิลด์ **เรียงลำดับใบสั่ง** คุณสามารถระบุว่าใบสั่งงานควรมีการดำเนินการในใบสั่งหนึ่งๆ หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f0cfc-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="f0cfc-126">แทรกหมายเลข 1, 2, 3 และหมายเลขต่อๆ ไป เพื่อระบุลำดับเฉพาะสำหรับใบสั่งงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f0cfc-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="f0cfc-127">คลิกปุ่ม **ใบสั่งงาน** เพื่อดูรายการของใบสั่งงานทั้งหมดที่รวมอยู่ในกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f0cfc-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="f0cfc-128">คลิก **การใช้กำลังการผลิต** เพื่อเปิด **การใช้กำลังการผลิต** เพื่อคำนวณและดูการใช้กำลังการผลิตสำหรับกำหนดการบำรุงรักษา ใบสั่งงานที่ไม่ได้จัดกำหนดการ และใบสั่งงานที่จัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="f0cfc-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="f0cfc-129">คลิกปุ่ม **การคาดการณ์สินค้า** เพื่อเปิด **การคาดการณ์สินค้า** เพื่อคำนวณและดูการคาดการณ์สำหรับสินค้า (อะไหล่สำรองและสินค้าที่ต้องการอื่นๆ) ที่เกี่ยวข้องกับกำหนดการบำรุงรักษา ใบสั่งงานที่ไม่ได้จัดกำหนดการ และใบสั่งงานที่จัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="f0cfc-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="f0cfc-130">คลิกปุ่ม **ใบขอซื้อของใบสั่งงาน** เพื่อเปิดรายการ **ใบขอซื้อของใบสั่งงาน** เพื่อดูรายการใบขอซื้อที่เกี่ยวข้องกับใบสั่งงานในกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f0cfc-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="f0cfc-131">คลิกปุ่ม **การซื้อใบสั่งงาน** เพื่อเปิดรายการ **การซื้อใบสั่งงาน** เพื่อดูรายการสั่งซื้อที่เกี่ยวข้องกับใบสั่งงานในกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f0cfc-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="f0cfc-132">เมื่อกลุ่มใบสั่งงานไม่เกี่ยวข้องกับการวางแผนงานของคุณอีกต่อไป ตั้งค่ากล่องกาเครื่องหมาย **การใช้งานอยู่** สำหรับกลุ่มนั้นให้เป็น "ไม่" ในมุมมองรายการ **กลุ่มใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="f0cfc-133">เลือกกล่องกาเครื่องหมาย **ลบความสัมพันธ์ของใบสั่งงาน** ถ้าคุณต้องการลบรายการใบสั่งงานทั้งหมด ตัวอย่างเช่น ถ้าต้องการสร้างที่ว่างเปล่าซึ่งคุณสามารถใช้สำหรับใบสั่งงานอื่นๆ ได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="f0cfc-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="f0cfc-134">อย่าลืมยกเลิกกล่องกาเครื่องหมาย **ลบความสัมพันธ์ของกลุ่มใบสั่งงาน** ถ้าคุณต้องการใช้กลุ่มใบสั่งงานเพื่อสร้างความสัมพันธ์ของใบสั่งงานใหม่ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="f0cfc-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![รูปที่ 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="f0cfc-136">เพิ่มใบสั่งงานไปยังกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f0cfc-136">Add work order to a work order pool</span></span>

<span data-ttu-id="f0cfc-137">ตามที่อธิบายไว้ในส่วนด้านบน คุณสามารถเพิ่มใบสั่งงานให้กับกลุ่มใบสั่งงานได้เมื่อคุณสร้างกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f0cfc-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="f0cfc-138">นอกจากนี้คุณยังสามารถเพิ่มใบสั่งงานไปยังกลุ่มใบสั่งงานจากรายการ **ใบสั่งงานทั้งหมด** รายการใดรายการหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f0cfc-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="f0cfc-139">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f0cfc-140">เลือกใบสั่งงานในรายการ และคลิก **กลุ่มใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="f0cfc-141">เลือก "เพิ่ม" ในฟิลด์ **เพิ่ม/ลบ**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="f0cfc-142">เลือกกลุ่มใบสั่งงานในฟิลด์ **กลุ่มใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="f0cfc-143">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-143">Click **OK**.</span></span>

6. <span data-ttu-id="f0cfc-144">หลังจากที่คุณได้เพิ่มใบสั่งงานไปยังกลุ่มใบสั่งงานแล้ว ถ้าคุณต้องการวางใบสั่งงานไว้ในลำดับที่ระบุในกลุ่ม: ให้เปิดหน้ารายการกลุ่มใบสั่งงานหนึ่งหน้า เลือกกลุ่ม และคลิก **แก้ไข** แล้วปรับปรุงการเรียงลำดับของใบสั่งงานที่อยู่ในกลุ่มในฟอร์ม **กลุ่มใบสั่งงาน** > แท็บด่วน **ใบสั่งงาน** > ฟิลด์ **จัดเรียงใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="f0cfc-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="f0cfc-145">ถ้าคุณต้องการลบใบสั่งงานที่เลือกออกจากกลุ่มใบสั่งงาน ให้เลือก "ลบ" ในขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="f0cfc-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

