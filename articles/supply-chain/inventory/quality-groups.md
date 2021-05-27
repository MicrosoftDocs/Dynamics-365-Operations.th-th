---
title: กลุ่มคุณภาพสินค้า
description: หัวข้อนี้จะอธิบายวิธีการใช้และสร้างกลุ่มคุณภาพสินค้าเพื่อจัดกลุ่มผลิตภัณฑ์ตามตรรกะและสามารถมอบหมายให้กับการเชื่อมโยงคุณภาพในการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติได้
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022263"
---
# <a name="item-quality-groups"></a><span data-ttu-id="94b25-103">กลุ่มคุณภาพสินค้า</span><span class="sxs-lookup"><span data-stu-id="94b25-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94b25-104">กลุ่มคุณภาพแสดงข้อกำหนดในการทดสอบทั่วไปสำหรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="94b25-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="94b25-105">หัวข้อนี้จะอธิบายวิธีการใช้และสร้างกลุ่มคุณภาพสินค้าเพื่อจัดกลุ่มผลิตภัณฑ์ตามตรรกะและสามารถมอบหมายให้กับการเชื่อมโยงคุณภาพในการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="94b25-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="94b25-106">เพื่อตั้งค่า แก้ไขและดูสินค้าที่กำหนดให้กับกลุ่มคุณภาพหรือกลุ่มคุณภาพที่กำหนดให้กับสินค้า ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> กลุ่มคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="94b25-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="94b25-107">หลังจากที่คุณกำหนดความต้องการทดสอบบนหน้า **กลุ่มทดสอบ** คุณสามารถกำหนดกฎสำหรับการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="94b25-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="94b25-108">เพื่อทำให้กระบวนการ คุณไม่กำหนดกฎสำหรับสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="94b25-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="94b25-109">คุณสามารถกำหนดกฎสำหรับกลุ่มคุณภาพบนหน้า **ความสัมพันธ์ของคุณภาพ** แทนได้</span><span class="sxs-lookup"><span data-stu-id="94b25-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="94b25-110">ตัวอย่างของกลุ่มคุณภาพของสินค้า</span><span class="sxs-lookup"><span data-stu-id="94b25-110">Example of an item quality group</span></span>

<span data-ttu-id="94b25-111">บริษัทผู้ผลิตจัดซื้อวัตถุดิบหลายอย่างที่มีการทดสอบสำหรับสินค้าสำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="94b25-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="94b25-112">ดังนั้นบริษัทกำหนดกลุ่มคุณภาพและกำหนดหมายเลขสินค้าที่เกี่ยวข้องกับวัตถุดิบสำหรับกลุ่มนั้น</span><span class="sxs-lookup"><span data-stu-id="94b25-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="94b25-113">ภายหลัง บริษัทสั่งซื้อวัตถุดิบชนิดใหม่ที่มีความต้องการทดสอบเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="94b25-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="94b25-114">แทนที่จะติดตั้งข้อกำหนดในการทดสอบใหม่สำหรับวัสดุใหม่ บริษัทเพิ่มหมายเลขสินค้าสำหรับวัสดุใหม่ให้กับกลุ่มคุณภาพที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="94b25-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="94b25-115">บริษัทเดียวกันนี้ยังผลิตสินค้าที่มี มีข้อกำหนดในการทดสอบเดียวกันและจัดส่งสินค้าที่มีข้อกำหนดแบบเดียวกันในการทดสอบก่อนจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="94b25-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="94b25-116">ดังนั้นบริษัทกำหนดกลุ่มคุณภาพเพิ่มเติมสองกลุ่มและกำหนดหมายเลขสินค้าที่เกี่ยวข้องให้กับกลุ่มคุณภาพแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="94b25-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="94b25-117">สร้างกลุ่มคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-117">Create a quality group</span></span>

<span data-ttu-id="94b25-118">เมื่อต้องการสร้างกลุ่มคุณภาพ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="94b25-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="94b25-119">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> กลุ่มคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="94b25-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="94b25-120">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="94b25-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="94b25-121">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="94b25-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="94b25-122">**กลุ่มคุณภาพ** – ป้อนรหัสหรือชื่อเฉพาะสำหรับกลุ่มคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="94b25-123">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของกลุ่มคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="94b25-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="94b25-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="94b25-125">เพิ่มสินค้าไปยังกลุ่มคุณภาพด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="94b25-125">Manually add items to a quality group</span></span>

<span data-ttu-id="94b25-126">ในการเพิ่มสินค้าลงในกลุ่มคุณภาพด้วยตนเอง ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="94b25-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="94b25-127">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> กลุ่มคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="94b25-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="94b25-128">เลือกกลุ่มคุณภาพที่คุณต้องการเพิ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="94b25-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="94b25-129">บนบานหน้าต่างการดำเนินการ เลือก **สินค้า**</span><span class="sxs-lookup"><span data-stu-id="94b25-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="94b25-130">บนหน้า **สินค้าในกลุ่มคุณภาพ** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="94b25-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="94b25-131">จากนั้น สำหรับแถวใหม่ ให้ตั้งค่าฟิลด์ **หมายเลขสินค้า** ให้กับหมายเลขสินค้าที่คุณต้องการเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="94b25-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="94b25-132">ทําซ้ำขั้นตอนก่อนหน้านี้สำหรับสินค้าเพิ่มเติมแต่ละรายการที่คุณต้องเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="94b25-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="94b25-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="94b25-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="94b25-134">เพิ่มสินค้าหลายรายการไปยังกลุ่มคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="94b25-135">ในการเพิ่มสินค้าหลายรายการลงในกลุ่มคุณภาพด้วยตนเอง ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="94b25-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="94b25-136">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> กลุ่มคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="94b25-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="94b25-137">สร้างหรือเลือกกลุ่มคุณภาพที่คุณต้องการเพิ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="94b25-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="94b25-138">บนบานหน้าต่างการดำเนินการ เลือก **เพิ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="94b25-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="94b25-139">ในกล่องโต้ตอบ **การสอบถาม** ให้ป้อนเงื่อนไขตัวกรองข้อมูลของสินค้าที่คุณต้องการเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="94b25-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="94b25-140">ตัวอย่างเช่น คุณอาจกรองข้อมูลสินค้าทั้งหมดในกลุ่มสินค้าหนึ่ง ๆ</span><span class="sxs-lookup"><span data-stu-id="94b25-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="94b25-141">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="94b25-141">Select **OK**.</span></span>
1. <span data-ttu-id="94b25-142">ในกล่องโต้ตอบ **เพิ่มสินค้า** กริดจะแสดงรายการทั้งหมดที่ตรงกับการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="94b25-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="94b25-143">ตรวจสอบผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="94b25-143">Review the results.</span></span>

    <span data-ttu-id="94b25-144">ถ้าต้องระบุการเปลี่ยนแปลงใด ๆ ให้เลือก **เลือก** เพื่อกลับไปที่กล่องโต้ตอบ **การสอบถาม** เพื่อปรับปรุงการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="94b25-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="94b25-145">เมื่อผลลัพธ์มีรายการทั้งหมดที่คุณต้องการเพิ่ม ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="94b25-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="94b25-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="94b25-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="94b25-147">เชื่อมโยงสินค้ากับกลุ่มคุณภาพด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="94b25-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="94b25-148">ในการเชื่อมโยงสินค้ากับกลุ่มคุณภาพด้วยตนเอง ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="94b25-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="94b25-149">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> กลุ่มคุณภาพสินค้า**</span><span class="sxs-lookup"><span data-stu-id="94b25-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="94b25-150">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="94b25-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="94b25-151">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="94b25-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="94b25-152">**หมายเลขสินค้า** – ให้เลือกหมายเลขสินค้าเพื่อเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="94b25-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="94b25-153">**กลุ่มคุณภาพ** – เลือกกลุ่มคุณภาพที่จะกําหนดให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="94b25-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="94b25-154">ทําซ้ําขั้นตอนก่อนหน้านี้ให้กับชุดสินค้าเพิ่มเติมแต่ละชุดและกลุ่มคุณภาพที่ต้องเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="94b25-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="94b25-155">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="94b25-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="94b25-156">เพิ่มกลุ่มคุณภาพจากหน้าผลิตภัณฑ์ที่นำออกใช้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="94b25-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="94b25-157">หากต้องการเพิ่มกลุ่มคุณภาพจากหน้า **ผลิตภัณฑ์ที่นำออกใช้** ด้วยตนเอง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="94b25-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="94b25-158">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="94b25-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="94b25-159">เลือกผลิตภัณฑ์ที่คุณต้องการกำหนดให้กับกลุ่มคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="94b25-160">บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการสินค้าคงคลัง** ในกลุ่ม **คุณภาพ** เลือก **กลุ่มคุณภาพสินค้า**</span><span class="sxs-lookup"><span data-stu-id="94b25-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="94b25-161">บนหน้า **สินค้าในกลุ่มคุณภาพ** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="94b25-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="94b25-162">จากนั้น ให้ตั้งค่าฟิลด์ **กลุ่มคุณภาพ** เป็นกลุ่มคุณภาพที่คุณต้องการกําหนดให้กับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="94b25-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="94b25-163">ทําซ้ําขั้นตอนก่อนหน้านี้ของกลุ่มคุณภาพเพิ่มเติมแต่ละกลุ่มที่คุณต้องการกําหนดให้กับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="94b25-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="94b25-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="94b25-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94b25-165">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="94b25-165">Additional resources</span></span>

- [<span data-ttu-id="94b25-166">เครื่องมือการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="94b25-167">การทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="94b25-168">กลุ่มการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="94b25-169">ตัวแปรการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="94b25-170">ความสัมพันธ์ของคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="94b25-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
