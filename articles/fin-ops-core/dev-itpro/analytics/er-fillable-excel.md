---
title: ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างเอกสารในรูปแบบ Excel
description: หัวข้อนี้อธิบายวิธีการออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่จะกรอกข้อมูลในเท็มเพลต Excel แล้วสร้างเอกสารการจัดรูปแบบของ Excel ขาออก
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8d6a18741d57829d1929fb8362dc4ba8e03a1bd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094040"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="6bbdc-103">ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างเอกสารในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6bbdc-104">คุณสามารถออกแบบการตั้งค่าคอนฟิกรูปแบบ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) ที่มี [ส่วนประกอบของรูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) ER ซึ่งคุณสามารถตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออกในรูปแบบสมุดงาน Microsoft Excel ได้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="6bbdc-105">ส่วนประกอบของรูปแบบ ER เฉพาะต้องใช้สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="6bbdc-106">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับลักษณะการทำงานนี้ ให้ทำตามขั้นตอนในหัวข้อ [ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML](tasks/er-design-reports-openxml-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="6bbdc-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="6bbdc-107">เพิ่มรูปแบบ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="6bbdc-107">Add a new ER format</span></span>

<span data-ttu-id="6bbdc-108">เมื่อคุณเพิ่มการตั้งค่าคอนฟิกรูปแบบ ER ใหม่เพื่อสร้างเอกสารขาออกในรูปแบบสมุดงาน Excel คุณต้องเลือกค่า **Excel** สำหรับแอททริบิวต์ **ชนิดรูปแบบ** ของรูปแบบหรือปล่อยให้แอททริบิวต์ของ **ชนิดรูปแบบ** ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6bbdc-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="6bbdc-109">ถ้าคุณเลือก **Excel** คุณสามารถตั้งค่าคอนฟิกรูปแบบเพื่อสร้างเอกสารขาออกในรูปแบบ Excel เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="6bbdc-110">ถ้าคุณปล่อยให้แอททริบิวต์ว่างเปล่า คุณสามารถตั้งค่าคอนฟิกรูปแบบเพื่อสร้างเอกสารขาออกในรูปแบบใดๆ ที่ได้รับการสนับสนุนโดยกรอบงาน ER</span><span class="sxs-lookup"><span data-stu-id="6bbdc-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="6bbdc-111">เมื่อต้องการตั้งค่าคอนฟิกส่วนประกอบของรูปแบบ ER ของการตั้งค่าคอนฟิก ให้เลือก **ตัวออกแบบ** บนบานหน้าต่างการดำเนินการและเปิดส่วนประกอบรูปแบบ ER เพื่อแก้ไขในตัวออกแบบการดำเนินงาน ER</span><span class="sxs-lookup"><span data-stu-id="6bbdc-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![เพจการตั้งค่าคอนฟิก](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="6bbdc-113">ส่วนประกอบไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="6bbdc-114">ป้อนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6bbdc-114">Manual entry</span></span>

<span data-ttu-id="6bbdc-115">คุณต้องเพิ่มส่วนประกอบของ **Excel\\File** ไปยังรูปแบบ ER ที่กำหนดไว้เพื่อสร้างเอกสารขาออกในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![ส่วนประกอบ Excel\File](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="6bbdc-117">เมื่อต้องการระบุโครงสร้างของเอกสารขาออก ให้แนบสมุดงาน Excel ที่มีส่วนขยาย. xlsx กับส่วนประกอบ **Excel\\File** เป็นเท็มเพลตสำหรับเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="6bbdc-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="6bbdc-118">เมื่อคุณแนบเท็มเพลตด้วยตนเอง คุณต้องใช้ [ชนิดเอกสาร](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) ที่ได้รับการตั้งค่าคอนฟิกไว้สำหรับวัตถุประสงค์ดังกล่าวใน [พารามิเตอร์ ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)</span><span class="sxs-lookup"><span data-stu-id="6bbdc-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![การเพิ่มไฟล์แนบลงในส่วนประกอบ Excel\File](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="6bbdc-120">ถ้าต้องการระบุวิธีการกรอกข้อมูลเท็มเพลตที่แนบเมื่อคุณรันรูปแบบ ER ที่ตั้งค่าคอนฟิก คุณต้องเพิ่มส่วนประกอบ **แผ่นงาน** **ช่วง** และ **เซลล์** ที่ซ้อนกันเข้ากับส่วนประกอบ **Excel\\File**</span><span class="sxs-lookup"><span data-stu-id="6bbdc-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="6bbdc-121">แต่ละส่วนประกอบที่ซ้อนกันต้องเชื่อมโยงกับสินค้าที่มีการระบุชื่อ Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="6bbdc-122">การนำเข้าเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6bbdc-122">Template import</span></span>

<span data-ttu-id="6bbdc-123">คุณสามารถเลือก **นำเข้าจาก Excel** บนแท็บ **นำเข้า** ของบานหน้าต่างการดำเนินการเพื่อนำเข้าเท็มเพลตใหม่ไปยังรูปแบบ ER เปล่า</span><span class="sxs-lookup"><span data-stu-id="6bbdc-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="6bbdc-124">ในตัวอย่างนี้ส่วนประกอบ **Excel\\File** จะถูกสร้างขึ้นโดยอัตโนมัติ และจะมีการแนบเท็มเพลตที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="6bbdc-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="6bbdc-125">ส่วนประกอบ ER ที่จำเป็นทั้งหมดจะถูกสร้างขึ้นโดยอัตโนมัติตามรายการของ Excel ที่มีการระบุชื่อรายการที่ค้นพบ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![เลือก นำเข้าจาก Excel](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="6bbdc-127">ถ้าคุณต้องการสร้างองค์ประกอบ **แผ่นงาน** ที่ไม่จำเป็นในรูปแบบ ER ที่สามารถแก้ไขได้ ให้ตั้งค่าตัวเลือก **สร้างองค์ประกอบของรูปแบบของแผ่นงาน Excel** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6bbdc-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="6bbdc-128">ส่วนประกอบของแผ่นงาน</span><span class="sxs-lookup"><span data-stu-id="6bbdc-128">Sheet component</span></span>

<span data-ttu-id="6bbdc-129">ส่วนประกอบของ **แผ่นงาน** บ่งชี้แผ่นงานของสมุดงาน Excel ที่แนบซึ่งต้องมีการกรอกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6bbdc-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="6bbdc-130">มีการกำหนดชื่อของแผ่นงานในเท็มเพลต Excel ในคุณสมบัติ **แผ่นงาน** ของส่วนประกอบนี้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="6bbdc-131">ส่วนประกอบนี้ไม่จำเป็นต้องระบุสำหรับสมุดงาน Excel ที่มีแผ่นงานเดียว</span><span class="sxs-lookup"><span data-stu-id="6bbdc-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="6bbdc-132">บนแท็บ **การแม็ป** ของตัวออกแบบการดำเนินงาน ER คุณสามารถตั้งค่าคอนฟิกคุณสมบัติ **ที่เปิดใช้งาน** สำหรับส่วนประกอบของ **แผ่นงาน** เพื่อระบุว่าต้องใส่ส่วนประกอบในเอกสารที่สร้างขึ้นหรือไม่:</span><span class="sxs-lookup"><span data-stu-id="6bbdc-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="6bbdc-133">ถ้ามีการตั้งค่าคอนฟิกของนิพจน์ของคุณสมบัติ **ที่เปิดใช้งาน** ให้ส่งคืนเป็น **จริง** ในเวลาที่รัน หรือถ้าไม่มีการตั้งค่าคอนฟิกนิพจน์ใดๆ แผ่นงานที่เหมาะสมจะถูกวางในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="6bbdc-134">ถ้ามีการตั้งค่าคอนฟิกนิพจน์ของคุณสมบัติ **ที่เปิดใช้งาน** เพื่อส่งคืนเป็น **เท็จ** ในเวลาที่รัน เอกสารที่สร้างขึ้นจะไม่มีแผ่นงาน</span><span class="sxs-lookup"><span data-stu-id="6bbdc-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![ตัวอย่างของส่วนประกอบแผ่นงาน](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="6bbdc-136">ส่วนประกอบของช่วง</span><span class="sxs-lookup"><span data-stu-id="6bbdc-136">Range component</span></span>

<span data-ttu-id="6bbdc-137">ส่วนประกอบของ **ช่วง** บ่งชี้ถึงช่วงของ Excel ที่ต้องควบคุมโดยส่วนประกอบ ER นี้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="6bbdc-138">มีการกำหนดช่วงในคุณสมบัติ **ช่วงของ Excel** ของส่วนประกอบนี้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="6bbdc-139">คุณสมบัติ **ทิศทางการจำลอง** ระบุว่าจะมีการทำซ้ำช่วงใดในเอกสารที่สร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="6bbdc-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="6bbdc-140">ถ้าคุณสมบัติ **ทิศทางการจำลอง** ถูกตั้งค่าเป็น **ไม่มีการจำลอง** ช่วง Excel ที่เหมาะสมจะไม่มีการทำซ้ำในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="6bbdc-141">ถ้าคุณสมบัติ **ทิศทางการจำลอง** ถูกตั้งค่าเป็น **แนวตั้ง** ช่วง Excel ที่เหมาะสมจะมีการทำซ้ำในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="6bbdc-142">ทุกช่วงที่จำลองแบบถูกวางไว้ให้ช่วงดั้งเดิมในเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="6bbdc-143">จำนวนของการทำซ้ำจะถูกกำหนดโดยจำนวนของเรกคอร์ดในแหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ที่ผูกกับส่วนประกอบ ER นี้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="6bbdc-144">ถ้าคุณสมบัติ **ทิศทางการจำลอง** ถูกตั้งค่าเป็น **แนวนอน** ช่วง Excel ที่เหมาะสมจะมีการทำซ้ำในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="6bbdc-145">ทุกช่วงที่จำลองแบบถูกวางไว้ทางด้านขวาของช่วงดั้งเดิมในเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="6bbdc-146">จำนวนของการทำซ้ำจะถูกกำหนดโดยจำนวนของเรกคอร์ดในแหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ที่ผูกกับส่วนประกอบ ER นี้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="6bbdc-147">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการจำลองแบบแนวนอน ให้ทำตามขั้นตอนต่างๆ ใน [ใช้ช่วงที่ขยายตามแนวนอนเพื่อเพิ่มคอลัมน์ในรายงานของ Excel แบบไดนามิก](tasks/er-horizontal-1.md)</span><span class="sxs-lookup"><span data-stu-id="6bbdc-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="6bbdc-148">ส่วนประกอบ **ช่วง** อาจมีส่วนประกอบ ER ที่ซ้อนกันอื่นๆ ที่ใช้ในการป้อนค่าในช่วง Excel ที่มีชื่อที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6bbdc-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="6bbdc-149">ถ้าส่วนประกอบใดๆ ของกลุ่ม **ข้อความ** ถูกใช้ในการป้อนค่า ค่าจะถูกป้อนในช่วงของ Excel เป็นค่าข้อความ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6bbdc-150">ใช้รูปแบบนี้เพื่อจัดรูปแบบค่าที่ป้อนตามตำแหน่งที่ตั้งที่กำหนดไว้ในแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="6bbdc-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="6bbdc-151">ถ้าส่วนประกอบ **เซลล์** ของกลุ่ม **Excel** ใช้ในการป้อนค่า จะมีการป้อนค่าในช่วงของ Excel เป็นค่าของชนิดข้อมูลที่กำหนดโดยการรวมของส่วนประกอบ **เซลล์** นั้น (ตัวอย่างเช่น **สตริง** **จริง** หรือ **จำนวนเต็ม**)</span><span class="sxs-lookup"><span data-stu-id="6bbdc-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="6bbdc-152">ใช้รูปแบบนี้เพื่อเปิดใช้งานแอปพลิเคชัน Excel เพื่อจัดรูปแบบค่าที่ป้อนตามตำแหน่งที่ตั้งของคอมพิวเตอร์เฉพาะที่ที่เปิดเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="6bbdc-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="6bbdc-153">บนแท็บ **การแม็ป** ของตัวออกแบบการดำเนินงาน ER คุณสามารถตั้งค่าคอนฟิกคุณสมบัติ **ที่เปิดใช้งาน** สำหรับส่วนประกอบของ **ช่วง** เพื่อระบุว่าต้องใส่ส่วนประกอบในเอกสารที่สร้างขึ้นหรือไม่:</span><span class="sxs-lookup"><span data-stu-id="6bbdc-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="6bbdc-154">ถ้ามีการตั้งค่าคอนฟิกของนิพจน์ของคุณสมบัติ **ที่เปิดใช้งาน** ให้ส่งคืนเป็น **จริง** ในเวลาที่รัน หรือถ้าไม่มีการตั้งค่าคอนฟิกนิพจน์ใดๆ ช่วงที่เหมาะสมจะถูกเติมในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="6bbdc-155">ถ้ามีการตั้งค่าคอนฟิกของนิพจน์ของคุณสมบัติ **ที่เปิดใช้งาน** ให้ส่งคืนเป็น **เท็จ** ในเวลาที่รัน และถ้าช่วงนี้ไม่ได้แสดงถึงแถวหรือคอลัมน์ทั้งหมด ช่วงที่เหมาะสมจะไม่ถูกเติมในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="6bbdc-156">ถ้ามีการตั้งค่าคอนฟิกของนิพจน์ของคุณสมบัติ **ที่เปิดใช้งาน** ให้ส่งคืนเป็น **เท็จ** ในเวลาที่รัน และถ้าช่วงนี้แสดงถึงแถวหรือคอลัมน์ทั้งหมด เอกสารที่สร้างขึ้นจะมีแถวและคอลัมน์เหล่านั้นเป็นแถวและคอลัมน์ที่ซ่อนอยู่</span><span class="sxs-lookup"><span data-stu-id="6bbdc-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="6bbdc-157">ส่วนประกอบเซลล์</span><span class="sxs-lookup"><span data-stu-id="6bbdc-157">Cell component</span></span>

<span data-ttu-id="6bbdc-158">ส่วนประกอบ **เซลล์** ใช้ในการกรอกข้อมูลใน Excel ที่ชื่อเซลล์ รูปร่าง และรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="6bbdc-159">เมื่อต้องการบ่งชี้ว่ามีการระบุชื่อออบเจ็กต์ของ Excel ที่ต้องถูกกรอกข้อมูลโดยส่วนประกอบ ER **เซลล์** คุณต้องระบุชื่อของออบเจ็กต์นั้นในคุณสมบัติ **ช่วงของ Excel** ของส่วนประกอบ **เซลล์**</span><span class="sxs-lookup"><span data-stu-id="6bbdc-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="6bbdc-160">บนแท็บ **การแม็ป** ของตัวออกแบบการดำเนินงาน ER คุณสามารถตั้งค่าคอนฟิกคุณสมบัติ **ที่เปิดใช้งาน** สำหรับส่วนประกอบของ **เซลล์** เพื่อระบุว่าต้องเติมออบเจ็กต์ในเอกสารที่สร้างขึ้นหรือไม่:</span><span class="sxs-lookup"><span data-stu-id="6bbdc-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="6bbdc-161">ถ้ามีการตั้งค่าคอนฟิกของนิพจน์ของคุณสมบัติ **ที่เปิดใช้งาน** ให้ส่งคืนเป็น **จริง** ในเวลาที่รัน หรือถ้าไม่มีการตั้งค่าคอนฟิกนิพจน์ใดๆ ออบเจ็กต์ที่เหมาะสมจะถูกเติมในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="6bbdc-162">การรวมของส่วนประกอบของ **เซลล์** นี้ ระบุค่าที่ถูกวางในออบเจ็กต์ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6bbdc-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="6bbdc-163">ถ้ามีการตั้งค่าคอนฟิกนิพจน์ของคุณสมบัติ **ที่เปิดใช้งาน** เพื่อส่งคืนเป็น **เท็จ** ในเวลาที่รัน จะไม่มีการเติมออบเจ็กต์ที่เหมาะสมในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="6bbdc-164">เมื่อมีการตั้งค่าคอนฟิกส่วนประกอบ **เซลล์** เพื่อป้อนค่าในเซลล์ อาจมีการผูกกับแหล่งข้อมูลที่ส่งคืนค่าของชนิดข้อมูลดั้งเดิม (ตัวอย่างเช่น **สตริง** **จำนวนจริง** หรือ **จำนวนเต็ม**)</span><span class="sxs-lookup"><span data-stu-id="6bbdc-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="6bbdc-165">ในกรณีนี้จะมีการป้อนค่าในเซลล์เป็นค่าของชนิดข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6bbdc-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="6bbdc-166">เมื่อมีการตั้งค่าคอนฟิกส่วนประกอบ **เซลล์** เพื่อป้อนค่าในรูปร่าง Excel อาจมีการผูกกับแหล่งข้อมูลที่ส่งคืนค่าของชนิดข้อมูลดั้งเดิม (ตัวอย่างเช่น **สตริง** **จำนวนจริง** หรือ **จำนวนเต็ม**)</span><span class="sxs-lookup"><span data-stu-id="6bbdc-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="6bbdc-167">ในกรณีนี้จะมีการป้อนค่าในรูปร่าง Excel เป็นข้อความของรูปร่างนั้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="6bbdc-168">สำหรับค่าของชนิดข้อมูลที่ไม่ใช่ **สตริง** การแปลงเป็นข้อความจะถูกทำให้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="6bbdc-169">คุณสามารถตั้งค่าคอนฟิกส่วนประกอบ **เซลล์** ให้กรอกข้อมูลในรูปร่างได้เฉพาะในกรณีที่มีการสนับสนุนคุณสมบัติข้อความของรูปร่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="6bbdc-170">เมื่อมีการตั้งค่าคอนฟิกส่วนประกอบ **เซลล์** เพื่อป้อนค่าในรูปภาพของ Excel อาจมีการผูกกับแหล่งข้อมูลที่ส่งคืนค่าของชนิดข้อมูล **คอนเทนเนอร์** ที่แสดงถึงรูปภาพในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="6bbdc-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="6bbdc-171">ในกรณีนี้จะมีการป้อนค่าในรูปภาพ Excel เป็นรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="6bbdc-172">รูปภาพและรูปร่างของ Excel ทั้งหมดถือเป็นการยึดตามมุมซ้ายด้านบนไปยังเซลล์หรือช่วงของ Excel โดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="6bbdc-173">ถ้าคุณต้องการคัดลอกรูปภาพหรือรูปร่าง Excel คุณต้องตั้งค่าคอนฟิกเซลล์หรือช่วงที่ยึดตามเซลล์หรือช่วงที่ถูกจำลองแบบ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="6bbdc-174">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการฝังรูปภาพและรูปร่าง ให้ดูที่ [ฝังรูปภาพและรูปร่างในเอกสารที่คุณสร้างขึ้นโดยใช้ ER](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="6bbdc-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="6bbdc-175">ส่วนประกอบของตัวแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="6bbdc-175">Page break component</span></span>

<span data-ttu-id="6bbdc-176">ส่วนประกอบ **PageBreak** บังคับ Excel ให้เริ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="6bbdc-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="6bbdc-177">ส่วนประกอบนี้ไม่จำเป็นต้องใช้เมื่อคุณต้องการใช้การแบ่งหน้าเริ่มต้นของ Excel แต่คุณควรใช้ในกรณีที่คุณต้องการให้ Excel ทำตามรูปแบบ ER ของคุณไปยังหน้าโครงสร้าง</span><span class="sxs-lookup"><span data-stu-id="6bbdc-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="6bbdc-178">แก้ไขรูปแบบ ER ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6bbdc-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="6bbdc-179">อัปเดตเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6bbdc-179">Update a template</span></span>

<span data-ttu-id="6bbdc-180">คุณสามารถเลือก **อัปเดตจาก Excel** บนแท็บ **นำเข้า** ของบานหน้าต่างการดำเนินการเพื่ออัปเดตเท็มเพลตไปยังรูปแบบ ER ที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="6bbdc-181">ในระหว่างกระบวนการนี้ เท็มเพลตของส่วนประกอบ **Excel\\File** ที่เลือกจะถูกแทนที่ด้วยเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="6bbdc-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="6bbdc-182">เนื้อหาของรูปแบบ ER ที่สามารถแก้ไขได้จะถูกซิงค์กับเนื้อหาของเท็มเพลต ER ที่อัปเดต</span><span class="sxs-lookup"><span data-stu-id="6bbdc-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="6bbdc-183">ส่วนประกอบรูปแบบ ER ใหม่จะถูกสร้างขึ้นโดยอัตโนมัติสำหรับทุกชื่อ Excel ถ้าไม่พบส่วนประกอบรูปแบบ ER ในรูปแบบที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="6bbdc-184">ส่วนประกอบรูปแบบ ER ทั้งหมดจะถูกลบออกจากรูปแบบ ER ที่สามารถแก้ไขได้ ถ้าไม่พบชื่อ Excel ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6bbdc-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="6bbdc-185">ให้ตั้งค่าตัวเลือก **สร้างองค์ประกอบของรูปแบบของแผ่นงาน Excel** เป็น **ใช่** ถ้าคุณต้องการสร้างองค์ประกอบ **แผ่นงาน** ที่ไม่จำเป็นในรูปแบบ ER ที่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="6bbdc-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="6bbdc-186">ถ้ารูปแบบ ER ที่สามารถแก้ไขได้มีองค์ประกอบ **แผ่นงาน** โดยดั้งเดิม เราขอแนะนำให้คุณตั้งค่าตัวเลือก **สร้างองค์ประกอบของรูปแบบของแผ่นงาน Excel** เป็น **ใช่** เมื่อคุณนำเข้าเท็มเพลตที่อัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="6bbdc-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="6bbdc-187">มิฉะนั้นองค์ประกอบที่ซ้อนกันทั้งหมดขององค์ประกอบ **แผ่นงาน** ต้นฉบับ จะถูกสร้างตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6bbdc-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="6bbdc-188">ดังนั้นการรวมทั้งหมดขององค์ประกอบรูปแบบที่สร้างขึ้นใหม่จะสูญหายในรูปแบบ ER ที่อัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="6bbdc-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![สร้างตัวเลือกองค์ประกอบรูปแบบของแผ่นงาน Excel ในการอัปเดตจากกล่องโต้ตอบ Excel](./media/er-excel-format-update-template.png)

<span data-ttu-id="6bbdc-190">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับลักษณะการทำงานนี้ ให้ทำตามขั้นตอนใน [ปรับเปลี่ยนรูปแบบการรายงานทางอิเล็กทรอนิกส์โดยนำเท็มเพลต Excel ไปใช้อีกครั้ง](modify-electronic-reporting-format-reapply-excel-template.md)</span><span class="sxs-lookup"><span data-stu-id="6bbdc-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="6bbdc-191">ตรวจสอบความถูกต้องของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="6bbdc-191">Validate an ER format</span></span>

<span data-ttu-id="6bbdc-192">เมื่อคุณตรวจสอบความถูกต้องของรูปแบบ ER ที่สามารถแก้ไขได้ ให้ทำการตรวจสอบความสอดคล้องกันเพื่อให้แน่ใจว่าชื่อ Excel มีอยู่ในเท็มเพลต Excel ที่มีการใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="6bbdc-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="6bbdc-193">คุณจะได้รับการแจ้งเตือนเกี่ยวกับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="6bbdc-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="6bbdc-194">สำหรับความไม่สอดคล้องกันบางส่วน ตัวเลือกในการแก้ไขปัญหาโดยอัตโนมัติจะถูกนำเสนอ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![ข้อความแสดงข้อผิดพลาดของการตรวจสอบความถูกต้อง](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a><span data-ttu-id="6bbdc-196">การควบคุมการคำนวณสูตรของ Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-196">Control the calculation of Excel formulas</span></span>

<span data-ttu-id="6bbdc-197">เมื่อมีการสร้างเอกสารขาออกในรูปแบบสมุดงาน Microsoft Excel เซลล์บางเซลล์ของเอกสารนี้อาจประกอบด้วยสูตรของ Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-197">When an outbound document in a Microsoft Excel workbook format is generated, some cells of this document might contain Excel formulas.</span></span> <span data-ttu-id="6bbdc-198">เมื่อเปิดใช้งานลักษณะการทำงาน **เปิดใช้งานการใช้ไลบรารี EPPlus ในกรอบงานการรายงานทางอิเล็กทรอนิกส์** คุณสามารถควบคุมได้ว่าจะคำนวณสูตรด้วยการเปลี่ยนแปลงค่าของ **ตัวเลือกการคำนวณ** ของ [พารามิเตอร์](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) ในแม่แบบ Excel ที่มีการใช้:</span><span class="sxs-lookup"><span data-stu-id="6bbdc-198">When the **Enable usage of EPPlus library in Electronic reporting framework** feature is enabled, you can control when the formulas are calculated by changing the value of the **Calculation Options** [parameter](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) in the Excel template that is being used:</span></span>

- <span data-ttu-id="6bbdc-199">เลือก **อัตโนมัติ** เพื่อคำนวณสูตรทั้งหมดที่ไม่ขึ้นอยู่กับทุกครั้งที่เอกสารที่สร้างขึ้นจะถูกผนวกตามช่วงใหม่ เซลล์ ฯลฯ</span><span class="sxs-lookup"><span data-stu-id="6bbdc-199">Select **Automatic** to recalculate all dependent formulas every time a generated document is appended by new ranges, cells, etc.</span></span>
    >[!NOTE]
    > <span data-ttu-id="6bbdc-200">ซึ่งอาจทำให้เกิดปัญหาประสิทธิภาพสำหรับแม่แบบ Excel ที่มีสูตรที่เกี่ยวข้องหลายสูตร</span><span class="sxs-lookup"><span data-stu-id="6bbdc-200">This might cause a performance issue for Excel templates that contain multiple related formulas.</span></span>
- <span data-ttu-id="6bbdc-201">เลือก **ด้วยตนเอง** เพื่อหลีกเลี่ยงการคำนวณสูตรใหม่เมื่อสร้างเอกสาร</span><span class="sxs-lookup"><span data-stu-id="6bbdc-201">Select **Manual** to avoid formula recalculation when a document is generated.</span></span>
    >[!NOTE]
    > <span data-ttu-id="6bbdc-202">การคำนวณสูตรใหม่จะถูกบังคับด้วยตนเองเมื่อมีการเปิดเอกสารที่สร้างขึ้นสำหรับการแสดงตัวอย่างโดยใช้ Excel</span><span class="sxs-lookup"><span data-stu-id="6bbdc-202">Formula recalculation is manually forced when a generated document is opened for preview using Excel.</span></span>
    > <span data-ttu-id="6bbdc-203">อย่าใช้ตัวเลือกนี้ถ้าคุณตั้งค่าคอนฟิกปลายทางเอ้อซึ่งสันนิษฐานว่าการใช้งานเอกสารที่สร้างขึ้นโดยไม่มีการแสดงตัวอย่างใน Excel (การแปลง PDF การส่งอีเมล์ ฯลฯ) เนื่องจากเอกสารที่สร้างขึ้นอาจไม่มีค่าในเซลล์ที่มีสูตร</span><span class="sxs-lookup"><span data-stu-id="6bbdc-203">Don't use this option if you configure an ER destination that assumes the usage of a generated document without its preview in Excel (PDF conversion, emailing, etc.)because the generated document might not contain values in cells that contain formulas.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6bbdc-204">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6bbdc-204">Additional resources</span></span>

[<span data-ttu-id="6bbdc-205">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6bbdc-205">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="6bbdc-206">ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="6bbdc-206">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="6bbdc-207">แก้ไขรูปแบบการรายงานทางอิเล็กทรอนิกส์ด้วยการใช้เท็มเพลต Excel อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="6bbdc-207">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="6bbdc-208">ใช้ช่วงที่สามารถขยายได้ตามแนวนอนเพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="6bbdc-208">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="6bbdc-209">ฝังข้อมูลและรูปร่างในเอกสารที่คุณสร้างโดยใช้ ER</span><span class="sxs-lookup"><span data-stu-id="6bbdc-209">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="6bbdc-210">ตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อดึงข้อมูลไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="6bbdc-210">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
