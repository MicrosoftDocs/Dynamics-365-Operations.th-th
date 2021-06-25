---
title: ตั้งค่าฟิลด์สำหรับแอปการจัดการคลังสินค้าบนมือถือ
description: หัวข้อนี้อธิบายวิธีการกำหนดและการตั้งค่าคอนฟิกชื่อฟิลด์และระดับความสำคัญในแอปการจัดการคลังสินค้าบนมือถือ
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc224d3fd6cf5b111f61066202090f10ba4a7e8a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189261"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="bef73-103">ตั้งค่าฟิลด์สำหรับแอปการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="bef73-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bef73-104">หัวข้อนี้อธิบายวิธีการกำหนดและการตั้งค่าคอนฟิกชื่อฟิลด์และระดับความสำคัญในแอปการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="bef73-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="bef73-105">หัวข้อนี้ใช้กับคุณลักษณะในการบริหารคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="bef73-106">ไม่สามารถใช้กับคุณลักษณะในการจัดการสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="bef73-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="bef73-107">แอปการจัดการคลังสินค้าบนมือถือเป็นแอปที่คุณสามารถใช้เพื่อทำงานในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="bef73-108">คุณสามารถกำหนดและตั้งค่าคอนฟิกชื่อฟิลด์ที่ใช้ในแอพลิเคชัน ตลอดจนตั้งค่าคอนฟิกระดับความสำคัญที่ควรจะกำหนดชื่อฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bef73-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="bef73-109">หัวข้อนี้อธิบายวิธีการกำหนดและการตั้งค่าคอนฟิกชื่อฟิลด์แอปการจัดการคลังสินค้าบนมือถือและระดับความสำคัญเหล่านี้ และวิธีการใช้</span><span class="sxs-lookup"><span data-stu-id="bef73-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="bef73-110">ตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-110">Configure warehouse app field names</span></span>

<span data-ttu-id="bef73-111">เมื่อคุณใช้แอพคลังสินค้าบนอุปกรณ์เคลื่อนที่ของคุณ คุณสามารถตั้งค่าคอนฟิกวิธีที่ควรแสดงข้อมูลเมตาของอุปกรณ์ของคุณบนหน้า **ชื่อฟิลด์แอพลิเคชันคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bef73-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="bef73-112">ในบริษัทใหม่ เลือก **สร้างการตั้งค่าเริ่มต้น** เพื่อสร้างชื่อฟิลด์ทั้งหมดที่จะถูกใช้ในลำดับงานของอุปกรณ์เคลื่อนที่คลังสินค้า และจากนั้นกำหนดโหมดการป้อนข้อมูลและชนิดการป้อนข้อมูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bef73-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="bef73-113">หลังจากที่คุณได้สร้างชื่อฟิลด์ทั้งหมด คุณสามารถเลือกตัวเลือกข้อมูลป้อนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bef73-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bef73-114">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bef73-114">Option</span></span></th>
<th><span data-ttu-id="bef73-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bef73-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bef73-116">วิธีการป้อนข้อมูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bef73-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="bef73-117">ตัวเลือกนี้กำหนดว่าควรแสดงฟิลด์การสแกนหรือฟิลด์ป้อนข้อมูลด้วยตนเองสำหรับชื่อฟิลด์ที่เลือกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bef73-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="bef73-118">ซึ่งเป็นประโยชน์ในการแยกฟิลด์โดยขึ้นอยู่กับว่าบาร์โค้ดถูกใช้สำหรับฟิลด์นั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bef73-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="bef73-119"><strong>หมายเหตุ:</strong> สำหรับชื่อฟิลด์ที่มีโหมดการป้อนข้อมูลที่คุณต้องการถูกตั้งค่าเป็น <strong>การสแกน</strong> คุณสามารถป้อนข้อมูลด้วยตนเองถ้าไม่สามารถอ่านบาร์โค้ดได้หรือบาร์โค้ดเสียหาย</span><span class="sxs-lookup"><span data-stu-id="bef73-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bef73-120">ชนิดของข้อมูลป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="bef73-120">Input type</span></span></td>
<td><span data-ttu-id="bef73-121">ตัวเลือกนี้จะกำหนดว่าควรใช้ชนิดการป้อนข้อมูลใดสำหรับชื่อฟิลด์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bef73-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="bef73-122">มีตัวเลือกสี่อย่าง:</span><span class="sxs-lookup"><span data-stu-id="bef73-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="bef73-123"><strong>การเลือก</strong> - ประกอบด้วยรายการของตัวเลือกที่ให้เลือก</span><span class="sxs-lookup"><span data-stu-id="bef73-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="bef73-124">ชื่อฟิลด์ที่มีตัวเลือกนี้จะไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="bef73-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="bef73-125"><strong>วันที่</strong> - ชื่อฟิลด์ที่ระบุเป็นวันที่จะแสดงรูปแบบวันที่พร้อมกับป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="bef73-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="bef73-126">ซึ่งจะช่วยให้ผู้ปฏิบัติงานคลังสินค้าสามารถดูว่าจะป้อนวันที่ในรูปแบบใด</span><span class="sxs-lookup"><span data-stu-id="bef73-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="bef73-127">ชื่อฟิลด์ที่มีตัวเลือกนี้จะไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="bef73-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="bef73-128"><strong>ตัวอักษร</strong> - ถ้ามีการเลือกไว้ แป้นพิมพ์อุปกรณ์จะถูกใช้เมื่อมีการป้อนข้อมูลด้วยตนเองในแอพลิเคชันนี้</span><span class="sxs-lookup"><span data-stu-id="bef73-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="bef73-129">สามารถเปลี่ยนประสบการณ์การใช้งานแป้นพิมพ์โดยขึ้นอยู่กับอุปกรณ์ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="bef73-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="bef73-130"><strong>ตัวเลข</strong> - สำหรับชื่อฟิลด์ที่ใช้การป้อนข้อมูลตัวเลขเท่านั้น คุณสามารถเลือกตัวเลือกนี้เพื่อแสดงแป้นพิมพ์ตัวเลขแบบกำหนดเองพร้อมกับฟิลด์การป้อนข้อมูลแทนแป้นพิมพ์อุปกรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="bef73-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="bef73-131">ตั้งค่าคอนฟิกระดับความสำคัญของฟิลด์แอพลิเคชันคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="bef73-132">ในหน้า **ระดับความสำคัญของฟิลด์แอพลิเคชันคลังสินค้า** คุณสามารถใส่ชื่อฟิลด์ไปยังกลุ่มระดับความสำคัญอื่นได้</span><span class="sxs-lookup"><span data-stu-id="bef73-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="bef73-133">ซึ่งทำให้สามารถตัดสินใจได้ว่าควรจะแสดงข้อมูลใดในหน้างานหลักเมื่อผู้ปฏิบัติงานคลังสินค้าทำงานโดยใช้แอพลิเคชันนี้</span><span class="sxs-lookup"><span data-stu-id="bef73-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="bef73-134">ถ้าคุณคลิก **สร้างการตั้งค่าเริ่มต้น** ชุดค่าเริ่มต้นของกลุ่มระดับความสำคัญจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="bef73-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="bef73-135">คุณสามารถสร้างกลุ่มการระดับความสำคัญได้มากเท่าที่จำเป็น แต่ระบบจะแสดงกลุ่มระดับความสำคัญเพียงสามกลุ่มบนหน้างาน</span><span class="sxs-lookup"><span data-stu-id="bef73-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="bef73-136">เมื่อระบบส่งข้อมูลเมตาไปยังแอพลิเคชัน ระบบจะกำหนดระดับความสำคัญที่เกี่ยวข้องให้กับแต่ละฟิลด์โดยขึ้นอยู่กับกลุ่มของระดับความสำคัญ และแอพลิเคชันจะแสดงระดับความสำคัญสามกลุ่มแรกที่อยู่ในข้อมูลเมตาในหน้างาน</span><span class="sxs-lookup"><span data-stu-id="bef73-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="bef73-137">ข้อมูลเมตาจำนวนมากที่เหลือจะถูกแสดงในหน้ารายละเอียดรอง</span><span class="sxs-lookup"><span data-stu-id="bef73-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="bef73-138">ตารางต่อไปนี้แสดงตัวอย่างของระดับความสำคัญ 5 กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bef73-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bef73-139">กลุ่มระดับความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="bef73-139">Priority group</span></span></th>
<th><span data-ttu-id="bef73-140">ฟิลด์ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="bef73-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="bef73-141">ระดับความสำคัญ 10</span><span class="sxs-lookup"><span data-stu-id="bef73-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="bef73-142">สินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-142">Item</span></span></li>
<li><span data-ttu-id="bef73-143">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="bef73-143">Quantity</span></span></li>
<li><span data-ttu-id="bef73-144">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="bef73-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="bef73-145">ระดับความสำคัญ 20</span><span class="sxs-lookup"><span data-stu-id="bef73-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="bef73-146">ตำแหน่งคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="bef73-146">Cluster position</span></span></li>
<li><span data-ttu-id="bef73-147">คลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="bef73-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="bef73-148">ระดับความสำคัญ 30</span><span class="sxs-lookup"><span data-stu-id="bef73-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="bef73-149">คำอธิบายสินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="bef73-150">ระดับความสำคัญ 40</span><span class="sxs-lookup"><span data-stu-id="bef73-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="bef73-151">โครงแบบ</span><span class="sxs-lookup"><span data-stu-id="bef73-151">Configuration</span></span></li>
<li><span data-ttu-id="bef73-152">สี</span><span class="sxs-lookup"><span data-stu-id="bef73-152">Color</span></span></li>
<li><span data-ttu-id="bef73-153">ขนาด</span><span class="sxs-lookup"><span data-stu-id="bef73-153">Size</span></span></li>
<li><span data-ttu-id="bef73-154">ลักษณะ</span><span class="sxs-lookup"><span data-stu-id="bef73-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="bef73-155">ระดับความสำคัญ 50</span><span class="sxs-lookup"><span data-stu-id="bef73-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="bef73-156">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="bef73-156">Location</span></span></li>
<li><span data-ttu-id="bef73-157">ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bef73-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bef73-158">ตัวอย่างเช่น เมื่อผู้ปฏิบัติงานคลังสินค้ากำลังทำงานบนอุปกรณ์เคลื่อนที่ ถ้าข้อมูลเมตาที่จะแสดงในแอพลิเคชันประกอบด้วยฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bef73-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="bef73-159">สินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-159">Item</span></span>
-   <span data-ttu-id="bef73-160">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="bef73-160">Quantity</span></span>
-   <span data-ttu-id="bef73-161">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="bef73-161">Unit of measure</span></span>
-   <span data-ttu-id="bef73-162">คำอธิบายสินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-162">Item description</span></span>
-   <span data-ttu-id="bef73-163">ขนาดและสถานที่</span><span class="sxs-lookup"><span data-stu-id="bef73-163">Size and Location</span></span>

<span data-ttu-id="bef73-164">ตามการตั้งค่าของระดับความสำคัญฟิลด์แอพลิเคชันคลังสินค้าในตารางข้างต้น ข้อมูล 3 แถวต่อไปนี้จะแสดงในหน้างาน:</span><span class="sxs-lookup"><span data-stu-id="bef73-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="bef73-165">แถว 1: สินค้า ปริมาณ หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="bef73-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="bef73-166">แถว 2: คำอธิบายสินค้า</span><span class="sxs-lookup"><span data-stu-id="bef73-166">Row 2: Item description</span></span>
-   <span data-ttu-id="bef73-167">แถว 3: ขนาด</span><span class="sxs-lookup"><span data-stu-id="bef73-167">Row 3: Size</span></span>

<span data-ttu-id="bef73-168">ข้อมูลเมตาที่เหลือ เช่น สถานที่ จะไม่ถูกแสดงในหน้างาน แต่จะแสดงอยู่ในหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="bef73-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="bef73-169">เมื่อต้องการเรียนรู้เพิ่มเติมและดูตัวอย่างของอินเทอร์เฟสผู้ใช้ ให้ดูที่ประกาศบล็อก [การประกาศ Finance and Operations - คลังสินค้า](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)</span><span class="sxs-lookup"><span data-stu-id="bef73-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bef73-170">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bef73-170">Additional resources</span></span>

[<span data-ttu-id="bef73-171">ติดตั้งและเชื่อมต่อแอปการบริหารคลังสินค้าบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="bef73-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]