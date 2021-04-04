---
title: เพิ่มฟิลด์ใหม่ลงในแม่แบบเอกสารทางธุรกิจใน Microsoft Excel
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการเพิ่มฟิลด์ใหม่ลงในแม่แบบเอกสารทางธุรกิจใน Microsoft Excel โดยใช้คุณลักษณะการจัดการเอกสารทางธุรกิจ
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 6368d763f44c015a6e85652b1880cfd86ff5ba09
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569032"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="3b7c0-103">เพิ่มฟิลด์ใหม่ลงในแม่แบบเอกสารทางธุรกิจใน Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="3b7c0-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3b7c0-104">คุณสามารถเพิ่มฟิลด์ใหม่ให้กับแม่แบบที่ใช้เพื่อสร้างเอกสารทางธุรกิจในรูปแบบ Microsoft Excel ได้</span><span class="sxs-lookup"><span data-stu-id="3b7c0-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="3b7c0-105">คุณสามารถเพิ่มฟิลด์เหล่านี้เป็นตัวยึดตำแหน่งที่จะใช้ในการกรอกเอกสารที่สร้างขึ้นโดยมีข้อมูลที่จำเป็นจากใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="3b7c0-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="3b7c0-106">สำหรับทุกฟิลด์ที่คุณเพิ่ม คุณสามารถระบุการผูกข้อมูลกับแหล่งข้อมูล เพื่อระบุว่าจะป้อนข้อมูลใบสมัครใดจะถูกป้อนในฟิลด์ เมื่อมีการใช้แม่แบบเพื่อสร้างเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="3b7c0-107">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b7c0-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="3b7c0-108">ตัวอย่างนี้แสดงวิธีการอัพเดตแม่แบบ เพื่อกรอกข้อมูลในฟิลด์ในฟอร์มใบแจ้งหนี้ข้อความอิสระที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3b7c0-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="3b7c0-109">ตั้งค่าคอนฟิกการจัดการเอกสารทางธุรกิจเพื่อแก้ไขแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="3b7c0-110">เนื่องจากการจัดการเอกสารทางธุรกิจ (BDM) ถูกสร้างขึ้นที่ด้านบนของกรอบงาน [ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) คุณต้องตั้งค่าคอนฟิกพารามิเตอร์ ER และ BDM ที่จำเป็นก่อนที่คุณจะสามารถเริ่มต้นการทำงานกับ BDM</span><span class="sxs-lookup"><span data-stu-id="3b7c0-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="3b7c0-111">ลงชื่อเข้าใช้อินสแตนซ์ของ Microsoft Dynamics 365 Finance เป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="3b7c0-112">ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์จากตัวอย่างในหัวข้อ [ภาพรวมของการจัดการเอกสารทางธุรกิจ](er-business-document-management.md):</span><span class="sxs-lookup"><span data-stu-id="3b7c0-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="3b7c0-113">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="3b7c0-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="3b7c0-114">เปิด BDM</span><span class="sxs-lookup"><span data-stu-id="3b7c0-114">Turn on BDM.</span></span>

<span data-ttu-id="3b7c0-115">ขณะนี้คุณสามารถเริ่มต้นการใช้ BDM เพื่อแก้ไขแม่แบบเอกสารทางธุรกิจได้</span><span class="sxs-lookup"><span data-stu-id="3b7c0-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="3b7c0-116">นำเข้าโซลูชันของ ERที่มีแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="3b7c0-117">ตัวอย่างในขั้นตอนนี้ใช้โซลูชันของ ER ที่เผยแพร่อย่างเป็นทางการ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="3b7c0-118">คุณต้องนำเข้าการตั้งค่าคอนฟิกของ ER ของโซลูชันนี้ในอินสแตนซ์ปัจจุบันของ Finance</span><span class="sxs-lookup"><span data-stu-id="3b7c0-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="3b7c0-119">การตั้งค่าคอนฟิกรูปแบบของ ER **ใบแจ้งหนี้ข้อความอิสระ (Excel)** ของโซลูชันนี้ประกอบด้วยแม่แบบเอกสารทางธุรกิจในรูปแบบ Excel ที่สามารถแก้ไขได้โดยใช้ BDM</span><span class="sxs-lookup"><span data-stu-id="3b7c0-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="3b7c0-120">นำเข้ารุ่นล่าสุดของการตั้งค่าคอนฟิกการจัดรูปแบบของ ER นี้จาก Microsoft Dynamics Lifecycle Service (LCS)</span><span class="sxs-lookup"><span data-stu-id="3b7c0-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="3b7c0-121">มีการนำเข้าการตั้งค่าคอนฟิกแบบจำลองข้อมูลของ ER และการแม็ปแบบจำลองของ ER โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="3b7c0-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวีธีการนำเข้าการตั้งค่าคอนฟิก ER ดู [จัดการวงจรการใช้งานการตั้งค่าคอนฟิก ER](general-electronic-reporting-manage-configuration-lifecycle.md)</span><span class="sxs-lookup"><span data-stu-id="3b7c0-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![เพจไลบรารีแอสเซทที่ใช้ร่วมกันของ LCS](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="3b7c0-124">แก้ไขแม่แบบเริ่มต้นแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="3b7c0-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="3b7c0-125">ลงชื่อเข้าใช้ในฐานะผู้ใช้ที่มีสิทธิ์เข้าถึงพื้นที่ทำงาน **การจัดการเอกสารทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="3b7c0-126">เปิดพื้นที่ทำงาน **การจัดการเอกสารทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-126">Open the **Business document management** workspace.</span></span>

    ![พื้นที่ทำงานของการจัดการเอกสารทางธุรกิจ](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="3b7c0-128">ในกริด ให้เลือกแม่แบบ **ใบแจ้งหนี้ข้อความอิสระ (Excel)**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="3b7c0-129">ในบานหน้าต่างด้านขวา ให้เลือก **แม่แบบใหม่** เพื่อสร้างแม่แบบใหม่ที่ยึดตามแม่แบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3b7c0-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="3b7c0-130">ในฟิลด์ **ชื่อเรื่อง** ให้ป้อน **ใบแจ้งหนี้ข้อความอิสระ (Excel) Contoso** เป็นชื่อของแม่แบบใหม่</span><span class="sxs-lookup"><span data-stu-id="3b7c0-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="3b7c0-131">เลือก **ตกลง** เพื่อยืนยันการเริ่มต้นของกระบวนการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="3b7c0-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="3b7c0-132">เพจโปรแกรมแก้ไขแม่แบบ BDM ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="3b7c0-132">The BDM template editor page appears.</span></span> <span data-ttu-id="3b7c0-133">คุณสามารถใช้ Microsoft 365 เพื่อแก้ไขแม่แบบที่เลือกแบบออนไลน์ในตัวควบคุมแบบฝัง</span><span class="sxs-lookup"><span data-stu-id="3b7c0-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![เพจโปรแกรมแก้ไขแม่แบบ BDM](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="3b7c0-135">เพิ่มป้ายชื่อสำหรับฟิลด์ใหม่ให้กับแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="3b7c0-136">บนหน้าโปรแกรมแก้ไขแม่แบบ BDM บน Excel ribbon บนแท็บ **มุมมอง** ให้เลือกกล่องกาเครื่องหมาย **หัวข้อและเส้นตาราง** สำหรับแม่แบบ Excel ที่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="3b7c0-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![กล่องกาเครื่องหมายหัวข้อและเส้นตารางที่เลือก](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="3b7c0-138">เลือกเซลล์ **E8:F8**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="3b7c0-139">บน Excel ribbon บนแท็บ **หลัก** เลือก **ผสาน & กึ่งกลาง** เพื่อผสานเซลล์ที่เลือกเข้ากับ **E8:F8** ใหม่ที่ผสาน</span><span class="sxs-lookup"><span data-stu-id="3b7c0-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="3b7c0-140">ในเซลล์ **E8:F8** ที่ผสาน ป้อน **URL**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="3b7c0-141">เลือกเซลล์ **E7:F7** ที่ผสาน เลือก **รูปแบบจิตรกร** แล้วเลือกเซลล์ **E8: F8** ที่ผสาน เพื่อจัดรูปแบบในลักษณะเดียวกับที่ใช้กับเซลล์ **E7: F7** ที่ผสาน</span><span class="sxs-lookup"><span data-stu-id="3b7c0-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![ป้ายชื่อสำหรับฟิลด์ใหม่ที่เพิ่มให้กับแม่แบบ](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="3b7c0-143">การจัดรูปแบบแม่แบบเพื่อจองพื้นที่สำหรับฟิลด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="3b7c0-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="3b7c0-144">บนหน้าโปรแกรมแก้ไขแม่แบบ BDM เลือกเซลล์ **G8:H8** ที่ผสาน</span><span class="sxs-lookup"><span data-stu-id="3b7c0-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="3b7c0-145">บน Excel ribbon บนแท็บ **หลัก** เลือก **ผสาน & กึ่งกลาง** เพื่อผสานเซลล์ที่เลือกเข้ากับ **G8:H8** ใหม่ที่ผสาน</span><span class="sxs-lookup"><span data-stu-id="3b7c0-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="3b7c0-146">เลือกเซลล์ **G7:H7** ที่ผสาน เลือก **รูปแบบจิตรกร** แล้วเลือกเซลล์ **G8:H8** ที่ผสาน เพื่อจัดรูปแบบในลักษณะเดียวกับที่ใช้กับเซลล์ **G7:H7** ที่ผสาน</span><span class="sxs-lookup"><span data-stu-id="3b7c0-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![พื้นที่ที่จองไว้สำหรับฟิลด์ใหม่](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="3b7c0-148">ในฟิลด์กล่อง **ชื่อ** เลือก **CompanyInfo**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="3b7c0-149">ช่วง **CompanyInfo** ของแม่แบบ Excel ปัจจุบัน จะเก็บฟิลด์ทั้งหมดที่จะใช้ในการเติมข้อมูลส่วนหัวของรายงานที่สร้างขึ้น โดยมีรายละเอียดของบริษัทปัจจุบันเป็นฝ่ายผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="3b7c0-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![ช่วง CompanyInfo ที่เลือก](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="3b7c0-151">เพิ่มฟิลด์ใหม่ให้กับแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="3b7c0-152">บนเพจ **โปรแกรมแก้ไขแม่แบบ BDM** บนบานหน้าต่างการดำเนินการ ให้เลือก **แสดงรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="3b7c0-153">ในบานหน้าต่าง **โครงสร้างแม่แบบ** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b7c0-154">คุณต้องปรับปรุงส่วนของแม่แบบที่คุณต้องการใช้เป็นฟิลด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="3b7c0-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="3b7c0-155">คุณได้ทำการปรับปรุงนี้โดยการจัดรูปแบบเซลล์ **G8:H8** ที่ผสาน</span><span class="sxs-lookup"><span data-stu-id="3b7c0-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![การเพิ่มฟิลด์ใหม่ให้กับแม่แบบ](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="3b7c0-157">เลือก **Excel\เซลล์** เพื่อเพิ่มฟิลด์ใหม่เป็นเซลล์ในแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="3b7c0-158">คุณสามารถเลือก **Excel\ช่วง** ถ้าคุณต้องการเพิ่มช่วงใหม่ให้กับแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="3b7c0-159">ช่วงที่ป้อนอาจประกอบด้วยหลายเซลล์</span><span class="sxs-lookup"><span data-stu-id="3b7c0-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="3b7c0-160">คุณสามารถเพิ่มเซลล์เหล่านี้ในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="3b7c0-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="3b7c0-161">โปรดสังเกตว่า แม่แบบ **CompanyInfo** จะถูกเลือกโดยอัตโนมัติในบานหน้าต่าง **โครงสร้างแม่แบบ** เนื่องจากเป็นส่วนประกอบหลักที่เหมาะสมที่สุดในโครงสร้างแม่แบบปัจจุบันสำหรับฟิลด์ที่คุณกำลังเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="3b7c0-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="3b7c0-162">ในฟิลด์ **ช่วงของ Excel** ให้ป้อน **CompanyURL_Value**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="3b7c0-163">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-163">Select **OK**.</span></span>

    ![ฟิลด์ CompanyURL_Value ที่เพิ่มเข้าในโครงสร้างแม่แบบ](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="3b7c0-165">ในบานหน้าต่าง **โครงสร้างแม่แบบ** ให้เลือกปุ่มจุดไข่ปลา (...) แล้วเลือก **แสดงการผูกข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![แสดงการผูกข้อมูลที่เลือก](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="3b7c0-167">ขณะนี้บานหน้าต่าง **โครงสร้างแม่แบบ** จะแสดงแหล่งข้อมูลที่มีอยู่ในรูปแบบของ ER ที่เน้น</span><span class="sxs-lookup"><span data-stu-id="3b7c0-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="3b7c0-168">เลือก **CompanyInfo_Value** เป็นฟิลด์ที่คุณวางแผนที่จะผูกกับแหล่งข้อมูลของรูปแบบของ ER ที่เน้น</span><span class="sxs-lookup"><span data-stu-id="3b7c0-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="3b7c0-169">ในส่วน **แหล่งข้อมูล** ของบานหน้าต่าง **โครงสร้างแม่แบบ** ขยาย **แบบจำลอง \> InvoiceBase \> CompanyInfo**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="3b7c0-170">ภายใต้ **CompanyInfo** เลือกรายการ **WebsiteURI**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![รายการ WebsiteURI ที่เลือก](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="3b7c0-172">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-172">Select **Bind**.</span></span>
11. <span data-ttu-id="3b7c0-173">ในบานหน้าต่าง **โครงสร้างแม่แบบ** เลือก **บันทึก** แล้วปิดเพจโปรแกรมแก้ไขแม่แบบ BDM</span><span class="sxs-lookup"><span data-stu-id="3b7c0-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="3b7c0-174">ในพื้นที่ทำงาน **การจัดการเอกสารทางธุรกิจ** แท็บ **แม่แบบ** ในบานหน้าต่างด้านขวาแสดงแม่แบบที่อัพเดต</span><span class="sxs-lookup"><span data-stu-id="3b7c0-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="3b7c0-175">ในกริด ให้สังเกตว่าฟิลด์ **สถานะ** สำหรับแม่แบบที่แก้ไขถูกเปลี่ยนเป็น **ร่าง** และฟิลด์ **การปรับปรุง** จะไม่ว่างเปล่าอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="3b7c0-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="3b7c0-176">การเปลี่ยนแปลงเหล่านี้บ่งชี้ว่ากระบวนการของการแก้ไขของแม่แบบนี้ได้เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="3b7c0-176">These changes indicate that the process of editing this template has been started.</span></span>

![แม่แบบที่แก้ไขแล้วในพื้นที่ทำงานการจัดการเอกสารธุรกิจ](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="3b7c0-178">ตรวจทานการตั้งค่าบริษัท</span><span class="sxs-lookup"><span data-stu-id="3b7c0-178">Review company settings</span></span>

1.  <span data-ttu-id="3b7c0-179">ไปที่ **การจัดการองค์กร \> องค์กร \> นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="3b7c0-180">บนแท็บด่วน **ข้อมูลการติดต่อ** โปรดตรวจสอบว่ามีการป้อน URL ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="3b7c0-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![URL ของบริษัทที่ป้อนบนหน้านิติบุคคล](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="3b7c0-182">สร้างเอกสารทางธุรกิจเพื่อทดสอบแม่แบบที่อัพเดต</span><span class="sxs-lookup"><span data-stu-id="3b7c0-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="3b7c0-183">ในใบสมัคร ให้เปลี่ยนบริษัทเป็น **USMF** และไปที่ **บัญชีลูกหนี้ \> ใบแจ้งหนี้ \> ใบแจ้งหนี้ข้อความอิสระทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="3b7c0-184">เลือกใบแจ้งหนี้ **FTI-00000002** แล้วจากนั้น เลือก **การจัดการการพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="3b7c0-185">ในบานหน้าต่างด้านซ้าย ให้ขยาย **โมดูล - บัญชีลูกหนี้ \> เอกสาร \> ใบแจ้งหนี้ข้อความอิสระ**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="3b7c0-186">ภายใต้ **ใบแจ้งหนี้ข้อความอิสระ** ให้เลือกระดับ **เอกสารต้นฉบับ** เพื่อระบุขอบเขตของใบแจ้งหนี้สำหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="3b7c0-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="3b7c0-187">ในบานหน้าต่างด้านขวา ในฟิลด์ **รูปแบบรายงาน** ให้เลือกแม่แบบ **ใบแจ้งหนี้ข้อความอิสระ (Excel) Contoso** สำหรับระดับเอกสารที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![แม่แบบใบแจ้งหนี้ข้อความอิสระ (Excel) Contoso ที่เลือก](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="3b7c0-189">กด **Esc** เพื่อปิดหน้าปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3b7c0-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="3b7c0-190">เลือก **พิมพ์ \> ที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="3b7c0-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="3b7c0-191">ดาวน์โหลดเอกสารที่สร้างขึ้น และเปิดเอกสารใน Excel</span><span class="sxs-lookup"><span data-stu-id="3b7c0-191">Download the generated document, and open it in Excel.</span></span>

    ![ใบแจ้งหนี้ข้อความอิสระใน Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="3b7c0-193">เท็มเพลตที่ปรับเปลี่ยนจะถูกใช้ในการสร้างรายงานใบแจ้งหนี้ข้อความอิสระสำหรับรายการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3b7c0-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="3b7c0-194">เมื่อต้องการวิเคราะห์วิธีการที่รายงานนี้ได้รับผลกระทบจากการเปลี่ยนแปลงที่คุณสร้างแม่แบบ รันรายงานนี้ในรอบเวลาของแอพลิเคชันหนึ่งได้ทันที หลังจากที่คุณปรับเปลี่ยนแม่แบบในรอบเวลาของแอพลิเคชันอื่น</span><span class="sxs-lookup"><span data-stu-id="3b7c0-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="3b7c0-195">ลิงค์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3b7c0-195">Related links</span></span>

[<span data-ttu-id="3b7c0-196">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="3b7c0-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="3b7c0-197">ภาพรวมของการจัดการเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3b7c0-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="3b7c0-198">ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="3b7c0-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]