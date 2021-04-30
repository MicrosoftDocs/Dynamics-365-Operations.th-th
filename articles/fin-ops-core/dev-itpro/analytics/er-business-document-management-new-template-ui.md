---
title: Microsoft Office-อินเทอร์เฟสผู้ใช้รูปแบบของเอกสารใหม่ในการจัดการเอกสารทางธุรกิจ
description: หัวข้อนี้อธิบายวิธีใช้ส่วนติดต่อผู้ใช้ใหม่ ในคุณลักษณะการจัดการเอกสารทางธุรกิจของกรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER)
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881047"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="23374-103">Microsoft Office-อินเทอร์เฟสผู้ใช้รูปแบบของเอกสารใหม่ในการจัดการเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="23374-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23374-104">การจัดการเอกสารทางธุรกิจช่วยให้ผู้ใช้ทางธุรกิจแก้ไขแม่แบบเอกสารทางธุรกิจ โดยใช้บริการ Microsoft 365 หรือแอปพลิเคชัน Microsoft Office บนเดสก์ทอปที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="23374-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="23374-105">การแก้ไขอาจรวมถึงการเปลี่ยนแปลงการออกแบบหรือการปรับใช้งานใหม่หรือผู้ใช้อาจเพิ่มตัวยึดเพื่อรวมข้อมูลเพิ่มเติมโดยไม่ต้องเปลี่ยนโค้ดต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="23374-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="23374-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานในการจัดการเอกสารทางธุรกิจ โปรดดูที่ [ภาพรวมการจัดการเอกสารทางธุรกิจ](er-business-document-management.md)</span><span class="sxs-lookup"><span data-stu-id="23374-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="23374-107">ส่วนติดต่อผู้ใช้ใหม่ (UI) มีความชัดเจนและสะดวกสบายในการใช้งานมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="23374-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="23374-108">พื้นที่ **เอกสารทางธุรกิจ** จะแสดงเฉพาะแม่แบบที่พร้อมใช้งานสำหรับผู้ให้บริการปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="23374-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="23374-109">ใน UI ก่อนหน้านี้ แท็บ **แม่แบบ** จะแสดงรายการแม่แบบทั้งหมดที่พร้อมใช้งานกับตัวให้บริการใดๆ</span><span class="sxs-lookup"><span data-stu-id="23374-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="23374-110">และยังแสดงแม่แบบทั้งหมดที่สร้างขึ้นและแก้ไขโดยผู้ใช้ใด ๆ ที่มีบทบาทเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="23374-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="23374-111">คุณสามารถใช้ปุ่ม **เอกสารใหม่** เพื่อสร้างและแก้ไขแม่แบบในการกำหนดค่ารูปแบบรายงานทางอิเล็กทรอนิกส์ (ER) ที่จัดทำโดยผู้ให้บริการรายอื่น</span><span class="sxs-lookup"><span data-stu-id="23374-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="23374-112">ตัวอย่างในหัวข้อนี้ ผู้ให้บริการ คือ Microsoft</span><span class="sxs-lookup"><span data-stu-id="23374-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="23374-113">หรือคุณสามารถสร้างแม่แบบโดยอัพโหลดแม่แบบของคุณเองในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="23374-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="23374-114">วิดีโอ [การสร้างเอกสารทางธุรกิจใหม่โดยใช้การจัดการเอกสารทางธุรกิจ](https://youtu.be/gAIYl-mM_pw) (ที่แสดงอยู่ข้างต้น) รวมอยู่ใน [เพลย์ลิสต์ Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) ที่มีอยู่ใน YouTube</span><span class="sxs-lookup"><span data-stu-id="23374-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="23374-115">ทำเอกสารใหม่ UI ในการจัดการเอกสารทางธุรกิจให้พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="23374-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="23374-116">ในการเริ่มใช้เอกสารใหม่ UI ในการจัดการเอกสารทางธุรกิจ คุณต้องเปิดใช้งาน **ประสบการณ์การใช้งาน Office-like UI สำหรับคุณลักษณะการจัดการเอกสารธุรกิจ** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="23374-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="23374-117">ทำตามขั้นตอนเหล่านี้เพื่อเปิดคุณลักษณะนี้สำหรับเอนทิตีทางกฎหมายทั้งหมดนี้</span><span class="sxs-lookup"><span data-stu-id="23374-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="23374-118">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** บนแท็บ **ทั้งหมด** ให้เลือก **ประสบการณ์การใช้งาน Office-like UI สำหรับคุณลักษณะการจัดการเอกสารธุรกิจ** ที่อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="23374-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="23374-119">เลือก **เปิดใช้งานเดี๋ยวนี้** เพื่อเปิดใช้งานคุณลักษณะที่เลือก</span><span class="sxs-lookup"><span data-stu-id="23374-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="23374-120">รีเฟรชหน้าเพื่อเข้าถึงคุณลักษณะใหม่</span><span class="sxs-lookup"><span data-stu-id="23374-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="23374-121">แก้ไขแม่แบบที่ผู้ให้บริการรายอื่นเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="23374-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="23374-122">ในพื้นที่ทำงาน **การจัดการเอกสารทางธุรกิจ** เลือก **เอกสารใหม่**</span><span class="sxs-lookup"><span data-stu-id="23374-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![พื้นที่ทำงานของการจัดการเอกสารทางธุรกิจ](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="23374-124">บนแท็บ **เลือก** ให้เลือกเอกสารที่ใช้เป็นแม่แบบ แล้วจึงเลือก **สร้างเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="23374-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![กล่องโต้ตอบเอกสารทางธุรกิจ](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="23374-126">ในกล่องโต้ตอบใหม่ ในฟิลด์ **ชื่อเรื่อง** เปลี่ยนชื่อเรื่องตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="23374-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="23374-127">ข้อความชื่อเรื่องใช้เพื่อตั้งชื่อการกำหนดค่ารูปแบบ ER ใหม่ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="23374-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="23374-128">รุ่นแบบร่างของการกำหนดค่านี้ (**สำเนารายงาน FTI ลูกค้า (GER)**) จะมีแม่แบบที่แก้ไขแล้ว และจะใช้ในการเรียกใช้รูปแบบ ER นี้สำหรับผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="23374-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="23374-129">แม่แบบต้นฉบับจากฐานการกำหนดค่ารูปแบบ ER จะใช้ในการเรียกใช้รูปแบบ ER นี้สำหรับผู้ใช้อื่นๆ ทุกคน</span><span class="sxs-lookup"><span data-stu-id="23374-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="23374-130">ในฟิลด์ **ชื่อ** ให้เปลี่ยนชื่อของการแก้ไขแม่แบบครั้งแรกที่แก้ไขได้ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="23374-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="23374-131">ในฟิลด์ **ข้อคิดเห็น** ให้ปรับปรุงหมายเหตุสำหรับการแก้ไขแม่แบบที่แก้ไขได้ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="23374-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="23374-132">เลือก **ตกลง** เพื่อยืนยันการเริ่มต้นของกระบวนการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="23374-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![กล่องโต้ตอบการสร้างเอกสาร ](./media/BDM_overview_new_template3.png)

<span data-ttu-id="23374-134">ปุ่ม **เอกสารใหม่** ใช้ในการสร้างและแก้ไขแม่แบบในการกำหนดค่ารูปแบบรายงานทางอิเล็กทรอนิกส์ (ER) ที่จัดทำโดยผู้ให้บริการรายอื่น</span><span class="sxs-lookup"><span data-stu-id="23374-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="23374-135">ตัวอย่างในหัวข้อนี้ ผู้ให้บริการ คือ Microsoft</span><span class="sxs-lookup"><span data-stu-id="23374-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="23374-136">เมื่อคุณเลือก **เอกสารใหม่** คุณสามารถดูแม่แบบทั้งหมดที่เป็นของผู้ให้บริการปัจจุบันและผู้ให้บริการรายอื่นได้</span><span class="sxs-lookup"><span data-stu-id="23374-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="23374-137">หลังจากที่คุณเลือกแม่แบบแล้ว แม่แบบจะเปิดให้แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="23374-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="23374-138">จากนั้น เท็มเพลตที่แก้ไขจะถูกจัดเก็บไว้ในการตั้งค่าคอนฟิกรูปแบบ ER ใหม่ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="23374-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="23374-139">อัปโหลดแม่แบบที่ใช้รูปแบบ Excel ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="23374-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="23374-140">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อให้ข้อมูลที่ต้องใช้ก่อนที่คุณจะอัปโหลดแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="23374-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="23374-141">ในพื้นที่ทำงาน **การจัดการเอกสารทางธุรกิจ** เลือก **เอกสารใหม่**</span><span class="sxs-lookup"><span data-stu-id="23374-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![พื้นที่ทำงานของการจัดการเอกสารทางธุรกิจ](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="23374-143">บนหน้า **สร้างแม่แบบใหม่** บนแท็บ **อัปโหลด** บนแท็บ **แม่แบบ** เลือก **เรียกดู** เพื่อค้นหาและเลือกไฟล์ Excel ที่คุณต้องการใช้เป็นแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="23374-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="23374-144">ในส่วน **แม่แบบ** ฟิลด์ **ชื่อ** และ **คำอธิบาย** จะถูกเติมโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="23374-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="23374-145">ชื่อและข้อความอธิบายของการตั้งค่าคอนฟิกรูปแบบ ER ใหม่ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="23374-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="23374-146">คุณสามารถแก้ไขฟิลด์เหล่านี้ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="23374-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="23374-147">ในส่วน **ชนิดเอกสาร** ในฟิลด์ **ชื่อ** ให้ระบุชนิดของเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="23374-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="23374-148">ค่านี้จะใช้ในการค้นหาแหล่งข้อมูลที่ถูกต้อง (นั่นคือการตั้งค่าคอนฟิกแบบจำลอง ER)</span><span class="sxs-lookup"><span data-stu-id="23374-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![แท็บแม่แบบ](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="23374-150">บนแท็บ **แหล่งข้อมูล** บนแท็บด่วน **ตัวกรอง** เลือก **ใช้ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="23374-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="23374-151">ในส่วน **แหล่งข้อมูล** ฟิลด์ **ชื่อ** จะถูกเติมโดยอัตโนมัติ หรือคุณสามารถเลือกค่าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="23374-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="23374-152">คุณสามารถใช้ตัวกรองข้อมูลเพื่อค้นหาชื่อแหล่งข้อมูลที่เหมาะสมตามชื่อ อธิบาย รหัสประเทศ/ภูมิภาค และชนิดเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="23374-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![แท็บแหล่งข้อมูล](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="23374-154">แท็บด่วน **ตัวกรอง** ใช้ในการค้นหาแหล่งข้อมูลที่ถูกต้อง (นั่นคือการตั้งค่าคอนฟิกแบบจำลอง ER)</span><span class="sxs-lookup"><span data-stu-id="23374-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="23374-155">คุณสามารถแก้ไขฟิลด์ตัวกรองข้อมูลทั้งหมดเพื่อค้นหาแหล่งข้อมูลที่เหมาะสมที่สุดของเอกสารที่คุณอัปโหลดอยู่</span><span class="sxs-lookup"><span data-stu-id="23374-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="23374-156">เงื่อนไขบนแท็บด่วน **ตัวกรอง** จะใช้เป็นเงื่อนไข **OR**</span><span class="sxs-lookup"><span data-stu-id="23374-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="23374-157">บนแท็บ **การแม็ป** ให้เลือก **ตรวจอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="23374-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="23374-158">ฟิลด์ **คำนิยามราก** จะถูกเติมโดยอัตโนมัติ หรือคุณสามารถเลือกค่าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="23374-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="23374-159">แท็บนี้จะแสดงการแม็ปสิ้นสุดสำหรับองค์ประกอบจากแม่แบบและแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="23374-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![แท็บการแม็ป](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="23374-161">การแม็ปในส่วน **โครงสร้างแม่แบบ** ใช้การจับคู่เต็มของป้ายชื่อหรืออธิบายในแหล่งข้อมูลในภาษาของผู้ใช้ และในชื่อเซลล์ในแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="23374-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="23374-162">เลือก **สร้างเอกสาร** เพื่อยืนยันว่าคุณต้องการสร้างแม่แบบและเริ่มต้นกระบวนการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="23374-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="23374-163">สำหรับข้อมูลเพิ่มเติม ดู [ภาพรวมการจัดการเอกสารทางธุรกิจ](er-business-document-management.md)</span><span class="sxs-lookup"><span data-stu-id="23374-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="23374-164">ถ้าไม่มีผู้ให้บริการในการรายงานทางอิเล็กทรอนิกส์ คุณสามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="23374-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="23374-165">ถ้าไม่มีตัวให้บริการที่ใช้งานอยู่ คุณสามารถเลือกที่จะเรียกใช้ตัวให้บริการได้</span><span class="sxs-lookup"><span data-stu-id="23374-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="23374-166">เมื่อต้องการสร้างตัวให้บริการ ให้เปลี่ยนชื่อตัวให้บริการในฟิลด์ **ชื่อ** ให้อัปเดตที่อยู่อินเทอร์เน็ตของผู้ให้บริการใหม่ในฟิลด์ **ที่อยู่อินเทอร์เน็ต** และเลือก **ตกลง** เพื่อยืนยัน</span><span class="sxs-lookup"><span data-stu-id="23374-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![สร้างตัวให้บริการใหม่ใน BDM](./media/bdm_create_provider.png)
    
- <span data-ttu-id="23374-168">เมื่อต้องการเรียกใช้ผู้ให้บริการที่มีอยู่ ให้เลือกชื่อของผู้ให้บริการในฟิลด์ **ผู้ให้บริการการตั้งค่าคอนฟิก** และเลือก **ตกลง** เพื่อตั้งค่าผู้ให้บริการเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="23374-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![เรียกใช้ตัวให้บริการใน BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="23374-170">แต่ละแม่แบบ BDM จะอ้างถึงตัวให้บริการให้เป็นผู้สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="23374-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="23374-171">นี่คือเหตุที่ตัวให้บริการที่ใช้งานอยู่จึงถูกต้องใช้ในแม่แบบนี้</span><span class="sxs-lookup"><span data-stu-id="23374-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
