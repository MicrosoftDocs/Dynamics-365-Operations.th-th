---
title: เปลี่ยนกลุ่มงานในงาน
description: หัวข้อนี้จะอธิบายวิธีการที่คุณสามารถใช้ปุ่มเปลี่ยนกลุ่มงานสำหรับรายการงาน เพื่อเปลี่ยนกลุ่มงานของงานที่มีอยู่
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001160"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="38e2e-103">เปลี่ยนกลุ่มงานในงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38e2e-104">คุณสามารถใช้กลุ่มงานเพื่อจัดระเบียบงานเป็นกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="38e2e-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="38e2e-105">ตัวอย่างเช่น คุณสามารถสร้างกลุ่มงานเพื่อจำแนกประเภทการงานที่เกิดขึ้นในที่ตั้งคลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="38e2e-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="38e2e-106">คุณลักษณะ *เปลี่ยนกลุ่มงานในงาน* จะเพิ่มปุ่ม **เปลี่ยนกลุ่มงาน** ไปยังบานหน้าต่างการดำเนินการของรายการงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="38e2e-107">ดังนั้น ผู้จัดการคลังสินค้าสามารถเปลี่ยนกลุ่มงานของงานที่มีอยู่ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="38e2e-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="38e2e-108">คุณลักษณะนี้จะช่วยให้ผู้จัดการสามารถตอบสนองต่อการเปลี่ยนแปลงในการผลิตในคลังสินค้าได้อย่างรวดเร็ว และจะช่วยปรับปรุงความสามารถในการปรับตัวต่อสถานการณ์ที่เปลี่ยนแปลงและความต้องการถ่ายโอนงานให้กับกลุ่มงานอื่น</span><span class="sxs-lookup"><span data-stu-id="38e2e-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="38e2e-109">เปิดใช้งานคุณลักษณะเปลี่ยนแปลงกลุ่มงานในงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="38e2e-110">ก่อนที่คุณจะเริ่มต้นการตั้งค่าหรือใช้คุณลักษณะนี้ คุณต้องตรวจสอบให้แน่ใจว่าพร้อมใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="38e2e-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="38e2e-111">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="38e2e-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="38e2e-112">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="38e2e-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="38e2e-113">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="38e2e-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="38e2e-114">**ชื่อคุณลักษณะ:** *เปลี่ยนแปลงกลุ่มงานในงาน*</span><span class="sxs-lookup"><span data-stu-id="38e2e-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="38e2e-115">ตั้งค่าคุณลักษณะเปลี่ยนแปลงกลุ่มงานในงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="38e2e-116">เมื่อต้องการใช้คุณลักษณะนี้ คุณต้องมีการตั้งค่ากลุ่มงานบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="38e2e-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="38e2e-117">นอกจากนี้ คุณยังอาจตั้งค่าเท็มเพลตงานของคุณเพื่อให้กำหนดกลุ่มโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="38e2e-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="38e2e-118">ถ้าคุณต้องการทำงานผ่านสถานการณ์จำลองตัวอย่างที่ระบุไว้ในภายหลังในหัวข้อนี้ ให้ตั้งค่าระบบของคุณตามที่อธิบายไว้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="38e2e-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="38e2e-119">ตั้งค่ากลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-119">Set up work pools</span></span>

<span data-ttu-id="38e2e-120">กลุ่มงานช่วยให้คุณสามารถจัดระเบียบรายการงานตามชนิดได้</span><span class="sxs-lookup"><span data-stu-id="38e2e-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="38e2e-121">เมื่อต้องการทำงานกับคุณลักษณะ *เปลี่ยนแปลงกลุ่มงานในงาน* คุณต้องมีอย่างน้อยสองกลุ่มงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="38e2e-122">เพื่อดูและเพิ่มกลุ่มงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="38e2e-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="38e2e-123">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> กลุ่มงาน**</span><span class="sxs-lookup"><span data-stu-id="38e2e-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="38e2e-124">ถ้าคุณกำลังทำงานกับข้อมูลสาธิตจากบริษัท **USMF** และจะทำงานผ่านสถานการณ์จำลองตัวอย่างในภายหลังในหัวข้อนี้ ให้เพิ่มกลุ่มงานสองกลุ่มที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="38e2e-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="38e2e-125">กลุ่มงานที่ 1:</span><span class="sxs-lookup"><span data-stu-id="38e2e-125">Work pool 1:</span></span>

        - <span data-ttu-id="38e2e-126">**รหัสกลุ่มงาน:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="38e2e-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="38e2e-127">**คำอธิบาย:** *Web Shop*</span><span class="sxs-lookup"><span data-stu-id="38e2e-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="38e2e-128">กลุ่มงานที่ 2:</span><span class="sxs-lookup"><span data-stu-id="38e2e-128">Work pool 2:</span></span>

        - <span data-ttu-id="38e2e-129">**รหัสกลุ่มงาน:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="38e2e-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="38e2e-130">**คำอธิบาย:** *ศูนย์บริการ*</span><span class="sxs-lookup"><span data-stu-id="38e2e-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="38e2e-131">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="38e2e-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="38e2e-132">ตั้งค่าเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-132">Set up work templates</span></span>

<span data-ttu-id="38e2e-133">สำหรับเท็มเพลตงานของคุณแต่ละเท็มเพลต คุณสามารถตั้งค่ากลุ่มงานเริ่มต้นได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="38e2e-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="38e2e-134">สำหรับเท็มเพลตที่เกี่ยวข้องแต่ละเท็มเพลต คุณจะกำหนดกลุ่มงานในคอลัมน์ **รหัสกลุ่มงาน**</span><span class="sxs-lookup"><span data-stu-id="38e2e-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="38e2e-135">ในกรณีนี้ รายการงานทั้งหมดที่สร้างขึ้นโดยใช้เท็มเพลตที่กำหนดจะสืบทอดกลุ่มงานที่กำหนดให้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="38e2e-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="38e2e-136">ถ้าคุณกำลังทำงานกับข้อมูลสาธิตจากบริษัท **USMF** และจะทำงานผ่านสถานการณ์จำลองตัวอย่างในภายหลังในหัวข้อนี้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="38e2e-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="38e2e-137">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="38e2e-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="38e2e-138">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไข** เพื่อเปลี่ยนหน้าไปยังโหมดการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="38e2e-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="38e2e-139">แก้ไขเท็มเพลตได้โดยการตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="38e2e-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="38e2e-140">**เท็มเพลตงาน:** *62 เบิกสินค้าไปแพค*</span><span class="sxs-lookup"><span data-stu-id="38e2e-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="38e2e-141">**รหัสกลุ่มงาน:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="38e2e-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="38e2e-142">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="38e2e-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="38e2e-143">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="38e2e-143">Example scenario</span></span>

<span data-ttu-id="38e2e-144">สถานการณ์นี้แสดงวิธีการเปลี่ยนสตรีมของการประมวลผลสำหรับรายการงานที่มีอยู่ด้วยการเปลี่ยนกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="38e2e-145">ซึ่งใช้ข้อมูลสาธิตจากบริษัท **USMF** และการตั้งค่าที่แนะนำก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="38e2e-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="38e2e-146">สร้างใบสั่งขายและนำใบสั่งขายออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="38e2e-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="38e2e-147">ยืนยันว่ามีปริมาณคงคลังคงเหลือเพียงพอสำหรับสินค้า *A0001* และ *A0002* ในคลังสินค้า *62*</span><span class="sxs-lookup"><span data-stu-id="38e2e-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="38e2e-148">ไปที่ **การบริหารสินค้าคงคลัง \> การสอบถามและรายงาน \> รายการปริมาณคงคลังคงเหลือ** และแก้ไขตัวกรองข้อมูลดังที่แสดงไว้ที่นี่:</span><span class="sxs-lookup"><span data-stu-id="38e2e-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="38e2e-149">ค่า **คลังสินค้า** เริ่มต้นด้วย *62*</span><span class="sxs-lookup"><span data-stu-id="38e2e-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="38e2e-150">ค่า **หมายเลขสินค้า** เป็น *A001* หรือ *A002*</span><span class="sxs-lookup"><span data-stu-id="38e2e-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="38e2e-151">ข้อมูลสาธิตแต่ละรายการควรมีปริมาณเท่ากับ 10</span><span class="sxs-lookup"><span data-stu-id="38e2e-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="38e2e-152">ถัดไป คุณต้องสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="38e2e-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="38e2e-153">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="38e2e-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="38e2e-154">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="38e2e-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="38e2e-155">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="38e2e-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="38e2e-156">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="38e2e-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="38e2e-157">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="38e2e-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="38e2e-158">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="38e2e-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="38e2e-159">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="38e2e-159">The new sales order is opened.</span></span> <span data-ttu-id="38e2e-160">ฟิลด์นี้ควรมีบรรทัดใหม่ว่างเปล่าในกริดบนแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="38e2e-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="38e2e-161">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="38e2e-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="38e2e-162">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="38e2e-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="38e2e-163">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="38e2e-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="38e2e-164">บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="38e2e-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="38e2e-165">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="38e2e-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="38e2e-166">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="38e2e-166">Close the page.</span></span>
1. <span data-ttu-id="38e2e-167">บน FastTab **บรรทัดใบสั่งขาย** ให้เลือก **เพิ่มบรรทัด** เพื่อเพิ่มอีกบรรทัดหนึ่งไปยังใบสั่งขายของคุณ</span><span class="sxs-lookup"><span data-stu-id="38e2e-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="38e2e-168">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="38e2e-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="38e2e-169">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="38e2e-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="38e2e-170">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="38e2e-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="38e2e-171">บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="38e2e-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="38e2e-172">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="38e2e-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="38e2e-173">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="38e2e-173">Close the page.</span></span>
1. <span data-ttu-id="38e2e-174">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="38e2e-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="38e2e-175">คุณได้รับข้อความที่ให้ข้อมูลที่แสดงรหัสเวฟและรหัสการจัดส่งที่สร้างขึ้นจากการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="38e2e-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="38e2e-176">จดบันทึกรหัสเวฟ</span><span class="sxs-lookup"><span data-stu-id="38e2e-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="38e2e-177">รีวิวเวฟขาออก</span><span class="sxs-lookup"><span data-stu-id="38e2e-177">Review the outbound wave</span></span>

1. <span data-ttu-id="38e2e-178">ไปที่ **การจัดการคลังสินค้า \> เวฟขาออก \> เวฟการจัดส่ง \> เวฟทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="38e2e-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="38e2e-179">ในกริด ค้นหารหัสเวฟที่สร้างจากการนำออกใช้ของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="38e2e-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="38e2e-180">เลือกรหัสเวฟเพื่อดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="38e2e-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="38e2e-181">บน FastTab **รายการเวฟ** ตรวจสอบให้แน่ใจว่ามีการแสดงรหัสการจัดส่งสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="38e2e-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="38e2e-182">ถ้ามีการตั้งค่าตัวเลือก **ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า** เป็น *ไม่* ในการตั้งค่าสำหรับเท็มเพลตเวฟการจัดส่ง คุณต้องประมวลผลเวฟด้วยตนเองโดยการเลือก **ประมวลผล** จากแท็บ **เวฟ** บนบานหน้าต่างการดำเนินการเพื่อสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="38e2e-183">ตรวจสอบให้แน่ใจว่าได้มีการประมวลผลเวฟแล้ว</span><span class="sxs-lookup"><span data-stu-id="38e2e-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="38e2e-184">การประมวลผลนี้สร้างงานที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="38e2e-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="38e2e-185">ดูรายละเอียดงานและเปลี่ยนกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-185">View work details and change the work pool</span></span>

<span data-ttu-id="38e2e-186">คุณสามารถใช้หน้า **รายละเอียดงาน** เพื่อดูงานที่สร้างขึ้น และจัดการกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="38e2e-187">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="38e2e-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="38e2e-188">เลือกแถวสำหรับงานที่เพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="38e2e-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="38e2e-189">คอลัมน์ **หมายเลขใบสั่ง** จะแสดงหมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="38e2e-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="38e2e-190">ฟิลด์ **รหัสกลุ่มงาน** จะถูกตั้งค่าเป็นรหัสกลุ่มงานที่มีการตั้งค่าในเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="38e2e-191">ถ้าคุณไม่เห็นฟิลด์ **รหัสกลุ่มงาน** ให้เพิ่มคอลัมน์ลงในกริด แล้วจากนั้น รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="38e2e-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="38e2e-192">เมื่อต้องการเปลี่ยนกลุ่มงานที่สัมพันธ์กับรหัสงาน บนบานหน้าต่างการดำเนินการ บนแท็บ **งาน** ให้เลือก **เปลี่ยนรหัสกลุ่มงาน**</span><span class="sxs-lookup"><span data-stu-id="38e2e-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="38e2e-193">ในกล่องโต้ตอบ **เปลี่ยนกลุ่มงาน** บน FastTab **พารามิเตอร์** ในฟิลด์ **รหัสกลุ่มงาน** ให้เลือก *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="38e2e-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="38e2e-194">เลือก **ตกลง** เพื่อใช้การเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="38e2e-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="38e2e-195">โปรดสังเกตว่า ในขณะนี้มีการเปลี่ยนแปลงค่าของฟิลด์ **รหัสกลุ่มงาน** เป็น *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="38e2e-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38e2e-196">เมื่อกล่องโต้ตอบ **เปลี่ยนกลุ่มงาน** ปรากฏขึ้น ฟิลด์ **รหัสกลุ่มงาน** อาจว่างเปล่าตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="38e2e-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="38e2e-197">ถ้าฟิลด์นี้ว่างเปล่า เมื่อคุณเลือก **ตกลง** เพื่อใช้การเปลี่ยนแปลง คุณจะลบกลุ่มงานทั้งหมดออกจากงาน</span><span class="sxs-lookup"><span data-stu-id="38e2e-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="38e2e-198">นอกจากการสลับกลุ่มงานแล้ว คุณสามารถใช้กระบวนงานนี้เพื่อเพิ่มกลุ่มงานไปยังรายการงานใดๆ ที่ไม่มีกลุ่มงาน หรือลบกลุ่มงานออกจากรายการงานใดๆ ที่มีกลุ่มงานอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="38e2e-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
