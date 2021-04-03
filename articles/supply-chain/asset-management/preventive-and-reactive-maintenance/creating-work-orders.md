---
title: การสร้างใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งงานในการจัดการสินทรัพย์
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 76306fb31e7e5297e6a5d64b97b5bd09b64349ee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500585"
---
# <a name="creating-work-orders"></a><span data-ttu-id="9dc53-103">การสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="9dc53-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9dc53-104">หลังจากที่คุณได้จัดกำหนดการงานการบำรุงรักษาเชิงป้องกัน ขั้นตอนต่อไปคือ สร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="9dc53-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="9dc53-105">คุณสามารถขั้นตอนนี้ให้เสร็จสมบูรณ์ได้โดยใช้หนึ่งในกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9dc53-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="9dc53-106">งานที่จัดกำหนดการไว้ในกำหนดการบำรุงรักษาอาจมีชนิดข้อมูลอ้างอิงที่แตกต่างกัน ตามที่อธิบายไว้ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9dc53-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="9dc53-107">ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="9dc53-107">Reference type</span></span> | <span data-ttu-id="9dc53-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9dc53-108">Description</span></span> |
|---|---|
| <span data-ttu-id="9dc53-109">แผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9dc53-109">Maintenance plans</span></span> | <span data-ttu-id="9dc53-110">งานบำรุงรักษาเชิงป้องกันที่ยึดตามชนิดของแผนการบำรุงรักษา *เวลา* หรือ *ตัวนับ*</span><span class="sxs-lookup"><span data-stu-id="9dc53-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="9dc53-111">รอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9dc53-111">Maintenance rounds</span></span> | <span data-ttu-id="9dc53-112">งานบำรุงรักษาเชิงป้องกันที่มีสินทรัพย์หลายอย่างที่จำเป็นต้องมีชนิดของการบำรุงรักษาที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="9dc53-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="9dc53-113">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9dc53-113">Maintenance request</span></span> | <span data-ttu-id="9dc53-114">การร้องขอการบํารุงรักษาหรือการซ่อมแซมสินทรัพย์ที่สร้างขึ้นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9dc53-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="9dc53-115">การร้องขอนี้สามารถแปลงเป็นใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="9dc53-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="9dc53-116">สร้างใบสั่งงานตามกำหนดการบำรุงรักษาของคุณ</span><span class="sxs-lookup"><span data-stu-id="9dc53-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="9dc53-117">เมื่อต้องการสร้างใบสั่งงานที่ขึ้นอยู่กับกำหนดการบำรุงรักษาของคุณ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9dc53-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="9dc53-118">เปิดหนึ่งในหน้าต่อไปนี้ โดยขึ้นอยู่กับวิธีที่คุณต้องการเลือกสินค้าในกำหนดการสำหรับใบสั่งงานของคุณ:</span><span class="sxs-lookup"><span data-stu-id="9dc53-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="9dc53-119">กำหนดการบำรุงรักษาทั้งหมด (**การจัดการสินทรัพย์ \> กำหนดการจัดการ \> กำหนดการบํารุงรักษาทั้งหมด**)</span><span class="sxs-lookup"><span data-stu-id="9dc53-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="9dc53-120">เปิดรายการกำหนดการบำรุงรักษา (**การจัดการสินทรัพย์ \> กำหนดการจัดการ \> เปิดรายการกำหนดการบํารุงรักษา**)</span><span class="sxs-lookup"><span data-stu-id="9dc53-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="9dc53-121">เปิดกลุ่มกำหนดการบำรุงรักษา (**การจัดการสินทรัพย์ \> กำหนดการจัดการ \> เปิดกลุ่มกำหนดการบํารุงรักษา**)</span><span class="sxs-lookup"><span data-stu-id="9dc53-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="9dc53-122">ในกริด ให้เลือกกล่องกาเครื่องหมายสำหรับงานบํารุงรักษาที่จัดกำหนดการไว้ทั้งหมดที่คุณต้องการสร้างใบสั่งงานให้</span><span class="sxs-lookup"><span data-stu-id="9dc53-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="9dc53-123">จากนั้น ในบานหน้าต่างการดำเนินการ เลือก **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="9dc53-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="9dc53-124">ในกล่องโต้ตอบ **สร้างใบสั่งงาน** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="9dc53-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="9dc53-125">ในฟิลด์ **ชั่วโมงการคาดการณ์ในการบำรุงรักษา** แสดงจำนวนรวมของชั่วโมงที่คาดการณ์สำหรับรายการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9dc53-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![กล่องโต้ตอบสร้างใบสั่งงาน](media/18-preventive-maintenance.png)

1. <span data-ttu-id="9dc53-127">ในส่วน **พารามิเตอร์** ให้ระบุจํานวนของใบสั่งงานที่ควรจะสร้าง</span><span class="sxs-lookup"><span data-stu-id="9dc53-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="9dc53-128">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9dc53-128">Select one of the following options:</span></span>

    - <span data-ttu-id="9dc53-129">**ใบสั่งงานหนึ่งใบต่อรายการ** – สร้างใบสั่งงานหนึ่งใบต่อรายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9dc53-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="9dc53-130">**ใบสั่งงานหนึ่งใบต่อ** – สร้างใบสั่งงานที่มีการจัดกลุ่มตามการตั้งค่าของตัวเลือกอื่นๆ ที่จะพร้อมใช้งาน เมื่อคุณเลือกตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="9dc53-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="9dc53-131">ในฟิลด์ **ชนิดใบสั่งงาน** ให้เลือกชนิดใบสั่งงานที่จะใช้สำหรับใบสั่งงานทั้งหมดที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="9dc53-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="9dc53-132">เลือก **ตกลง** เพื่อสร้างใบสั่งงานตามการตั้งค่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="9dc53-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="9dc53-133">จัดกลุ่มรายการใบสั่งงานที่สร้างโดยอัตโนมัติ ในขณะที่รันแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9dc53-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="9dc53-134">คุณลักษณะนี้จะช่วยให้คุณสามารถกําหนดกฎสำหรับการจัดกลุ่มรายการใบสั่งงานภายใต้ใบสั่งงานหนึ่งๆ เมื่อมีการตั้งค่าระบบให้สร้างใบสั่งงานโดยอัตโนมัติ โดยยึดตามแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9dc53-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="9dc53-135">ก่อนหน้านี้ ใบสั่งงานที่สร้างโดยอัตโนมัติสามารถมีรายการได้เพียงรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="9dc53-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="9dc53-136">อย่างไรก็ตาม ขณะนี้คุณสามารถจัดกลุ่มใบสั่งงานตาม ตัวอย่างเช่น สินทรัพย์ ชนิดสินทรัพย์ หรือตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="9dc53-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="9dc53-137">(สามารถจัดกลุ่มใบสั่งงานที่สร้างขึ้นด้วยตนเองด้วยวิธีนี้ได้ ตามที่อธิบายไว้ในส่วนก่อนหน้านี้ของหัวข้อนี้)</span><span class="sxs-lookup"><span data-stu-id="9dc53-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="9dc53-138">เปิดใช้งานการจัดกลุ่มสำหรับใบสั่งงานที่สร้างโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9dc53-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="9dc53-139">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="9dc53-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="9dc53-140">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9dc53-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="9dc53-141">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9dc53-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9dc53-142">**โมดูล:** *การจัดการสินทรัพย์*</span><span class="sxs-lookup"><span data-stu-id="9dc53-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="9dc53-143">**ชื่อคุณลักษณะ:** *(พรีวิว) ใช้กฎสำหรับการจัดกลุ่มใบสั่งงาน ในขณะที่รันแผนการบำรุงรักษา*</span><span class="sxs-lookup"><span data-stu-id="9dc53-143">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="9dc53-144">ตั้งค่าการจัดกลุ่มสำหรับใบสั่งงานที่สร้างโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9dc53-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="9dc53-145">เพื่อตั้งค่าการจัดกลุ่มสำหรับใบสั่งงานที่สร้างโดยอัตโนมัติ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9dc53-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="9dc53-146">ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> การบำรุงรักษาเชิงป้องกัน \> แผนการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="9dc53-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="9dc53-147">สำหรับแต่ละแผนที่คุณต้องการสร้างใบสั่งงานที่จัดกลุ่ม ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9dc53-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="9dc53-148">เลือกแผนในบานหน้าต่างรายการ</span><span class="sxs-lookup"><span data-stu-id="9dc53-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="9dc53-149">บน FastTab **รายการ** ให้ตรวจสอบให้แน่ใจว่าได้เลือกกล่องกาเครื่องหมาย **สร้างอัตโนมัติ** ในทุกรายการ</span><span class="sxs-lookup"><span data-stu-id="9dc53-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="9dc53-150">ไปที่ **การจัดการสินทรัพย์ \> ประจำงวด \> การบำรุงรักษาเชิงป้องกัน \> จัดกำหนดการแผนการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="9dc53-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="9dc53-151">ในกล่องโต้ตอบ **จัดกำหนดการแผนการบํารุงรักษา** ในส่วน **รอบระยะเวลา** ให้ระบุระดับเวลาสำหรับแผน (ล่วงหน้าแค่ไหนเมื่อค้นหางานบำรุงรักษาที่จัดกำหนดการเพื่อสร้างงานให้)</span><span class="sxs-lookup"><span data-stu-id="9dc53-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="9dc53-152">ตั้งค่าตัวเลือก **สร้างใบสั่งงานจากกำหนดการโดยอัตโนมัติ** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="9dc53-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="9dc53-153">ในส่วน **ใบสั่งงาน** ให้เลือกตัวเลือกอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9dc53-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="9dc53-154">**ใบสั่งงานหนึ่งใบต่อรายการ** – สร้างใบสั่งงานหนึ่งใบต่อรายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9dc53-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="9dc53-155">(ตัวเลือกนี้จะมีฟังก์ชันเดียวกันที่พร้อมใช้งานเมื่อคุณลักษณะ *ใช้กฎสำหรับการจัดกลุ่มใบสั่งงาน ในขณะที่รันแผนการบำรุงรักษา* ถูกปิด)</span><span class="sxs-lookup"><span data-stu-id="9dc53-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="9dc53-156">**ใบสั่งงานหนึ่งใบต่อ** – สร้างใบสั่งงานที่มีการจัดกลุ่มตามการตั้งค่าของตัวเลือกอื่นๆ ที่จะพร้อมใช้งาน เมื่อคุณเลือกตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="9dc53-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="9dc53-157">หากคุณต้องการให้ตัวเลือกมีผลบังคับ เมื่อคุณรันเฉพาะแผนการบำรุงรักษาบางอย่างของคุณ บน FastTab **เรกคอร์ดที่จะรวม** ให้เพิ่มตัวกรองข้อมูลตามที่คุณต้องการ เช่นเดียวกับที่คุณอาจใช้สําหรับงานในชุดงานอื่นๆ ใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9dc53-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="9dc53-158">บน FastTab **รันในเบื้องหลัง** ให้ตั้งค่าตัวเลือกชุดงานและการจัดกำหนดการตามที่คุณต้องการ เช่นเดียวกับที่คุณอาจทำสำหรับงานในชุดงานอื่นๆ ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9dc53-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="9dc53-159">เลือก **ตกลง** เพื่อรันและ/หรือจัดกำหนดการแผนบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9dc53-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]