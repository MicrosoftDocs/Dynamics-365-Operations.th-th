---
title: (RCS) นำเข้าไฟล์ในรูปแบบ XML ที่มีแอททริบิวต์ที่เลือกกำหนดได้
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการที่ผู้ใช้สามารถออกแบบการตั้งค่าคอนฟิกรูปแบบ ER เพื่อนำเข้าไฟล์ในรูปแบบ XML ที่มีแอททริบิวต์ที่เลือกกำหนดได้
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727086"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="24b5c-103">(RCS) นำเข้าไฟล์ในรูปแบบ XML ที่มีแอททริบิวต์ที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="24b5c-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24b5c-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถออกแบบการตั้งค่าคอนฟิกรูปแบบ ER เพื่อนำเข้าไฟล์ในรูปแบบ XML ซึ่งประกอบด้วยแอททริบิวต์ที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="24b5c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="24b5c-105">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="24b5c-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="24b5c-106">ก่อนที่คุณจะเริ่มต้น ให้ดาวน์โหลดและบันทึกไฟล์ IncomingDocumentToLearnHowToHandleOptionalAttributes.xml ภายในเครื่องจาก [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)</span><span class="sxs-lookup"><span data-stu-id="24b5c-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="24b5c-107">ไปที่ **พื้นที่ทำงานทั้งหมด** > **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="24b5c-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="24b5c-108">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="24b5c-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="24b5c-109">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="24b5c-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="24b5c-110">คลิก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="24b5c-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="24b5c-111">สร้างแบบจำลองการจัดโครงแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="24b5c-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="24b5c-112">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="24b5c-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="24b5c-113">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'แบบจำลองที่จะนำเข้าไฟล์ xml'</span><span class="sxs-lookup"><span data-stu-id="24b5c-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="24b5c-114">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="24b5c-115">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="24b5c-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="24b5c-116">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="24b5c-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="24b5c-117">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'ราก'</span><span class="sxs-lookup"><span data-stu-id="24b5c-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="24b5c-118">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="24b5c-118">Click **Add**.</span></span>
8.  <span data-ttu-id="24b5c-119">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="24b5c-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="24b5c-120">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'รายการ'</span><span class="sxs-lookup"><span data-stu-id="24b5c-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="24b5c-121">ในฟิลด์ **ประเภทรายการ** ให้เลือก **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="24b5c-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="24b5c-122">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="24b5c-122">Click **Add**.</span></span>
12. <span data-ttu-id="24b5c-123">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="24b5c-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="24b5c-124">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="24b5c-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="24b5c-125">ในฟิลด์ **ประเภทรายการ** ให้เลือก **สตริง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="24b5c-126">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="24b5c-126">Click **Add**.</span></span>
16. <span data-ttu-id="24b5c-127">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-127">Click **Save**.</span></span>
17. <span data-ttu-id="24b5c-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="24b5c-128">Close the page.</span></span>
18. <span data-ttu-id="24b5c-129">คลิก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="24b5c-129">Click **Change status**.</span></span>
19. <span data-ttu-id="24b5c-130">คลิก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="24b5c-130">Click **Complete**.</span></span>
20. <span data-ttu-id="24b5c-131">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="24b5c-132">สร้างรูปแบบสำหรับการนำเข้าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="24b5c-132">Create a format for data import</span></span>
1.  <span data-ttu-id="24b5c-133">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="24b5c-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="24b5c-134">ในฟิลด์ **สร้าง** ป้อน 'รูปแบบตามแบบจำลองข้อมูล แบบจำลองในการนำเข้าไฟล์ xml'</span><span class="sxs-lookup"><span data-stu-id="24b5c-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="24b5c-135">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'รูปแบบที่จะนำเข้าไฟล์ xml'</span><span class="sxs-lookup"><span data-stu-id="24b5c-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="24b5c-136">เลือก **ใช่** ในฟิลด์ **สนับสนุนการนำเข้าข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="24b5c-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="24b5c-137">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="24b5c-138">ออกแบบรูปแบบเพื่อแยกวิเคราะห์ไฟล์ขาเข้าในรูปแบบ xml</span><span class="sxs-lookup"><span data-stu-id="24b5c-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="24b5c-139">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="24b5c-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="24b5c-140">คลิก **เพิ่มราก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="24b5c-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="24b5c-141">ในแผนภูมิ เลือก **XML\องค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="24b5c-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="24b5c-142">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'ราก'</span><span class="sxs-lookup"><span data-stu-id="24b5c-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="24b5c-143">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-143">Click **OK**.</span></span>
6.  <span data-ttu-id="24b5c-144">คลิก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="24b5c-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="24b5c-145">ในแผนภูมิ เลือก **XML\องค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="24b5c-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="24b5c-146">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'เอกสาร'</span><span class="sxs-lookup"><span data-stu-id="24b5c-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="24b5c-147">ในฟิลด์ **ความหลากหลาย** ให้เลือก **หนึ่งต่อหลายรายการ**</span><span class="sxs-lookup"><span data-stu-id="24b5c-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="24b5c-148">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-148">Click **OK**.</span></span>
11. <span data-ttu-id="24b5c-149">ในแผนภูมิ ให้เลือก **ราก\เอกสาร**</span><span class="sxs-lookup"><span data-stu-id="24b5c-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="24b5c-150">คลิก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="24b5c-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="24b5c-151">ในแผนภูมิ เลือก **XML\แอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="24b5c-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="24b5c-152">ในฟิลด์ **ชื่อ** พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="24b5c-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="24b5c-153">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-153">Click **OK**.</span></span>
16. <span data-ttu-id="24b5c-154">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="24b5c-155">ออกแบบการแม็ปรูปแบบเพื่อบันทึกข้อมูลที่แยกวิเคราะห์ไปยังแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="24b5c-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="24b5c-156">คลิก **แม็ปรูปแบบไปยังแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="24b5c-157">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-157">Click **New**.</span></span>
3. <span data-ttu-id="24b5c-158">ในฟิลด์ **ข้อกำหนด** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="24b5c-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="24b5c-159">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="24b5c-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="24b5c-160">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'การแม็ป'</span><span class="sxs-lookup"><span data-stu-id="24b5c-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="24b5c-161">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-161">Click **Save**.</span></span>
7. <span data-ttu-id="24b5c-162">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="24b5c-162">Click **Designer**.</span></span>
8. <span data-ttu-id="24b5c-163">ในแผนภูมิ ให้ขยาย **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="24b5c-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="24b5c-164">ในแผนภูมิ ให้ขยาย **format\root: XML Element(root)**</span><span class="sxs-lookup"><span data-stu-id="24b5c-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="24b5c-165">ในแผนภูมิ เลือก \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="24b5c-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="24b5c-166">(เอกสาร)\*\*</span><span class="sxs-lookup"><span data-stu-id="24b5c-166">(document)\*\*.</span></span>
11. <span data-ttu-id="24b5c-167">คลิก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-167">Click **Bind**.</span></span>
12. <span data-ttu-id="24b5c-168">ในแผนภูมิ ขยาย \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="24b5c-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="24b5c-169">(เอกสาร)\*\*</span><span class="sxs-lookup"><span data-stu-id="24b5c-169">(document)\*\*.</span></span>
13. <span data-ttu-id="24b5c-170">ในแผนภูมิ เลือก \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="24b5c-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="24b5c-171">(เอกสาร)\รหัส\*\*</span><span class="sxs-lookup"><span data-stu-id="24b5c-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="24b5c-172">ในแผนภูมิ ให้ขยาย **List = format.root.document**</span><span class="sxs-lookup"><span data-stu-id="24b5c-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="24b5c-173">ในแผนภูมิ ให้เลือก **List = format.root.document\Code**</span><span class="sxs-lookup"><span data-stu-id="24b5c-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="24b5c-174">คลิก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-174">Click **Bind**.</span></span>
17. <span data-ttu-id="24b5c-175">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-175">Click **Save**.</span></span>
18. <span data-ttu-id="24b5c-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="24b5c-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="24b5c-177">รันการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="24b5c-177">Run format mapping</span></span>
1. <span data-ttu-id="24b5c-178">คลิก **รัน**</span><span class="sxs-lookup"><span data-stu-id="24b5c-178">Click **Run**.</span></span>
2. <span data-ttu-id="24b5c-179">คลิก **เรียกดู** และเลือก **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**</span><span class="sxs-lookup"><span data-stu-id="24b5c-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="24b5c-180">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="24b5c-181">ไม่มีการนำเข้าไฟล์ที่เลือกเป็นการออกแบบรูปแบบ สันนิษฐานการมีอยู่ของแอททริบิวต์ 'id' สำหรับองค์ประกอบ 'เอกสาร' แต่ไฟล์ที่นำเข้าจะไม่มีแอททริบิวต์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="24b5c-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="24b5c-182">แก้ไขโครงสร้างรูปแบบเพื่อจัดการแอททริบิวต์ xml เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="24b5c-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="24b5c-183">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="24b5c-183">Close the page.</span></span>
2. <span data-ttu-id="24b5c-184">ในแผนภูมิ ให้ขยาย **root\document**</span><span class="sxs-lookup"><span data-stu-id="24b5c-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="24b5c-185">ในแผนภูมิ ให้เลือก **root\document\id**</span><span class="sxs-lookup"><span data-stu-id="24b5c-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="24b5c-186">เลือก **ใช่** ในฟิลด์ **สตริงที่ว่างสำหรับแอททริบิวต์ที่ขาดหายไป**</span><span class="sxs-lookup"><span data-stu-id="24b5c-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="24b5c-187">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="24b5c-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="24b5c-188">รันการแม็ปรูปแบบเพื่อทดสอบการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="24b5c-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="24b5c-189">คลิก **แม็ปรูปแบบไปยังแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="24b5c-190">คลิก **รัน**</span><span class="sxs-lookup"><span data-stu-id="24b5c-190">Click **Run**.</span></span>
3. <span data-ttu-id="24b5c-191">คลิก **เรียกดู** และเลือกไฟล์ **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**</span><span class="sxs-lookup"><span data-stu-id="24b5c-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="24b5c-192">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="24b5c-192">Click **OK**.</span></span>
5. <span data-ttu-id="24b5c-193">ตรวจทานไฟล์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="24b5c-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="24b5c-194">มีการนำเข้าไฟล์ที่เหมือนกันกับการออกแบบรูปแบบ ขณะนี้ให้พิจารณาถึงแอททริบิวต์ 'รหัส' สำหรับองค์ประกอบ 'เอกสาร' เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="24b5c-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
