---
title: ส่วนติดต่อผู้ใช้เอกสารใหม่ในการจัดการเอกสารทางธุรกิจ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีใช้ส่วนติดต่อผู้ใช้เอกสารใหม่ ในคุณลักษณะการจัดการเอกสารทางธุรกิจของการรายงานทางอิเล็กทรอนิกส์
author: v-anamir
ms.date: 05/12/2019
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
ms.openlocfilehash: 4c430e21e3bf7f1c01c7b60c0bef58fb49c0c601
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748352"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="32c9a-103">อินเทอร์เฟสผู้ใช้ของเอกสารใหม่ในการจัดการเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="32c9a-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32c9a-104">การจัดการเอกสารทางธุรกิจช่วยให้ผู้ใช้ทางธุรกิจแก้ไขแม่แบบเอกสารทางธุรกิจ โดยใช้บริการ Microsoft 365 หรือแอปพลิเคชัน Microsoft Office บนเดสก์ทอปที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="32c9a-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="32c9a-105">การแก้ไขอาจรวมถึงการเปลี่ยนแปลงการออกแบบหรือการปรับใช้งานใหม่หรือผู้ใช้อาจเพิ่มตัวยึดเพื่อรวมข้อมูลเพิ่มเติมโดยไม่ต้องเปลี่ยนโค้ดต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="32c9a-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="32c9a-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานในการจัดการเอกสารทางธุรกิจ โปรดดูที่ [ภาพรวมการจัดการเอกสารทางธุรกิจ](er-business-document-management.md)</span><span class="sxs-lookup"><span data-stu-id="32c9a-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="32c9a-107">ส่วนติดต่อผู้ใช้เอกสารใหม่ (UI) มีความชัดเจนและสะดวกสบายในการใช้งานมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="32c9a-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="32c9a-108">พื้นที่ **เอกสารทางธุรกิจ** จะแสดงเฉพาะแม่แบบที่พร้อมใช้งานสำหรับผู้ให้บริการปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="32c9a-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="32c9a-109">ปุ่ม **เอกสารใหม่** อนุญาตให้ผู้ใช้สร้างและแก้ไขแม่แบบในการกำหนดค่ารูปแบบรายงานทางอิเล็กทรอนิกส์ (ER) ที่จัดทำโดยผู้ให้บริการรายอื่น</span><span class="sxs-lookup"><span data-stu-id="32c9a-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="32c9a-110">ตัวอย่างในหัวข้อนี้ ผู้ให้บริการ คือ Microsoft</span><span class="sxs-lookup"><span data-stu-id="32c9a-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="32c9a-111">ทำเอกสารใหม่ UI ในการจัดการเอกสารทางธุรกิจให้พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="32c9a-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="32c9a-112">ในการเริ่มใช้เอกสารใหม่ UI ในการจัดการเอกสารทางธุรกิจ คุณต้องเปิดใช้งาน **ประสบการณ์การใช้งาน Office-like UI สำหรับคุณลักษณะการจัดการเอกสารธุรกิจ** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="32c9a-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="32c9a-113">ทำตามขั้นตอนเหล่านี้เพื่อเปิดคุณลักษณะนี้สำหรับเอนทิตีทางกฎหมายทั้งหมดนี้</span><span class="sxs-lookup"><span data-stu-id="32c9a-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="32c9a-114">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** บนแท็บ **สร้าง** ให้เลือก **ประสบการณ์การใช้งาน Office-like UI สำหรับคุณลักษณะการจัดการเอกสารธุรกิจ** ที่อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="32c9a-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="32c9a-115">เลือก **เปิดใช้งานเดี๋ยวนี้** เพื่อเปิดใช้งานคุณลักษณะที่เลือก</span><span class="sxs-lookup"><span data-stu-id="32c9a-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="32c9a-116">รีเฟรชหน้าเพื่อเข้าถึงคุณลักษณะใหม่</span><span class="sxs-lookup"><span data-stu-id="32c9a-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="32c9a-117">แก้ไขแม่แบบที่ผู้ให้บริการรายอื่นเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="32c9a-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="32c9a-118">ในพื้นที่ทำงาน **การจัดการเอกสารทางธุรกิจ** เลือก **เอกสารใหม่**</span><span class="sxs-lookup"><span data-stu-id="32c9a-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![พื้นที่ทำงานของการจัดการเอกสารทางธุรกิจ](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="32c9a-120">ในกล่องโต้ตอบ ให้เลือกเอกสารที่ใช้เป็นแม่แบบ แล้วจึงเลือก **สร้างเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="32c9a-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![กล่องโต้ตอบเอกสารทางธุรกิจ](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="32c9a-122">ในกล่องโต้ตอบใหม่ ในฟิลด์ **ชื่อเรื่อง** เปลี่ยนชื่อเรื่องตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="32c9a-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="32c9a-123">ข้อความชื่อเรื่องใช้เพื่อตั้งชื่อการกำหนดค่ารูปแบบ ER ใหม่ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="32c9a-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="32c9a-124">รุ่นแบบร่างของการกำหนดค่านี้ (**สำเนารายงาน FTI ลูกค้า (GER)**) จะมีแม่แบบที่แก้ไขแล้ว และจะใช้ในการเรียกใช้รูปแบบ ER นี้สำหรับผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="32c9a-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="32c9a-125">แม่แบบต้นฉบับจากฐานการกำหนดค่ารูปแบบ ER จะใช้ในการเรียกใช้รูปแบบ ER นี้สำหรับผู้ใช้อื่นๆ ทุกคน</span><span class="sxs-lookup"><span data-stu-id="32c9a-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="32c9a-126">ในฟิลด์ **ชื่อ** ให้เปลี่ยนชื่อของการแก้ไขแม่แบบครั้งแรกที่แก้ไขได้ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="32c9a-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="32c9a-127">ในฟิลด์ **ข้อคิดเห็น** ให้ปรับปรุงหมายเหตุสำหรับการแก้ไขแม่แบบที่แก้ไขได้ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="32c9a-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="32c9a-128">เลือก **ตกลง** เพื่อยืนยันการเริ่มต้นของกระบวนการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="32c9a-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![กล่องโต้ตอบการสร้างเอกสาร ](./media/BDM_overview_new_template3.png)

<span data-ttu-id="32c9a-130">ปุ่ม **เอกสารใหม่** ใช้ในการสร้างและแก้ไขแม่แบบในการกำหนดค่ารูปแบบรายงานทางอิเล็กทรอนิกส์ (ER) ที่จัดทำโดยผู้ให้บริการรายอื่น</span><span class="sxs-lookup"><span data-stu-id="32c9a-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="32c9a-131">ตัวอย่างในหัวข้อนี้ ผู้ให้บริการ คือ Microsoft</span><span class="sxs-lookup"><span data-stu-id="32c9a-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="32c9a-132">เมื่อคุณเลือก **เอกสารใหม่** คุณสามารถดูแม่แบบทั้งหมดที่เป็นของผู้ให้บริการปัจจุบันและผู้ให้บริการรายอื่นได้</span><span class="sxs-lookup"><span data-stu-id="32c9a-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="32c9a-133">หลังจากที่คุณเลือกแม่แบบแล้ว แม่แบบจะเปิดให้แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="32c9a-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="32c9a-134">จากนั้น เท็มเพลตที่แก้ไขจะถูกจัดเก็บไว้ในการตั้งค่าคอนฟิกรูปแบบ ER ใหม่ที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="32c9a-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="32c9a-135">สำหรับข้อมูลเพิ่มเติม ดู [ภาพรวมการจัดการเอกสารทางธุรกิจ](er-business-document-management.md)</span><span class="sxs-lookup"><span data-stu-id="32c9a-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]