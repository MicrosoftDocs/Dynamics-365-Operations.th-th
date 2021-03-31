---
title: โมดูลแท็บ
description: หัวข้อนี้ครอบคลุมโมดูลแท็บและอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209238"
---
# <a name="tab-module"></a><span data-ttu-id="39f37-103">โมดูลแท็บ</span><span class="sxs-lookup"><span data-stu-id="39f37-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="39f37-104">หัวข้อนี้ครอบคลุมโมดูลแท็บและอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39f37-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="39f37-105">โมดูลแท็บเป็นโมดูลที่เหมือนกับคอนเทนเนอร์ที่ใช้ในการจัดระเบียบข้อมูลบนหน้าไซต์บนแท็บ</span><span class="sxs-lookup"><span data-stu-id="39f37-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="39f37-106">ผู้ใช้สามารถใช้ในหน้าใดก็ได้ที่ต้องแสดงข้อมูลบนแท็บ</span><span class="sxs-lookup"><span data-stu-id="39f37-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="39f37-107">ภายในโมดูลแท็บทั้งหมด สามารถเพิ่มโมดูลรายการแท็บได้ตั้งแต่หนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="39f37-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="39f37-108">แต่ละโมดูลของรายการแท็บจะแสดงถึงแท็บเดียว ในแต่ละโมดูลแท็บจะสามารถเพิ่มโมดูลอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="39f37-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="39f37-109">ไม่มีข้อจำกัดสำหรับชนิดของโมดูลที่สามารถเพิ่มเข้าในโมดูลแท็บได้</span><span class="sxs-lookup"><span data-stu-id="39f37-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="39f37-110">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลแท็บบนหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="39f37-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="39f37-111">ในตัวอย่างนี้ แท็บ **การจัดส่ง** ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="39f37-111">In this example, the **Shipping** tab selected.</span></span>

![ตัวอย่างของโมดูลแท็บ](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="39f37-113">คุณสมบัติของโมดูลแท็บ</span><span class="sxs-lookup"><span data-stu-id="39f37-113">Tab module properties</span></span>

| <span data-ttu-id="39f37-114">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="39f37-114">Property name</span></span> | <span data-ttu-id="39f37-115">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="39f37-115">Values</span></span> | <span data-ttu-id="39f37-116">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="39f37-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="39f37-117">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="39f37-117">Heading</span></span> | <span data-ttu-id="39f37-118">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="39f37-118">Text</span></span> | <span data-ttu-id="39f37-119">คุณสมบัตินี้จะระบุส่วนหัวของข้อความที่ไม่บังคับสำหรับโมดูลแท็บ</span><span class="sxs-lookup"><span data-stu-id="39f37-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="39f37-120">ดัชนีแท็บที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="39f37-120">Active Tab Index</span></span> | <span data-ttu-id="39f37-121">ลำดับ</span><span class="sxs-lookup"><span data-stu-id="39f37-121">Number</span></span> | <span data-ttu-id="39f37-122">คุณสมบัตินี้ระบุแท็บที่ควรเปิดใช้งานโดยค่าเริ่มต้นเมื่อมีการโหลดหน้า</span><span class="sxs-lookup"><span data-stu-id="39f37-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="39f37-123">ถ้าไม่มีการระบุค่า รายการแท็บแรกจะใช้งานโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="39f37-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="39f37-124">คุณสมบัติของโมดูลรายการแท็บ</span><span class="sxs-lookup"><span data-stu-id="39f37-124">Tab item module properties</span></span>

| <span data-ttu-id="39f37-125">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="39f37-125">Property name</span></span> | <span data-ttu-id="39f37-126">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="39f37-126">Values</span></span> | <span data-ttu-id="39f37-127">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="39f37-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="39f37-128">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="39f37-128">Title</span></span> | <span data-ttu-id="39f37-129">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="39f37-129">Text</span></span> | <span data-ttu-id="39f37-130">คุณสมบัตินี้จะระบุชื่อเรื่องของข้อความสำหรับโมดูลรายการแท็บ</span><span class="sxs-lookup"><span data-stu-id="39f37-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="39f37-131">เพิ่มโมดูลแท็บไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="39f37-131">Add a tab module to a page</span></span>

<span data-ttu-id="39f37-132">การเพิ่มโมดูลแท็บไปยังหน้า และตั้งค่าคุณสมบัติ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="39f37-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="39f37-133">ใช้เท็มเพลตการตลาด Fabrikam (หรือเท็มเพลตที่ไม่มีข้อจำกัด) เพื่อสร้างหน้าใหม่ที่ชื่อ **หน้านโยบายร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="39f37-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="39f37-134">ในช่อง **หลัก** ของ **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39f37-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39f37-135">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39f37-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39f37-136">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39f37-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39f37-137">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **แท็บ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39f37-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39f37-138">ในบานหน้าต่างคุณสมบัติของโมดูลแท็บ ให้เลือก **ส่วนหัว** ถัดจากสัญลักษณ์ดินสอ</span><span class="sxs-lookup"><span data-stu-id="39f37-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="39f37-139">ในกล่องโต้ตอบ **หัวเรื่อง** ภายใต้ **ข้อความส่วนหัว** ให้ป้อนข้อความส่วนหัว (ตัวอย่างเช่น **นโยบาย**)</span><span class="sxs-lookup"><span data-stu-id="39f37-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="39f37-140">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39f37-140">Then select **OK**.</span></span>
1. <span data-ttu-id="39f37-141">ในช่อง **แท็บ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39f37-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39f37-142">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายการแท็บ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39f37-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39f37-143">ในบานหน้าต่างคุณสมบัติของโมดูลรายการแท็บที่อยู่ภายใต้ **ชื่อเรื่อง** ให้ป้อนข้อความชื่อเรื่อง (ตัวอย่างเช่น **การส่งคืน**)</span><span class="sxs-lookup"><span data-stu-id="39f37-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="39f37-144">ในช่อง **รายการแท็บ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39f37-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39f37-145">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **บล็อกข้อความ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39f37-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39f37-146">ในบานหน้าต่างคุณสมบัติของโมดูลบล็อกข้อความ ภายใต้ **ข้อความตกแต่ง** ให้ป้อนย่อหน้าของข้อความ</span><span class="sxs-lookup"><span data-stu-id="39f37-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="39f37-147">ในช่อง **แท็บ** ให้เพิ่มโมดูลของรายการแท็บเพิ่มเติมที่มีชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="39f37-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="39f37-148">ในแต่ละโมดูลรายการแท็บ ให้เพิ่มโมดูลบล็อกข้อความที่มีเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="39f37-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="39f37-149">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="39f37-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="39f37-150">หน้าจะแสดงโมดูลแท็บที่มีโมดูลแท็บรายการแท็บที่มีเนื้อหาที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="39f37-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="39f37-151">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="39f37-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39f37-152">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="39f37-152">Additional resources</span></span>

[<span data-ttu-id="39f37-153">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="39f37-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="39f37-154">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="39f37-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="39f37-155">โมดูล Accordion</span><span class="sxs-lookup"><span data-stu-id="39f37-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="39f37-156">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="39f37-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]