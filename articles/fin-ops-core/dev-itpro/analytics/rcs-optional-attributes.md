---
title: นำเข้าไฟล์ในรูปแบบ XML ที่มีแอททริบิวต์ตัวเลือก
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการออกแบบรูปแบบ ER ซึ่งระบุแอททริบิวต์ XML เพื่อแยกเอกสารอิเล็กทรอนิกส์ขาเข้าในรูปแบบ XML
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 10795c90cb90961c17a4326b71ed43dc72039f2b
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117436"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="52739-103">นำเข้าไฟล์ในรูปแบบ XML ที่มีแอททริบิวต์ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="52739-103">Import files in XML format with optional attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52739-104">คุณสามารถออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแยกเอกสารอิเล็กทรอนิกส์ขาเข้าในรูปแบบ XML ได้</span><span class="sxs-lookup"><span data-stu-id="52739-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="52739-105">สามารถระบุแอททริบิวต์บางอย่างขององค์ประกอบ XML ในรูปแบบ ER เป็นแบบไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="52739-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="52739-106">ซึ่งจะช่วยให้คุณสามารถจัดการกับไฟล์ขาเข้าที่มีและที่ไม่มีแอททริบิวต์ XML ดังกล่าวได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="52739-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="52739-107">จากนั้นคุณสามารถใช้เนื้อหาจากไฟล์เหล่านี้เพื่ออัพเดตข้อมูลแอพลิเคชันได้</span><span class="sxs-lookup"><span data-stu-id="52739-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="52739-108">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการขั้นตอนในหัวข้อ [(RCS) นำเข้าไฟล์ในรูปแบบ XML ที่มีแอททริบิวต์ที่เลือกกำหนดได้](tasks/import-files-xml-format-optional-attributes.md) ให้เสร็จสมบูรณ์ ซึ่งเป็นส่วนหนึ่งของ 7.5.4.3 ได้รับ/พัฒนากระบวนการทางธุรกิจของส่วนประกอบของบริการและโซลูชันด้านไอที (10677)</span><span class="sxs-lookup"><span data-stu-id="52739-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="52739-109">คุณสามารถดาวน์โหลดไฟล์คู่มืองานนี้และไฟล์ตัวอย่างที่เชื่อมโยงได้จาก [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)</span><span class="sxs-lookup"><span data-stu-id="52739-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="52739-110">คำอธิบายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="52739-110">Content description</span></span>       | <span data-ttu-id="52739-111">ไฟล์</span><span class="sxs-lookup"><span data-stu-id="52739-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="52739-112">ไฟล์ตัวอย่างในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="52739-112">Sample file in XML format</span></span> | <span data-ttu-id="52739-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="52739-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="52739-114">คู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="52739-114">Task guide</span></span>                | <span data-ttu-id="52739-115">RCS นำเข้าไฟล์ในรูปแบบ XML ที่มีแอททริบิวต์.axtr ที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="52739-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="52739-116">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถออกแบบการตั้งค่าคอนฟิกรูปแบบ ER เพื่อนำเข้าไฟล์ในรูปแบบ XML ซึ่งประกอบด้วยแอททริบิวต์ที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="52739-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="52739-117">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในขั้นตอนดำเนินการให้เสร็จสมบูรณ์ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="52739-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="52739-118">ก่อนที่คุณจะเริ่มต้น ให้ดาวน์โหลดและบันทึกไฟล์ IncomingDocumentToLearnHowToHandleOptionalAttributes.xml เฉพาะที่จาก Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 )</span><span class="sxs-lookup"><span data-stu-id="52739-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="52739-119">ไปที่ **การจัดการองค์กร** > **พื้นที่ทำงาน** > **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="52739-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="52739-120">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="52739-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="52739-121">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ให้ดำเนินขั้นตอนต่างๆ ในหัวข้อ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="52739-121">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="52739-122">คลิก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="52739-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="52739-123">สร้างแบบจำลองการจัดโครงแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="52739-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="52739-124">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52739-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="52739-125">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'แบบจำลองที่จะนำเข้าไฟล์ xml'</span><span class="sxs-lookup"><span data-stu-id="52739-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="52739-126">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="52739-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="52739-127">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="52739-127">Click **Designer**.</span></span>
5. <span data-ttu-id="52739-128">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52739-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="52739-129">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'ราก'</span><span class="sxs-lookup"><span data-stu-id="52739-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="52739-130">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="52739-130">Click **Add**.</span></span>
8. <span data-ttu-id="52739-131">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52739-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="52739-132">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'รายการ'</span><span class="sxs-lookup"><span data-stu-id="52739-132">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="52739-133">ในฟิลด์ **ประเภทรายการ** ให้เลือก **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="52739-133">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="52739-134">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="52739-134">Click **Add**.</span></span>
12.    <span data-ttu-id="52739-135">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52739-135">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="52739-136">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="52739-136">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="52739-137">ในฟิลด์ **ประเภทรายการ** ให้เลือก **สตริง**</span><span class="sxs-lookup"><span data-stu-id="52739-137">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="52739-138">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="52739-138">Click **Add**.</span></span>
16.    <span data-ttu-id="52739-139">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="52739-139">Click **Save**.</span></span>
17.    <span data-ttu-id="52739-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="52739-140">Close the page.</span></span>
18.    <span data-ttu-id="52739-141">คลิก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="52739-141">Click **Change status**.</span></span>
19.    <span data-ttu-id="52739-142">คลิก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="52739-142">Click **Complete**.</span></span>
20.    <span data-ttu-id="52739-143">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="52739-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="52739-144">สร้างรูปแบบสำหรับการนำเข้าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="52739-144">Create a format for data import</span></span>
1. <span data-ttu-id="52739-145">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52739-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="52739-146">ในฟิลด์ **สร้าง** ป้อน 'รูปแบบตามแบบจำลองข้อมูล แบบจำลองในการนำเข้าไฟล์ xml'</span><span class="sxs-lookup"><span data-stu-id="52739-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="52739-147">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'รูปแบบที่จะนำเข้าไฟล์ xml'</span><span class="sxs-lookup"><span data-stu-id="52739-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="52739-148">เลือก **ใช่** ในฟิลด์ **สนับสนุนการนำเข้าข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="52739-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="52739-149">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="52739-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="52739-150">ออกแบบรูปแบบเพื่อแยกวิเคราะห์ไฟล์ขาเข้าในรูปแบบ xml</span><span class="sxs-lookup"><span data-stu-id="52739-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="52739-151">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="52739-151">Click **Designer**.</span></span>
2. <span data-ttu-id="52739-152">คลิก **เพิ่มราก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52739-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="52739-153">ในแผนภูมิ เลือก **XML\องค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="52739-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="52739-154">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'ราก'</span><span class="sxs-lookup"><span data-stu-id="52739-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="52739-155">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="52739-155">Click **OK**.</span></span>
6. <span data-ttu-id="52739-156">คลิก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52739-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="52739-157">ในแผนภูมิ เลือก **XML\องค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="52739-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="52739-158">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'เอกสาร'</span><span class="sxs-lookup"><span data-stu-id="52739-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="52739-159">ในฟิลด์ **ความหลากหลาย** ให้เลือก **หนึ่งต่อหลายรายการ**</span><span class="sxs-lookup"><span data-stu-id="52739-159">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="52739-160">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="52739-160">Click **OK**.</span></span>
11.    <span data-ttu-id="52739-161">ในแผนภูมิ ให้เลือก **ราก\เอกสาร**</span><span class="sxs-lookup"><span data-stu-id="52739-161">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="52739-162">คลิก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52739-162">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="52739-163">ในแผนภูมิ เลือก **XML\แอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="52739-163">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="52739-164">ในฟิลด์ **ชื่อ** พิมพ์ 'id'</span><span class="sxs-lookup"><span data-stu-id="52739-164">In the **Name** field, type 'id'.</span></span>
15.    <span data-ttu-id="52739-165">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="52739-165">Click **OK**.</span></span>
16.    <span data-ttu-id="52739-166">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="52739-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="52739-167">ออกแบบการแม็ปรูปแบบเพื่อบันทึกข้อมูลที่แยกวิเคราะห์ไปยังแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="52739-167">Design a format mapping to save parsed information to data model</span></span>
1.    <span data-ttu-id="52739-168">คลิก **แม็ปรูปแบบไปยังแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="52739-168">Click **Map format to model**.</span></span>
2.    <span data-ttu-id="52739-169">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="52739-169">Click **New**.</span></span>
3.    <span data-ttu-id="52739-170">ในฟิลด์ **ข้อกำหนด** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="52739-170">In the **Definition** field, enter or select a value.</span></span>
4.    <span data-ttu-id="52739-171">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'การแม็ป'</span><span class="sxs-lookup"><span data-stu-id="52739-171">In the **Name** field, type 'Mapping'.</span></span>
5.    <span data-ttu-id="52739-172">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="52739-172">Click **Save**.</span></span>
6.    <span data-ttu-id="52739-173">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="52739-173">Click **Designer**.</span></span>
7.    <span data-ttu-id="52739-174">ในแผนภูมิ ให้ขยาย **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="52739-174">In the tree, expand **format**.</span></span>
8.    <span data-ttu-id="52739-175">ในแผนภูมิ ให้ขยาย **format\root: XML Element(root)**</span><span class="sxs-lookup"><span data-stu-id="52739-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.    <span data-ttu-id="52739-176">ในแผนภูมิ เลือก \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="52739-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="52739-177">(เอกสาร)\*\*</span><span class="sxs-lookup"><span data-stu-id="52739-177">(document)\*\*.</span></span>
10.    <span data-ttu-id="52739-178">คลิก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="52739-178">Click **Bind**.</span></span>
11.    <span data-ttu-id="52739-179">ในแผนภูมิ ขยาย \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="52739-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="52739-180">(เอกสาร)\*\*</span><span class="sxs-lookup"><span data-stu-id="52739-180">(document)\*\*.</span></span>
12.    <span data-ttu-id="52739-181">ในแผนภูมิ เลือก \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="52739-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="52739-182">(เอกสาร)\รหัส\*\*</span><span class="sxs-lookup"><span data-stu-id="52739-182">(document)\id\*\*.</span></span>
13.    <span data-ttu-id="52739-183">ในแผนภูมิ ให้ขยาย **List = format.root.document**</span><span class="sxs-lookup"><span data-stu-id="52739-183">In the tree, expand **List = format.root.document**.</span></span>
14.    <span data-ttu-id="52739-184">ในแผนภูมิ ให้เลือก **List = format.root.document\Code**</span><span class="sxs-lookup"><span data-stu-id="52739-184">In the tree, select **List = format.root.document\Code**.</span></span>
15.    <span data-ttu-id="52739-185">คลิก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="52739-185">Click **Bind**.</span></span>
16.    <span data-ttu-id="52739-186">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="52739-186">Click **Save**.</span></span>
17.    <span data-ttu-id="52739-187">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="52739-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="52739-188">รันการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="52739-188">Run format mapping</span></span>
1. <span data-ttu-id="52739-189">คลิก **รัน**</span><span class="sxs-lookup"><span data-stu-id="52739-189">Click **Run**.</span></span>
2. <span data-ttu-id="52739-190">คลิก **เรียกดู** และเลือกไฟล์ **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**</span><span class="sxs-lookup"><span data-stu-id="52739-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="52739-191">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="52739-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="52739-192">ไม่มีการนำเข้าไฟล์ที่เลือก เนื่องจากการออกแบบรูปแบบสันนิษฐานการมีอยู่ของแอททริบิวต์ 'รหัส' สำหรับองค์ประกอบ 'เอกสาร' แต่ไฟล์ที่นำเข้าจะไม่มีแอททริบิวต์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="52739-192">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="52739-193">แก้ไขโครงสร้างรูปแบบเพื่อจัดการแอททริบิวต์ xml เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="52739-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="52739-194">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="52739-194">Close the page.</span></span>
2. <span data-ttu-id="52739-195">ในแผนภูมิ ให้ขยาย **root\document**</span><span class="sxs-lookup"><span data-stu-id="52739-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="52739-196">ในแผนภูมิ ให้เลือก **root\document\id**</span><span class="sxs-lookup"><span data-stu-id="52739-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="52739-197">ในฟิลด์ **สตริงที่ว่างสำหรับแอททริบิวต์ที่ขาดหายไป** เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="52739-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="52739-198">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="52739-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="52739-199">รันการแม็ปรูปแบบเพื่อทดสอบการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="52739-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="52739-200">คลิก **แม็ปรูปแบบไปยังแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="52739-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="52739-201">คลิก **รัน**</span><span class="sxs-lookup"><span data-stu-id="52739-201">Click **Run**.</span></span>
3. <span data-ttu-id="52739-202">คลิก **เรียกดู** และเลือกไฟล์ **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**</span><span class="sxs-lookup"><span data-stu-id="52739-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="52739-203">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="52739-203">Click **OK**.</span></span>
5. <span data-ttu-id="52739-204">ตรวจทานไฟล์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="52739-204">Review the generated file.</span></span> <span data-ttu-id="52739-205">โปรดทราบว่ามีการนำเข้าไฟล์ที่เหมือนกัน เนื่องจากในขณะนี้การออกแบบรูปแบบพิจารณาถึงแอททริบิวต์ 'รหัส' สำหรับองค์ประกอบ 'เอกสาร' เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="52739-205">Note that same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>
