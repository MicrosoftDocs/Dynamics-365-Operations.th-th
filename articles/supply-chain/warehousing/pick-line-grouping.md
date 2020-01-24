---
title: การจัดกลุ่มรายการการเบิกสินค้า
description: หัวข้อนี้แสดงภาพรวมของการจัดกลุ่มรายการการเบิกสินค้า
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906279"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="3a655-103">การจัดกลุ่มรายการการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a655-104">ในการจัดกลุ่มรายการการเบิกสินค้า รายการงานที่หลากหลายที่มีสินค้าและสถานที่เดียวกันสามารถรวมเป็นการเบิกสินค้าเดียวที่จะถูกนำเสนอให้กับผู้ใช้บนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="3a655-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="3a655-105">ดังนั้น ผู้ปฏิบัติงานคลังสินค้าสามารถได้รับคำแนะนำที่มีประสิทธิภาพมากที่สุดที่เป็นไปได้ แต่การแยกที่จำเป็นของรายการงานในระบบยังถูกรักษาไว้ด้วยเช่นกัน (ตัวอย่างเช่น สำหรับคอนเทนเนอร์และใบสั่งที่แตกต่างกัน)</span><span class="sxs-lookup"><span data-stu-id="3a655-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="3a655-106">ตั้งค่าการจัดกลุ่มรายการการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="3a655-107">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="3a655-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="3a655-108">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่** และสร้างรายการเมนูใหม่ที่มีชื่อว่า **สินค้าในรายการกลุ่มการขาย – สั่งการโดยผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3a655-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="3a655-109">ภายใต้ **รายการเมนูสำหรับอุปกรณ์เคลื่อนที่** ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3a655-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="3a655-110">ในฟิลด์ **ชื่อรายการเมนู** ให้ป้อน **การเบิกสินค้าขาย - รายการกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="3a655-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="3a655-111">ในฟิลด์ **ชื่อเรื่อง** ให้ป้อน **การเบิกสินค้าขาย - รายการกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="3a655-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="3a655-112">ในฟิลด์ **โหมด** เลือก **งาน**</span><span class="sxs-lookup"><span data-stu-id="3a655-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="3a655-113">ตั้งค่าตัวเลือก **ใช้งานที่มีอยู่** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3a655-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="3a655-114">บน FastTab **ทั่วไป** คุณสามารถตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3a655-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="3a655-115">ในฟิลด์ **สั่งการโดย** เลือก **สั่งการโดยผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3a655-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="3a655-116">ตั้งค่าตัวเลือก **สร้างป้ายทะเบียน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3a655-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="3a655-117">ตั้งค่าตัวเลือก **จัดกลุ่มการเบิกสินค้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3a655-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="3a655-118">บน FastTab **คลาสงาน** ให้ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกคลาสงานที่ถูกต้องสำหรับรายการเมนูบนอุปกรณ์เคลื่อนที่:</span><span class="sxs-lookup"><span data-stu-id="3a655-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="3a655-119">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3a655-119">Select **New**.</span></span>
    2. <span data-ttu-id="3a655-120">ในฟิลด์ **รหัสคลาสงาน** ให้เลือก **การขาย** หรือ **การเบิกสินค้า SO** โดยขึ้นอยู่กับคลังสินค้าที่คุณจะใช้</span><span class="sxs-lookup"><span data-stu-id="3a655-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="3a655-121">ในฟิลด์ **ชนิดใบสั่งงาน** เลือก **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="3a655-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="3a655-122">ตั้งค่าเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="3a655-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="3a655-123">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="3a655-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="3a655-124">เพิ่มรายการเมนูที่คุณเพิ่งสร้างไปยังเมนูที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3a655-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="3a655-125">ตั้งค่าเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="3a655-125">Set up a work template</span></span>

1. <span data-ttu-id="3a655-126">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="3a655-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="3a655-127">ค้นหาเท็มเพลตงานที่ควรใช้กับฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="3a655-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="3a655-128">สำหรับตัวอย่างนี้ ให้เลือกเท็มเพลตงาน Contoso **51 ขั้นตอนการเบิกสินค้า** มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="3a655-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="3a655-129">บนเมนู เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="3a655-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="3a655-130">บนแท็บ **การเรียงลำดับ** เลือก **เพิ่ม** และจากนั้นตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3a655-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="3a655-131">ในฟิลด์ **ตาราง** เลือก **ธุรกรรมงานชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="3a655-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="3a655-132">ในฟิลด์ **ตารางสืบทอด** เลือก **ธุรกรรมงานชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="3a655-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="3a655-133">ในฟิลด์ **ฟิลด์** ให้เลือก **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="3a655-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="3a655-134">ในฟิลด์ **แนวทางการค้นหา** เลือก **การเรียงจากน้อยไปมาก**</span><span class="sxs-lookup"><span data-stu-id="3a655-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="3a655-135">สำหรับฟังก์ชันการจัดกลุ่มรายการการเบิกสินค้าไปยังงาน จะต้องเรียงลำดับรายการงานตามรหัสสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="3a655-136">ถ้ารายการที่มีสินค้าเดียวกันไม่ได้เรียงลำดับทีละรายการ จะไม่มีการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="3a655-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="3a655-137">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3a655-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="3a655-138">สร้างงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-138">Create picking work</span></span>

<span data-ttu-id="3a655-139">ก่อนที่คุณจะสามารถตั้งค่าการจัดกลุ่มรายการการเบิกสินค้า คุณจะต้องสร้างงานขาออกที่มีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="3a655-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="3a655-140">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="3a655-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="3a655-141">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3a655-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="3a655-142">ในฟิลด์ **บัญชีลูกค้า** เลือกลูกค้าใดๆ</span><span class="sxs-lookup"><span data-stu-id="3a655-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="3a655-143">บน FastTab **ทั่วไป** ในฟิลด์ **คลังสินค้า** เลือก **51**</span><span class="sxs-lookup"><span data-stu-id="3a655-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="3a655-144">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3a655-144">Then select **OK**.</span></span>
5. <span data-ttu-id="3a655-145">ภายใต้ **รายการใบสั่งขาย** เพิ่มรายการหกรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3a655-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="3a655-146">**รายการที่ 1:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **M9200**</span><span class="sxs-lookup"><span data-stu-id="3a655-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="3a655-147">ในฟิลด์ **ปริมาณ** ให้ป้อน **3**</span><span class="sxs-lookup"><span data-stu-id="3a655-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="3a655-148">**รายการที่ 2:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **M9201**</span><span class="sxs-lookup"><span data-stu-id="3a655-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="3a655-149">ในฟิลด์ **ปริมาณ** ให้ป้อน **3**</span><span class="sxs-lookup"><span data-stu-id="3a655-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="3a655-150">**รายการที่ 3:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **M9202**</span><span class="sxs-lookup"><span data-stu-id="3a655-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="3a655-151">ในฟิลด์ **ปริมาณ** ให้ป้อน **2**</span><span class="sxs-lookup"><span data-stu-id="3a655-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="3a655-152">**รายการที่ 4:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **M9200**</span><span class="sxs-lookup"><span data-stu-id="3a655-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="3a655-153">ในฟิลด์ **ปริมาณ** ให้ป้อน **1**</span><span class="sxs-lookup"><span data-stu-id="3a655-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="3a655-154">**รายการที่ 5:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **M9200**</span><span class="sxs-lookup"><span data-stu-id="3a655-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="3a655-155">ในฟิลด์ **ปริมาณ** ให้ป้อน **3**</span><span class="sxs-lookup"><span data-stu-id="3a655-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="3a655-156">**รายการที่ 6:** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **M9202**</span><span class="sxs-lookup"><span data-stu-id="3a655-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="3a655-157">ในฟิลด์ **ปริมาณ** ให้ป้อน **7**</span><span class="sxs-lookup"><span data-stu-id="3a655-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="3a655-158">นี่คือสรุปของปริมาณรวมสำหรับแต่ละรายการ:</span><span class="sxs-lookup"><span data-stu-id="3a655-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="3a655-159">**สินค้า M9200:** รายการละ 7</span><span class="sxs-lookup"><span data-stu-id="3a655-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="3a655-160">**สินค้า M9201:** รายการละ 3</span><span class="sxs-lookup"><span data-stu-id="3a655-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="3a655-161">**สินค้า M9202:** รายการละ 9</span><span class="sxs-lookup"><span data-stu-id="3a655-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="3a655-162">ก่อนที่คุณจะนำใบสั่งออกใช้กับคลังสินค้า คุณต้องตรวจสอบให้แน่ใจว่าสถานที่เบิกสินค้ามีสินค้าคงคลังเพียงพอสำหรับสินค้าทั้งหมดในใบสั่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3a655-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="3a655-163">ตรวจทานการตั้งค่า **คำสั่งสถานที่** เพื่อกำหนดสถานที่เบิกสินค้าที่จะใช้สำหรับการเบิกสินค้าตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3a655-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="3a655-164">จองสินค้าคงคลัง และนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="3a655-165">มีการสร้างรหัสงานที่มีหกบรรทัด</span><span class="sxs-lookup"><span data-stu-id="3a655-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="3a655-166">รายการถูกเรียงลำดับตามหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="3a655-167">รันโฟลว์อุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="3a655-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="3a655-168">บนอุปกรณ์เคลื่อนที่ ให้เลือกเมนูที่มีรายการเมนูบนอุปกรณ์เคลื่อนที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="3a655-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="3a655-169">เลือกรายการเมนู **การเบิกสินค้าขาย – รายการกลุ่ม** และเริ่มต้นการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="3a655-170">หลังจากที่คุณเลือกเมนูและป้อนรหัสงาน คุณจะเห็นขั้นตอนการเบิกสินค้าที่มีการจัดกลุ่มรายการเบิกสินค้าทั้งหมดสำหรับสินค้า M9200</span><span class="sxs-lookup"><span data-stu-id="3a655-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="3a655-171">คุณได้รับคำแนะนำในการเลือก 7 รายการจากสินค้า M9200</span><span class="sxs-lookup"><span data-stu-id="3a655-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="3a655-172">ยืนยันขั้นตอนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="3a655-173">ไปที่หน้าจอไคลเอ็นต์ของงานระหว่างทำ และสังเกตว่ารายการเบิกสินค้าทั้งสามรายการสำหรับสินค้า M9200 ถูกปิดพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="3a655-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="3a655-174">รายการงาน 4 จะถูกนำเสนอ</span><span class="sxs-lookup"><span data-stu-id="3a655-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="3a655-175">ยืนยันขั้นตอนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a655-175">Confirm the pick step.</span></span>

    <span data-ttu-id="3a655-176">ขั้นตอนการเบิกสินค้าสุดท้ายบนอุปกรณ์เคลื่อนที่จะรวมรายการการเบิกสินค้าสองรายการสุดท้ายจากใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3a655-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="3a655-177">ดำเนินการขั้นตอนการเบิกสินค้าสำหรับ 9 รายการจากสินค้า M9202</span><span class="sxs-lookup"><span data-stu-id="3a655-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="3a655-178">ยืนยันขั้นตอนการส่งสินค้าและคู่การรับ/ส่งสินค้าเพิ่มเติมใดๆ เพื่อทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3a655-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="3a655-179">สามารถจัดกลุ่มรายการงานได้เฉพาะเมื่อมีการเรียงลำดับเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3a655-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="3a655-180">ไม่มีการสนับสนุนฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3a655-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="3a655-181">สินค้าตามน้ำหนักจริง</span><span class="sxs-lookup"><span data-stu-id="3a655-181">Catch-weight items.</span></span> <span data-ttu-id="3a655-182">ถ้ามีสินค้าตามน้ำหนักจริงใดๆ ในงาน คุณจะได้รับข้อความแสดงข้อผิดพลาดก่อนที่คุณจะเริ่มเลือก</span><span class="sxs-lookup"><span data-stu-id="3a655-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="3a655-183">การเบิกสินค้าเป็นรายชิ้น</span><span class="sxs-lookup"><span data-stu-id="3a655-183">Piece picking.</span></span>
>    - <span data-ttu-id="3a655-184">รายการงานที่ยังทำงานการเติมสินค้าไม่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="3a655-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="3a655-185">การเบิกสินค้าเกิน</span><span class="sxs-lookup"><span data-stu-id="3a655-185">Over-picking.</span></span>
