---
title: การจัดกลุ่มรายการการเบิกสินค้า
description: หัวข้อนี้แสดงภาพรวมของการจัดกลุ่มรายการการเบิกสินค้า
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fe0e63ef742b7bfd09684a94d273a1841d24599c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828285"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="2a1ec-103">การจัดกลุ่มรายการการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a1ec-104">การจัดกลุ่มรายการการเบิกสินค้าช่วยให้รายการงานที่หลากหลายที่มีสินค้าและสถานที่เดียวกันสามารถรวมเป็นการเบิกสินค้าเดียวที่จะถูกนำเสนอให้กับผู้ใช้บนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2a1ec-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="2a1ec-105">ดังนั้น ผู้ปฏิบัติงานคลังสินค้าสามารถได้รับคำแนะนำที่มีประสิทธิภาพมากที่สุดที่เป็นไปได้ แต่การแยกของรายการงานที่จำเป็นในระบบ (สำหรับคอนเทนเนอร์ ใบสั่ง และอื่น ๆ ที่แตกต่างกัน) ยังถูกรักษาไว้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="2a1ec-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="2a1ec-106">เปิดคุณลักษณะการจัดกลุ่มรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="2a1ec-107">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2a1ec-108">ผู้ดูแลระบบสามารถใช้พื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="2a1ec-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2a1ec-109">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2a1ec-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2a1ec-110">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2a1ec-111">**ชื่อคุณลักษณะ:** *การจัดกลุ่มรายการเบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="2a1ec-112">ตั้งค่าการจัดกลุ่มรายการการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="2a1ec-113">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2a1ec-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="2a1ec-114">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2a1ec-115">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2a1ec-116">ในฟิลด์ **ชื่อรายการเมนู** ให้ป้อน *สินค้าในรายการกลุ่มการขาย*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="2a1ec-117">ในฟิลด์ **ชื่อเรื่อง** ให้ป้อน *สินค้าในรายการกลุ่มการขาย*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="2a1ec-118">ชื่อนี้จะแสดงในเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2a1ec-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="2a1ec-119">ในฟิลด์ **โหมด** เลือก *งาน*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="2a1ec-120">ตั้งค่าตัวเลือก **ใช้งานที่มีอยู่** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="2a1ec-121">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2a1ec-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2a1ec-122">ในฟิลด์ **สั่งการโดย** เลือก *สั่งการโดยผู้ใช้*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="2a1ec-123">ตั้งค่าตัวเลือก **สร้างป้ายทะเบียน** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="2a1ec-124">ตั้งค่าตัวเลือก **จัดกลุ่มการเบิกสินค้า** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="2a1ec-125">ยอมรับค่าเริ่มต้นสำหรับตัวเลือกอื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="2a1ec-126">ให้ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกคลาสงานที่ถูกต้องสำหรับรายการเมนูบนอุปกรณ์เคลื่อนที่:</span><span class="sxs-lookup"><span data-stu-id="2a1ec-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="2a1ec-127">บนแท็บ **คลาสงาน** ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="2a1ec-128">ในฟิลด์ **รหัสคลาสงาน** คุณสามารถเลือก *การขาย* หรือ *การเบิกสินค้า SO* โดยขึ้นอยู่กับคลังสินค้าที่คุณจะใช้</span><span class="sxs-lookup"><span data-stu-id="2a1ec-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="2a1ec-129">สำหรับสถานการณ์นี้ *การเบิกสินค้า SO*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="2a1ec-130">ฟิลด์ **ชนิดใบสั่งงาน** ตั้งค่าเป็น *ใบสั่งขาย* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="2a1ec-131">ตั้งค่าเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2a1ec-131">Set up a mobile device menu</span></span>

<span data-ttu-id="2a1ec-132">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเพิ่มรายการเมนูที่คุณเพิ่งสร้างขึ้นในเมนู **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="2a1ec-133">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="2a1ec-134">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2a1ec-135">บานหน้าต่างรายการแสดงเมนูอุปกรณ์เคลื่อนที่ที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2a1ec-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="2a1ec-136">เลือก *ขาออก* ในรายการ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="2a1ec-137">ในรายการ **เมนูและรายการเมนูที่พร้อมใช้งาน** ให้ค้นหาและเลือกรายการเมนู *สินค้าในรายการกลุ่มการขาย* ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="2a1ec-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="2a1ec-138">เลือกปุ่มลูกศรขวาเพื่อย้ายรายการเมนู *สินค้าในรายการกลุ่มการขาย* ไปยังรายการ **โครงสร้างเมนู**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="2a1ec-139">ใช้ปุ่มลูกศรขึ้นและลูกศรลงเพื่อย้ายรายการเมนูไปยังตำแหน่งที่ต้องการในโครงสร้างเมนู</span><span class="sxs-lookup"><span data-stu-id="2a1ec-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="2a1ec-140">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="2a1ec-141">ตั้งค่าเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="2a1ec-141">Set up a work template</span></span>

1. <span data-ttu-id="2a1ec-142">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="2a1ec-143">ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="2a1ec-144">ในกริด **ภาพรวม** ให้ค้นหาและเลือกแม่แบบงานที่ควรใช้กับฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="2a1ec-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="2a1ec-145">สำหรับสถานการณ์นี้ เลือกแม่แบบ *51 ขั้นตอนการเบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="2a1ec-146">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="2a1ec-147">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **การเรียงลำดับ** ให้เลือก **เพิ่ม** แล้วจากนั้นตั้งค่าค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="2a1ec-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="2a1ec-148">ในคอลัมน์ **ตาราง** เลือก *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="2a1ec-149">ในคอลัมน์ **ตารางสืบทอด** เลือก *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="2a1ec-150">ในคอลัมน์ **ฟิลด์** ให้เลือก *หมายเลขสินค้า*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="2a1ec-151">ในคอลัมน์ **แนวทางการค้นหา** เลือก *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="2a1ec-152">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบและบันทึกการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="2a1ec-153">คุณจะได้รับข้อความแสดงข้อความต่อไปนี้: "การจัดกลุ่มจะถูกรีเซ็ต ดำเนินการต่อหรือไม่"</span><span class="sxs-lookup"><span data-stu-id="2a1ec-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="2a1ec-154">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a1ec-155">สำหรับฟังก์ชันการจัดกลุ่มรายการการเบิกสินค้าไปยังงาน จะต้องเรียงลำดับรายการงานตามรหัสสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="2a1ec-156">ถ้ารายการที่มีสินค้าเดียวกันไม่ได้เรียงลำดับทีละรายการ จะไม่มีการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="2a1ec-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="2a1ec-157">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2a1ec-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="2a1ec-158">สร้างงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-158">Create picking work</span></span>

<span data-ttu-id="2a1ec-159">ก่อนที่คุณจะสามารถตั้งค่าการจัดกลุ่มรายการการเบิกสินค้า คุณจะต้องสร้างงานขาออกที่มีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="2a1ec-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="2a1ec-160">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2a1ec-161">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="2a1ec-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="2a1ec-162">ในฟิลด์ **บัญชีลูกค้า** เลือก *US-004*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="2a1ec-163">บน FastTab **ทั่วไป** ในฟิลด์ **คลังสินค้า** เลือก *51*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="2a1ec-164">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-164">Select **OK**.</span></span>
1. <span data-ttu-id="2a1ec-165">บนแท็บด่วน **รายการใบสั่งขาย** เพิ่มรายการหกรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2a1ec-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="2a1ec-166">**รายการที่ 1:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก *M9200*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="2a1ec-167">ในฟิลด์ **ปริมาณ** ให้ป้อน *3*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="2a1ec-168">**รายการที่ 2:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก *M9201*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="2a1ec-169">ในฟิลด์ **ปริมาณ** ให้ป้อน *3*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="2a1ec-170">**รายการที่ 3:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก *M9202*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="2a1ec-171">ในฟิลด์ **ปริมาณ** ให้ป้อน *2*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="2a1ec-172">**รายการที่ 4:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก *M9200*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="2a1ec-173">ในฟิลด์ **ปริมาณ** ให้ป้อน *1*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="2a1ec-174">**รายการที่ 5:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก *M9200*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="2a1ec-175">ในฟิลด์ **ปริมาณ** ให้ป้อน *3*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="2a1ec-176">**รายการที่ 6:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก *M9202*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="2a1ec-177">ในฟิลด์ **ปริมาณ** ให้ป้อน *7*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="2a1ec-178">นี่คือสรุปของปริมาณรวมสำหรับแต่ละรายการ:</span><span class="sxs-lookup"><span data-stu-id="2a1ec-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="2a1ec-179">**สินค้า M9200:** รายการละ *7*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="2a1ec-180">**สินค้า M9201:** รายการละ *3*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="2a1ec-181">**สินค้า M9202:** รายการละ *9*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="2a1ec-182">ก่อนที่คุณจะนำใบสั่งออกใช้กับคลังสินค้า คุณต้องตรวจสอบให้แน่ใจว่าสถานที่เบิกสินค้ามีสินค้าคงคลังเพียงพอสำหรับสินค้าทั้งหมดในใบสั่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2a1ec-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="2a1ec-183">ตรวจทานการตั้งค่า **คำสั่งสถานที่** เพื่อกำหนดสถานที่เบิกสินค้าที่จะใช้สำหรับการเบิกสินค้าตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="2a1ec-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="2a1ec-184">หากคุณใช้สภาพแวดล้อมข้อมูลสาธิตของ Contoso ในคลังสินค้า *51* ให้ยืนยันว่ามีสินค้าคงคลังที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2a1ec-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="2a1ec-185">ตอนนี้ คุณต้องจองสินค้าคงคลังในแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="2a1ec-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="2a1ec-186">บนแท็บด่วน **บรรทัดใบสั่งขาย** ให้เลือกบรรทัดใดบรรทัดหนึ่งที่ต้องจองไว้</span><span class="sxs-lookup"><span data-stu-id="2a1ec-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="2a1ec-187">บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="2a1ec-188">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อใช้การจอง</span><span class="sxs-lookup"><span data-stu-id="2a1ec-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="2a1ec-189">จากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-189">Then close the page.</span></span>
1. <span data-ttu-id="2a1ec-190">ทําซ้ําขั้นตอน 8 ถึง 10 ของบรรทัดที่เหลือที่ต้องจอง</span><span class="sxs-lookup"><span data-stu-id="2a1ec-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="2a1ec-191">คุณต้องนำออกใช้ใบสั่งขายไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="2a1ec-192">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2a1ec-193">คุณจะได้รับข้อความระบุว่ามีการสร้างการจัดส่งและเวฟแล้ว และมีการส่งเวฟเพื่อรันในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2a1ec-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="2a1ec-194">เมื่อเวฟและงานแบบดาวน์สตรีมทั้งหมดเสร็จสมบูรณ์แล้ว รหัสงานจะถูกสร้างขึ้นสำหรับงานที่มีหกรายการ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="2a1ec-195">รายการถูกเรียงลำดับตามหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="2a1ec-196">ไปที่ **การจัดการคลังสินค้า \> งาน \> งานทั้งหมด** เพื่อดูงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="2a1ec-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="2a1ec-197">จดบันทึกค่า **รหัสงาน** เนื่องจากคุณจะต้องใช้ในกระบวนงานถัดไป</span><span class="sxs-lookup"><span data-stu-id="2a1ec-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="2a1ec-198">เริ่มการเบิกสินค้าจากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2a1ec-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="2a1ec-199">ลงชื่อเข้าใช้อุปกรณ์เคลื่อนที่ในฐานะผู้ใช้ที่ถูกตั้งค่าสำหรับคลังสินค้า *51*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="2a1ec-200">บนอุปกรณ์เคลื่อนที่ ให้เลือกเมนูที่มีรายการเมนูบนอุปกรณ์เคลื่อนที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="2a1ec-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="2a1ec-201">สำหรับสถานการณ์นี้ **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="2a1ec-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="2a1ec-202">เลือกรายการเมนู **สินค้าในรายการกลุ่มการขาย** เพื่อเริ่มต้นการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="2a1ec-203">ป้อนค่า **รหัสงาน** ที่คุณบันทึกในกระบวนงานก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="2a1ec-204">คุณควรดูขั้นตอนการเบิกสินค้าที่มีการจัดกลุ่มรายการเบิกสินค้าทั้งหมดของสินค้า *M9200* และคุณควรได้รับคำแนะนำในการเบิก *7* รายการของแต่ละ *M9200*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2a1ec-205">บนอุปกรณ์เคลื่อนที่ งานการเบิกสินค้าจะรวมรายการงานเบิกสินค้าสามรายการเป็นขั้นตอนการเบิกสินค้าเดียวของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2a1ec-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="2a1ec-206">ยืนยันขั้นตอนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="2a1ec-207">ไปที่หน้าของงานสำหรับรหัสงาน และสังเกตว่ารายการเบิกสินค้าทั้งสามรายการสำหรับสินค้า *M9200* ถูกปิดพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="2a1ec-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="2a1ec-208">กลับไปที่อุปกรณ์เคลื่อนที่ และเบิกสินค้าต่อ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="2a1ec-209">รายการงาน 4 สำหรับสินค้า *M9201* ควรถูกนําเสนอ</span><span class="sxs-lookup"><span data-stu-id="2a1ec-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="2a1ec-210">เนื่องจากใบสั่งมีรายการงานเพียงรายการเดียว จึงไม่มีสิ่งใดให้รวม</span><span class="sxs-lookup"><span data-stu-id="2a1ec-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="2a1ec-211">ยืนยันขั้นตอนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2a1ec-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="2a1ec-212">ขั้นตอนการเบิกสินค้าสุดท้ายบนอุปกรณ์เคลื่อนที่จะรวมรายการการเบิกสินค้าสองรายการสุดท้ายจากใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="2a1ec-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="2a1ec-213">ดำเนินการขั้นตอนการเบิกสินค้าสำหรับ *9* รายการจากสินค้า *M9202*</span><span class="sxs-lookup"><span data-stu-id="2a1ec-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="2a1ec-214">ยืนยันขั้นตอนการส่งสินค้าและคู่การรับ/ส่งสินค้าเพิ่มเติมใดๆ เพื่อทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2a1ec-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="2a1ec-215">สามารถจัดกลุ่มรายการงานได้เฉพาะเมื่อมีการเรียงลำดับเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2a1ec-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="2a1ec-216">ไม่มีการสนับสนุนฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2a1ec-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="2a1ec-217">สินค้าตามน้ำหนักจริง</span><span class="sxs-lookup"><span data-stu-id="2a1ec-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="2a1ec-218">ถ้ามีสินค้าตามน้ำหนักจริงใดๆ ในงาน คุณจะได้รับข้อความแสดงข้อผิดพลาดก่อนที่คุณจะเริ่มเลือก</span><span class="sxs-lookup"><span data-stu-id="2a1ec-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="2a1ec-219">การเบิกสินค้าเป็นรายชิ้น</span><span class="sxs-lookup"><span data-stu-id="2a1ec-219">Piece picking</span></span>
>   - <span data-ttu-id="2a1ec-220">รายการงานที่ยังทำงานการเติมสินค้าไม่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="2a1ec-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="2a1ec-221">การเบิกสินค้าเกิน</span><span class="sxs-lookup"><span data-stu-id="2a1ec-221">Over-picking</span></span>
>   - <span data-ttu-id="2a1ec-222">การปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด</span><span class="sxs-lookup"><span data-stu-id="2a1ec-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]