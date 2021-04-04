---
title: อัปเดตโครงสร้างของแม่แบบเอกสารทางธุรกิจ
description: หัวข้อนี้จะอธิบายถึงวิธีการอัพเดตโครงสร้างของแม่แบบเอกสารธุรกิจโดยใช้ลักษณะการทำงานการจัดการเอกสารทางธุรกิจ
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 09813115544701ea3fffb6be06114bcdd63c0ba0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570459"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="7b5ee-103">อัปเดตโครงสร้างของแม่แบบเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b5ee-104">ในบานหน้าต่าง **โครงสร้างแม่แบบ** ของโปรแกรมแก้ไขแม่แบบ [การจัดการเอกสารทางธุรกิจ](er-business-document-management.md) คุณสามารถปรับเปลี่ยนแม่แบบเอกสารธุรกิจโดย [การเพิ่มฟิลด์ใหม่](er-bdm-add-field-to-excel-template.md) ลงในแม่แบบใน Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="7b5ee-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="7b5ee-105">หลังจากนั้นจะมีการปรับปรุงโครงสร้างของแม่แบบโดยอัตโนมัติใน Dynamics 365 Finance เพื่อให้สะท้อนถึงการเปลี่ยนแปลงที่คุณทำไว้ในบานหน้าต่าง **โครงสร้างแม่แบบ**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="7b5ee-106">นอกจากนี้คุณยังสามารถแก้ไขแม่แบบได้โดยใช้ฟังก์ชัน Office 365 ออนไลน์</span><span class="sxs-lookup"><span data-stu-id="7b5ee-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="7b5ee-107">ตัวอย่างเช่น คุณสามารถเพิ่มรายการใหม่ที่มีการระบุชื่อ เช่น รูปภาพหรือรูปร่าง ไปยังแผ่นงานที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="7b5ee-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="7b5ee-108">ในกรณีนี้ โครงสร้างของแม่แบบจะไม่ได้รับการอัพเดตโดยอัตโนมัติในการเงิน และสินค้าที่คุณเพิ่มจะไม่ปรากฏในบานหน้าต่าง **โครงสร้างแม่แบบ**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="7b5ee-109">อัพเดตโครงสร้างแม่แบบด้วยตนเองในการเงินโดยเลือก **อัพเดตโครงสร้าง** บนหน้าโปรแกรมแก้ไขแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="7b5ee-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการตัวอย่างต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="7b5ee-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="7b5ee-111">ตัวอย่าง: อัปเดตโครงสร้างของแม่แบบเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="7b5ee-112">ตัวอย่างนี้แสดงวิธีการที่ผู้ดูแลระบบสามารถอัพเดตโครงสร้างของแม่แบบเอกสารธุรกิจในการเงินหลังจากที่มีการปรับเปลี่ยนแม่แบบได้ใน Office Online</span><span class="sxs-lookup"><span data-stu-id="7b5ee-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="7b5ee-113">ส่วนต่อไปนี้อธิบายขั้นตอนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="7b5ee-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="7b5ee-114">การจัดเตรียมแม่แบบเอกสารธุรกิจสำหรับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="7b5ee-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="7b5ee-115">ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ใน [ภาพรวมของการจัดการเอกสารธุรกิจ](er-business-document-management.md)</span><span class="sxs-lookup"><span data-stu-id="7b5ee-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="7b5ee-116">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="7b5ee-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="7b5ee-117">นำเข้าโซลูชัน ER</span><span class="sxs-lookup"><span data-stu-id="7b5ee-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="7b5ee-118">เปิดใช้งานการจัดการเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="7b5ee-119">ตั้งค่าคอนฟิกพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="7b5ee-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="7b5ee-120">แก้ไขแม่แบบเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-120">Edit a business document template</span></span>

1. <span data-ttu-id="7b5ee-121">ในพื้นที่ทำงาน **การจัดการเอกสารทางธุรกิจ** เลือก **เอกสารใหม่**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="7b5ee-122">บนหน้า **สร้างแม่แบบใหม่** ให้เลือกแม่แบบ **ใบแจ้งหนี้ข้อความอิสระ (ตัวอย่าง ER) (Excel)**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="7b5ee-123">เลือก **สร้างเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-123">Select **Create document**.</span></span>
4. <span data-ttu-id="7b5ee-124">ในฟิลด์ **ชื่อ** ให้ป้อน **Litware ตัวอย่างของ FTI**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="7b5ee-125">เลือก **ตกลง** เพื่อสร้างแม่แบบใหม่</span><span class="sxs-lookup"><span data-stu-id="7b5ee-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b5ee-126">หากคุณยังไม่ได้เข้าสู่ระบบ Office Online คุณจะ [ถูกนำไปยังหน้าลงชื่อเข้าใช้ Office 365](er-business-document-management.md#frequently-asked-questions)</span><span class="sxs-lookup"><span data-stu-id="7b5ee-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="7b5ee-127">เมื่อต้องการกลับไปยังสภาพแวดล้อมทางการเงินของคุณ ให้เลือกปุ่ม **ย้อนกลับ** ในเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="7b5ee-128">มีการเปิดแม่แบบใหม่สำหรับการแก้ไขในตัวควบคุมฝังตัวแบบออนไลน์ของ Excel บนหน้าโปรแกรมแก้ไขแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="7b5ee-129">[![การใช้พื้นที่ทำงานการจัดการเอกสารธุรกิจเพื่อเริ่มต้นการแก้ไขแม่แบบเอกสารธุรกิจ](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="7b5ee-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="7b5ee-130">ตรวจทานโครงสร้างปัจจุบันของแม่แบบที่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="7b5ee-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="7b5ee-131">ใน Excel Online บน ribbon บนแท็บ **มุมมอง** ในกลุ่ม **แสดง** เลือก **เส้นตาราง**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="7b5ee-132">ในแม่แบบที่สามารถแก้ไขได้ ให้เลือกสี่เหลี่ยมด้านบนชื่อแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="7b5ee-133">สี่เหลี่ยมนี้เป็นรูปภาพที่ชื่อ **rptHeaderCompLogo**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="7b5ee-134">ถ้าบานหน้าต่าง **โครงสร้างแม่แบบ** ซ่อนอยู่ ให้เลือก **แสดงโครงสร้าง**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="7b5ee-135">ในบานหน้าต่าง **โครงสร้างแม่แบบ** ขยาย **รายงาน \> ใบแจ้งหนี้ \> rptHeader \> rptHeaderPart1**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="7b5ee-136">โปรดสังเกตว่าในโครงสร้างแม่แบบในทางการเงิน รายการ **rptHeaderCompLogo** จะมีการแสดงเป็นรายการรองของ **รายงาน \> ใบแจ้งหนี้ \> rptHeader \> rptHeaderPart1**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="7b5ee-137">[![การใช้พื้นที่ทำงานการจัดการเอกสารธุรกิจเพื่อทบทวนโครงสร้างปัจจุบันของแม่แบบที่สามารถแก้ไขได้](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="7b5ee-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="7b5ee-138">อัปเดตโครงสร้างของเท็มเพลตเอกสารทางธุรกิจโดยการลบรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="7b5ee-139">ใน Excel Online ในแม่แบบที่สามารถแก้ไขได้ ให้เลือกรูปภาพ **rptHeaderCompLogo**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="7b5ee-140">ทำตามขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้เพื่อลบรูปภาพที่เลือกจากแม่แบบที่สามารถแก้ไขได้:</span><span class="sxs-lookup"><span data-stu-id="7b5ee-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="7b5ee-141">เลือกคีย์ **ลบ** บนแป้นพิมพ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="7b5ee-142">เลือกค้างไว้ (หรือคลิกขวา) ที่รูปภาพแล้วเลือก **ตัด**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b5ee-143">ปัจจุบันรายการ **rptHeaderCompLogo** ยังคงอยู่ในโครงสร้างแม่แบบในการเงินถึง แม้ว่ารูปภาพจะไม่รวมอยู่ในแม่แบบ Excel อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="7b5ee-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="7b5ee-144">เลือก **อัพเดตโครงสร้าง** เพื่อซิงค์โครงสร้างของแม่แบบที่สามารถแก้ไขได้ใน Excel และการเงิน</span><span class="sxs-lookup"><span data-stu-id="7b5ee-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="7b5ee-145">ในบานหน้าต่าง **โครงสร้างแม่แบบ** ขยาย **รายงาน \> ใบแจ้งหนี้ \> rptHeader \> rptHeaderPart1**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="7b5ee-146">โปรดสังเกตว่า รายการ **rptHeaderCompLogo** ไม่รวมอยู่ในโครงสร้างแม่แบบในการเงินอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="7b5ee-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="7b5ee-147">[![การใช้พื้นที่ทำงานการจัดการเอกสารธุรกิจเพื่อลบรูปภาพจากแม่แบบเอกสารธุรกิจ](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="7b5ee-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="7b5ee-148">อัปเดตโครงสร้างของแม่แบบเอกสารทางธุรกิจโดยการเพิ่มรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="7b5ee-149">ใน Excel Online บน ribbon บนแท็บ **แทรก** ในกลุ่ม **ภาพประกอบ** เลือก **รูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="7b5ee-150">เลือก **เลือกไฟล์** ไปที่รูปภาพที่คุณต้องการเพิ่ม เลือก แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="7b5ee-151">เลือก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-151">Select **Insert**.</span></span>
4. <span data-ttu-id="7b5ee-152">ย้ายรูปภาพใหม่จนกว่าจะอยู่ในสถานที่ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7b5ee-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="7b5ee-153">ตามค่าเริ่มต้น Excel จะตั้งชื่อรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-153">By default, Excel names the picture.</span></span> <span data-ttu-id="7b5ee-154">ตัวอย่างเช่น อาจใช้ชื่อรูปภาพ **2**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="7b5ee-155">เลือก **อัพเดตโครงสร้าง** เพื่อซิงค์โครงสร้างของแม่แบบที่สามารถแก้ไขได้ใน Excel และการเงิน</span><span class="sxs-lookup"><span data-stu-id="7b5ee-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="7b5ee-156">ในบานหน้าต่าง **โครงสร้างแม่แบบ** ขยาย **รายงาน \> ใบแจ้งหนี้ \> rptHeader \> rptHeaderPart1**</span><span class="sxs-lookup"><span data-stu-id="7b5ee-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="7b5ee-157">โปรดสังเกตว่ารูปภาพใหม่รวมเป็นรายการในโครงสร้างแม่แบบในการเงิน</span><span class="sxs-lookup"><span data-stu-id="7b5ee-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="7b5ee-158">[![การใช้พื้นที่ทำงานการจัดการเอกสารธุรกิจเพื่อเพิ่มรูปภาพแม่แบบเอกสารธุรกิจ](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="7b5ee-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="7b5ee-159">ลิงค์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="7b5ee-159">Related links</span></span>

[<span data-ttu-id="7b5ee-160">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="7b5ee-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7b5ee-161">ภาพรวมของการจัดการเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7b5ee-161">Business document management overview</span></span>](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]