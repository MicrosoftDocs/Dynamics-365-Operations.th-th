---
title: โมดูลแท็บ
description: หัวข้อนี้ครอบคลุมถึงโมดูลแท็บ และอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 60af9b74f7e647e83229e352a03c09d63d0c7902
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417380"
---
# <a name="tab-module"></a><span data-ttu-id="91285-103">โมดูลแท็บ</span><span class="sxs-lookup"><span data-stu-id="91285-103">Tab module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="91285-104">หัวข้อนี้ครอบคลุมถึงโมดูลแท็บ และอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="91285-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="91285-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="91285-105">Overview</span></span>

<span data-ttu-id="91285-106">โมดูลแท็บเป็นโมดูลที่เหมือนกับคอนเทนเนอร์ที่ใช้ในการจัดระเบียบข้อมูลบนหน้าไซต์บนแท็บ</span><span class="sxs-lookup"><span data-stu-id="91285-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="91285-107">ผู้ใช้สามารถใช้ในหน้าใดก็ได้ที่ต้องแสดงข้อมูลบนแท็บ</span><span class="sxs-lookup"><span data-stu-id="91285-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="91285-108">ภายในโมดูลแท็บทั้งหมด สามารถเพิ่มโมดูลรายการแท็บได้ตั้งแต่หนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="91285-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="91285-109">แต่ละโมดูลของรายการแท็บจะแสดงถึงแท็บเดียว ในแต่ละโมดูลแท็บจะสามารถเพิ่มโมดูลอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="91285-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="91285-110">ไม่มีข้อจำกัดสำหรับชนิดของโมดูลที่สามารถเพิ่มเข้าในโมดูลแท็บได้</span><span class="sxs-lookup"><span data-stu-id="91285-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="91285-111">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลแท็บบนหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="91285-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="91285-112">ในตัวอย่างนี้ แท็บ **การจัดส่ง** ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="91285-112">In this example, the **Shipping** tab selected.</span></span>

![ตัวอย่างของโมดูลแท็บ](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="91285-114">คุณสมบัติของโมดูลแท็บ</span><span class="sxs-lookup"><span data-stu-id="91285-114">Tab module properties</span></span>

| <span data-ttu-id="91285-115">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="91285-115">Property name</span></span> | <span data-ttu-id="91285-116">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="91285-116">Values</span></span> | <span data-ttu-id="91285-117">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="91285-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="91285-118">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="91285-118">Heading</span></span> | <span data-ttu-id="91285-119">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="91285-119">Text</span></span> | <span data-ttu-id="91285-120">คุณสมบัตินี้จะระบุส่วนหัวของข้อความที่ไม่บังคับสำหรับโมดูลแท็บ</span><span class="sxs-lookup"><span data-stu-id="91285-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="91285-121">ดัชนีแท็บที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="91285-121">Active Tab Index</span></span> | <span data-ttu-id="91285-122">ลำดับ</span><span class="sxs-lookup"><span data-stu-id="91285-122">Number</span></span> | <span data-ttu-id="91285-123">คุณสมบัตินี้ระบุแท็บที่ควรเปิดใช้งานโดยค่าเริ่มต้นเมื่อมีการโหลดหน้า</span><span class="sxs-lookup"><span data-stu-id="91285-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="91285-124">ถ้าไม่มีการระบุค่า รายการแท็บแรกจะใช้งานโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="91285-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="91285-125">คุณสมบัติของโมดูลรายการแท็บ</span><span class="sxs-lookup"><span data-stu-id="91285-125">Tab item module properties</span></span>

| <span data-ttu-id="91285-126">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="91285-126">Property name</span></span> | <span data-ttu-id="91285-127">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="91285-127">Values</span></span> | <span data-ttu-id="91285-128">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="91285-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="91285-129">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="91285-129">Title</span></span> | <span data-ttu-id="91285-130">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="91285-130">Text</span></span> | <span data-ttu-id="91285-131">คุณสมบัตินี้จะระบุชื่อเรื่องของข้อความสำหรับโมดูลรายการแท็บ</span><span class="sxs-lookup"><span data-stu-id="91285-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="91285-132">เพิ่มโมดูลแท็บไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="91285-132">Add a tab module to a page</span></span>

<span data-ttu-id="91285-133">การเพิ่มโมดูลแท็บไปยังหน้า และตั้งค่าคุณสมบัติ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="91285-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="91285-134">ใช้เท็มเพลตการตลาด Fabrikam (หรือเท็มเพลตที่ไม่มีข้อจำกัด) เพื่อสร้างหน้าใหม่ที่ชื่อ **หน้านโยบายร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="91285-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="91285-135">ในช่อง **หลัก** ของ **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="91285-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91285-136">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="91285-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91285-137">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="91285-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91285-138">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **แท็บ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="91285-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91285-139">ในบานหน้าต่างคุณสมบัติของโมดูลแท็บ ให้เลือก **ส่วนหัว** ถัดจากสัญลักษณ์ดินสอ</span><span class="sxs-lookup"><span data-stu-id="91285-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="91285-140">ในกล่องโต้ตอบ **หัวเรื่อง** ภายใต้ **ข้อความส่วนหัว** ให้ป้อนข้อความส่วนหัว (ตัวอย่างเช่น **นโยบาย**)</span><span class="sxs-lookup"><span data-stu-id="91285-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="91285-141">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="91285-141">Then select **OK**.</span></span>
1. <span data-ttu-id="91285-142">ในช่อง **แท็บ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="91285-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91285-143">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายการแท็บ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="91285-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91285-144">ในบานหน้าต่างคุณสมบัติของโมดูลรายการแท็บที่อยู่ภายใต้ **ชื่อเรื่อง** ให้ป้อนข้อความชื่อเรื่อง (ตัวอย่างเช่น **การส่งคืน**)</span><span class="sxs-lookup"><span data-stu-id="91285-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="91285-145">ในช่อง **รายการแท็บ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="91285-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91285-146">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **บล็อกข้อความ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="91285-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91285-147">ในบานหน้าต่างคุณสมบัติของโมดูลบล็อกข้อความ ภายใต้ **ข้อความตกแต่ง** ให้ป้อนย่อหน้าของข้อความ</span><span class="sxs-lookup"><span data-stu-id="91285-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="91285-148">ในช่อง **แท็บ** ให้เพิ่มโมดูลของรายการแท็บเพิ่มเติมที่มีชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="91285-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="91285-149">ในแต่ละโมดูลรายการแท็บ ให้เพิ่มโมดูลบล็อกข้อความที่มีเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="91285-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="91285-150">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="91285-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="91285-151">หน้าจะแสดงโมดูลแท็บที่มีโมดูลแท็บรายการแท็บที่มีเนื้อหาที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="91285-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="91285-152">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="91285-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91285-153">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="91285-153">Additional resources</span></span>

[<span data-ttu-id="91285-154">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="91285-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="91285-155">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="91285-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="91285-156">โมดูลหีบ</span><span class="sxs-lookup"><span data-stu-id="91285-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="91285-157">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="91285-157">Text block module</span></span>](add-content-rich-block.md)
