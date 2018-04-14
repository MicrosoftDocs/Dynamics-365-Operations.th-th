---
title: "ตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันในแอพลิเคชัน Warehousing"
description: "หัวข้อนี้อธิบายวิธีการกำหนดและการตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันคลังสินค้าและระดับความสำคัญใน Finance and Operations"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5bb469d48af54ec25174a33a4645e4545cd740f1
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="a0b4b-103">ตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันในแอพลิเคชัน Warehousing</span><span class="sxs-lookup"><span data-stu-id="a0b4b-103">Configure app field names in Warehousing app</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="a0b4b-104">หัวข้อนี้อธิบายวิธีการกำหนดและการตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันคลังสินค้าและระดับความสำคัญใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a0b4b-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="a0b4b-105">**หมายเหตุ:** หัวข้อนี้ใช้กับคุณลักษณะในการบริหารคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="a0b4b-106">ไม่สามารถใช้กับคุณลักษณะในการจัดการสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="a0b4b-107">Finance and Operations - คลังสินค้าเป็นแอพลิเคชันที่คุณสามารถใช้เพื่อทำงานในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="a0b4b-108">คุณสามารถกำหนดและตั้งค่าคอนฟิกชื่อฟิลด์ที่ใช้ในแอพลิเคชัน ตลอดจนตั้งค่าคอนฟิกระดับความสำคัญที่ควรจะกำหนดชื่อฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a0b4b-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="a0b4b-109">หัวข้อนี้อธิบายวิธีการกำหนดและการตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันคลังสินค้าและระดับความสำคัญเหล่านี้ และวิธีการใช้ใน Finance and Operations - คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="a0b4b-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกการเชื่อมต่อกับ Finance and Operations - คลังสินค้า ให้ดูบทสอน [ติดตั้งและตั้งค่า Finance and Operations - คลังสินค้า](install-configure-warehousing-app.md)</span><span class="sxs-lookup"><span data-stu-id="a0b4b-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="a0b4b-111">ตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-111">Configure warehouse app field names</span></span>

<span data-ttu-id="a0b4b-112">เมื่อคุณใช้ Finance and Operations - คลังสินค้าบนอุปกรณ์เคลื่อนที่ของคุณ คุณสามารถตั้งค่าคอนฟิกวิธีที่ควรแสดงข้อมูลเมตาของอุปกรณ์ของคุณบนหน้า **ชื่อฟิลด์แอพลิเคชันคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a0b4b-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="a0b4b-113">ในบริษัทใหม่ใน Finance and Operations เลือก **สร้างการตั้งค่าเริ่มต้น** เพื่อสร้างชื่อฟิลด์ทั้งหมดที่จะถูกใช้ในลำดับงานของอุปกรณ์เคลื่อนที่คลังสินค้า และจากนั้นกำหนดโหมดการป้อนข้อมูลและชนิดการป้อนข้อมูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a0b4b-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="a0b4b-114">หลังจากที่คุณได้สร้างชื่อฟิลด์ทั้งหมด คุณสามารถเลือกตัวเลือกข้อมูลป้อนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0b4b-115">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="a0b4b-115">Option</span></span></th>
<th><span data-ttu-id="a0b4b-116">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a0b4b-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0b4b-117">วิธีการป้อนข้อมูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a0b4b-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="a0b4b-118">ตัวเลือกนี้กำหนดว่าควรแสดงฟิลด์การสแกนหรือฟิลด์ป้อนข้อมูลด้วยตนเองสำหรับชื่อฟิลด์ที่เลือกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a0b4b-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="a0b4b-119">ซึ่งเป็นประโยชน์ในการแยกฟิลด์โดยขึ้นอยู่กับว่าบาร์โค้ดถูกใช้สำหรับฟิลด์นั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a0b4b-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="a0b4b-120"><strong>หมายเหตุ:</strong> สำหรับชื่อฟิลด์ที่มีโหมดการป้อนข้อมูลที่คุณต้องการถูกตั้งค่าเป็น <strong>การสแกน</strong> คุณสามารถป้อนข้อมูลด้วยตนเองถ้าไม่สามารถอ่านบาร์โค้ดได้หรือบาร์โค้ดเสียหาย</span><span class="sxs-lookup"><span data-stu-id="a0b4b-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0b4b-121">ชนิดของข้อมูลป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-121">Input type</span></span></td>
<td><span data-ttu-id="a0b4b-122">ตัวเลือกนี้จะกำหนดว่าควรใช้ชนิดการป้อนข้อมูลใดสำหรับชื่อฟิลด์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a0b4b-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="a0b4b-123">มีตัวเลือกสี่อย่าง:</span><span class="sxs-lookup"><span data-stu-id="a0b4b-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="a0b4b-124"><strong>การเลือก</strong> - ประกอบด้วยรายการของตัวเลือกที่ให้เลือก</span><span class="sxs-lookup"><span data-stu-id="a0b4b-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="a0b4b-125">ชื่อฟิลด์ที่มีตัวเลือกนี้จะไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="a0b4b-126"><strong>วันที่</strong> - ชื่อฟิลด์ที่ระบุเป็นวันที่จะแสดงรูปแบบวันที่พร้อมกับป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="a0b4b-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="a0b4b-127">ซึ่งจะช่วยให้ผู้ปฏิบัติงานคลังสินค้าสามารถดูว่าจะป้อนวันที่ในรูปแบบใด</span><span class="sxs-lookup"><span data-stu-id="a0b4b-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="a0b4b-128">ชื่อฟิลด์ที่มีตัวเลือกนี้จะไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="a0b4b-129"><strong>ตัวอักษร</strong> - ถ้ามีการเลือกไว้ แป้นพิมพ์อุปกรณ์จะถูกใช้เมื่อมีการป้อนข้อมูลด้วยตนเองในแอพลิเคชันนี้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="a0b4b-130">สามารถเปลี่ยนประสบการณ์การใช้งานแป้นพิมพ์โดยขึ้นอยู่กับอุปกรณ์ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="a0b4b-131"><strong>ตัวเลข</strong> - สำหรับชื่อฟิลด์ที่ใช้การป้อนข้อมูลตัวเลขเท่านั้น คุณสามารถเลือกตัวเลือกนี้เพื่อแสดงแป้นพิมพ์ตัวเลขแบบกำหนดเองพร้อมกับฟิลด์การป้อนข้อมูลแทนแป้นพิมพ์อุปกรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="a0b4b-132">ตั้งค่าคอนฟิกระดับความสำคัญของฟิลด์แอพลิเคชันคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="a0b4b-133">ในหน้า **ระดับความสำคัญของฟิลด์แอพลิเคชันคลังสินค้า** คุณสามารถใส่ชื่อฟิลด์ไปยังกลุ่มระดับความสำคัญอื่นได้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="a0b4b-134">ซึ่งทำให้สามารถตัดสินใจได้ว่าควรจะแสดงข้อมูลใดในหน้างานหลักเมื่อผู้ปฏิบัติงานคลังสินค้าทำงานโดยใช้แอพลิเคชันนี้</span><span class="sxs-lookup"><span data-stu-id="a0b4b-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="a0b4b-135">ถ้าคุณคลิก **สร้างการตั้งค่าเริ่มต้น** ชุดค่าเริ่มต้นของกลุ่มระดับความสำคัญจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a0b4b-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="a0b4b-136">คุณสามารถสร้างกลุ่มการระดับความสำคัญได้มากเท่าที่จำเป็น แต่ระบบจะแสดงกลุ่มระดับความสำคัญเพียงสามกลุ่มบนหน้างาน</span><span class="sxs-lookup"><span data-stu-id="a0b4b-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="a0b4b-137">เมื่อ Finance and Operations ส่งข้อมูลเมตาไปยังแอพลิเคชัน ระบบจะกำหนดระดับความสำคัญที่เกี่ยวข้องให้กับแต่ละฟิลด์โดยขึ้นอยู่กับกลุ่มของระดับความสำคัญ และแอพลิเคชันจะแสดงระดับความสำคัญสามกลุ่มแรกที่อยู่ในข้อมูลเมตาในหน้างาน</span><span class="sxs-lookup"><span data-stu-id="a0b4b-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="a0b4b-138">ข้อมูลเมตาจำนวนมากที่เหลือจะถูกแสดงในหน้ารายละเอียดรอง</span><span class="sxs-lookup"><span data-stu-id="a0b4b-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="a0b4b-139">ตารางต่อไปนี้แสดงตัวอย่างของระดับความสำคัญ 5 กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="a0b4b-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0b4b-140">กลุ่มระดับความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="a0b4b-140">Priority group</span></span></th>
<th><span data-ttu-id="a0b4b-141">ฟิลด์ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="a0b4b-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="a0b4b-142">ระดับความสำคัญ 10</span><span class="sxs-lookup"><span data-stu-id="a0b4b-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="a0b4b-143">สินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-143">Item</span></span></li>
<li><span data-ttu-id="a0b4b-144">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a0b4b-144">Quantity</span></span></li>
<li><span data-ttu-id="a0b4b-145">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="a0b4b-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="a0b4b-146">ระดับความสำคัญ 20</span><span class="sxs-lookup"><span data-stu-id="a0b4b-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="a0b4b-147">ตำแหน่งคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="a0b4b-147">Cluster position</span></span></li>
<li><span data-ttu-id="a0b4b-148">คลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="a0b4b-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="a0b4b-149">ระดับความสำคัญ 30</span><span class="sxs-lookup"><span data-stu-id="a0b4b-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="a0b4b-150">คำอธิบายสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="a0b4b-151">ระดับความสำคัญ 40</span><span class="sxs-lookup"><span data-stu-id="a0b4b-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="a0b4b-152">โครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a0b4b-152">Configuration</span></span></li>
<li><span data-ttu-id="a0b4b-153">สี</span><span class="sxs-lookup"><span data-stu-id="a0b4b-153">Color</span></span></li>
<li><span data-ttu-id="a0b4b-154">ขนาด</span><span class="sxs-lookup"><span data-stu-id="a0b4b-154">Size</span></span></li>
<li><span data-ttu-id="a0b4b-155">ลักษณะ</span><span class="sxs-lookup"><span data-stu-id="a0b4b-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="a0b4b-156">ระดับความสำคัญ 50</span><span class="sxs-lookup"><span data-stu-id="a0b4b-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="a0b4b-157">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="a0b4b-157">Location</span></span></li>
<li><span data-ttu-id="a0b4b-158">ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="a0b4b-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0b4b-159">ตัวอย่างเช่น เมื่อผู้ปฏิบัติงานคลังสินค้ากำลังทำงานบนอุปกรณ์เคลื่อนที่ ถ้าข้อมูลเมตาที่จะแสดงในแอพลิเคชันประกอบด้วยฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0b4b-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="a0b4b-160">สินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-160">Item</span></span>
-   <span data-ttu-id="a0b4b-161">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a0b4b-161">Quantity</span></span>
-   <span data-ttu-id="a0b4b-162">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="a0b4b-162">Unit of measure</span></span>
-   <span data-ttu-id="a0b4b-163">คำอธิบายสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-163">Item description</span></span>
-   <span data-ttu-id="a0b4b-164">ขนาดและสถานที่</span><span class="sxs-lookup"><span data-stu-id="a0b4b-164">Size and Location</span></span>

<span data-ttu-id="a0b4b-165">ตามการตั้งค่าของระดับความสำคัญฟิลด์แอพลิเคชันคลังสินค้าในตารางข้างต้น ข้อมูล 3 แถวต่อไปนี้จะแสดงในหน้างาน:</span><span class="sxs-lookup"><span data-stu-id="a0b4b-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="a0b4b-166">แถว 1: สินค้า ปริมาณ หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="a0b4b-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="a0b4b-167">แถว 2: คำอธิบายสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-167">Row 2: Item description</span></span>
-   <span data-ttu-id="a0b4b-168">แถว 3: ขนาด</span><span class="sxs-lookup"><span data-stu-id="a0b4b-168">Row 3: Size</span></span>

<span data-ttu-id="a0b4b-169">ข้อมูลเมตาที่เหลือ เช่น สถานที่ จะไม่ถูกแสดงในหน้างาน แต่จะแสดงอยู่ในหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="a0b4b-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="a0b4b-170">เมื่อต้องการเรียนรู้เพิ่มเติมและดูตัวอย่างของส่วนติดต่อผู้ใช้ ให้ดูที่ประกาศบล็อก [การประกาศ Finance and Operations - คลังสินค้า](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)</span><span class="sxs-lookup"><span data-stu-id="a0b4b-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="see-also"></a><span data-ttu-id="a0b4b-171">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="a0b4b-171">See also</span></span>
--------

[<span data-ttu-id="a0b4b-172">ติดตั้งและตั้งค่าคอนฟิก Microsoft Dynamics 365 for Finance and Operations – คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a0b4b-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




