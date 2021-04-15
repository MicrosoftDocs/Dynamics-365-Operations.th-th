---
title: โมดูลหีบ
description: หัวข้อนี้ครอบคลุมถึงโมดูลหีบเพลงและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ba973299291276fe48d82360e203ca28f02aaffb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796281"
---
# <a name="accordion-module"></a><span data-ttu-id="d6552-103">โมดูล Accordion</span><span class="sxs-lookup"><span data-stu-id="d6552-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6552-104">หัวข้อนี้ครอบคลุมถึงโมดูลหีบเพลงและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d6552-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d6552-105">โมดูหีบเป็นโมดูลที่คล้ายกับคอนเทนเนอร์ที่ใช้ในการจัดระเบียบข้อมูลหรือโมดูลในหน้าโดยมีความสามารถในการพับเก็บแบบลิ้นชัก</span><span class="sxs-lookup"><span data-stu-id="d6552-105">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="d6552-106">โมดูลหีบสามารถใช้ในหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="d6552-106">An accordion module can be used on any page.</span></span>

<span data-ttu-id="d6552-107">ภายในโมดูลหีบทั้งหมด คุณสามารถเพิ่มโมดูลหีบหนึ่งรายการขึ้นไปได้</span><span class="sxs-lookup"><span data-stu-id="d6552-107">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="d6552-108">แต่ละโมดูลรายการหีบจะแสดงถึงลิ้นชักแบบยุบได้</span><span class="sxs-lookup"><span data-stu-id="d6552-108">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="d6552-109">ภายในโมดูลรายการหีบทั้งหมด คุณสามารถเพิ่มโมดูลได้ตั้งแต่หนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="d6552-109">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="d6552-110">ไม่มีข้อจำกัดสำหรับชนิดของโมดูลที่สามารถเพิ่มเข้าในโมดูลรายการหีบได้</span><span class="sxs-lookup"><span data-stu-id="d6552-110">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="d6552-111">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูหีบที่ใช้ในการจัดระเบียบข้อมูลบนหน้าคำถามที่ถามบ่อย (FAQ) ของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d6552-111">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![ตัวอย่างของโมดูลหีบ](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="d6552-113">คุณสมบัติโมดูลหีบ</span><span class="sxs-lookup"><span data-stu-id="d6552-113">Accordion module properties</span></span>

| <span data-ttu-id="d6552-114">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="d6552-114">Property name</span></span> | <span data-ttu-id="d6552-115">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="d6552-115">Values</span></span> | <span data-ttu-id="d6552-116">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d6552-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d6552-117">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="d6552-117">Heading</span></span> | <span data-ttu-id="d6552-118">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="d6552-118">Text</span></span> | <span data-ttu-id="d6552-119">คุณสมบัตินี้จะระบุส่วนหัวของข้อความที่ไม่บังคับสำหรับโมดูลหีบ</span><span class="sxs-lookup"><span data-stu-id="d6552-119">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="d6552-120">ขยายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d6552-120">Expand All</span></span> | <span data-ttu-id="d6552-121">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d6552-121">**True** or **False**</span></span> | <span data-ttu-id="d6552-122">ถ้ามีการตั้งค่าเป็น **จริง** ฟังก์ชันขยาย/ยุบจะเปิดอยู่เพื่อให้สามารถขยายและยุบรายการทั้งหมดในโมดูลหีบ</span><span class="sxs-lookup"><span data-stu-id="d6552-122">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="d6552-123">ลักษณะการโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="d6552-123">Interaction Style</span></span> | <span data-ttu-id="d6552-124">**อิสระ** หรือ **ขยายรายการเดียวเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="d6552-124">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="d6552-125">คุณสมบัตินี้จะกำหนดลักษณะของการโต้ตอบสำหรับรายการหีบ</span><span class="sxs-lookup"><span data-stu-id="d6552-125">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="d6552-126">ถ้ามีการตั้งค่าเป็น **อิสระ** รายการหีบแต่ละรายการจะถูกขยายหรือยุบโดยอิสระ</span><span class="sxs-lookup"><span data-stu-id="d6552-126">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="d6552-127">ถ้ามีการตั้งค่าให้ **ขยายหนึ่งรายการเท่านั้น** จะสามารถขยายรายการได้เพียงรายการเดียวเท่านั้นในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="d6552-127">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="d6552-128">เมื่อมีการขยายรายการแล้ว จะมีการยุบรายการที่ขยายไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="d6552-128">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="d6552-129">คุณสมบัติโมดูลรายการหีบ</span><span class="sxs-lookup"><span data-stu-id="d6552-129">Accordion item module properties</span></span>

| <span data-ttu-id="d6552-130">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="d6552-130">Property name</span></span> | <span data-ttu-id="d6552-131">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="d6552-131">Values</span></span> | <span data-ttu-id="d6552-132">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d6552-132">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d6552-133">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="d6552-133">Title</span></span> | <span data-ttu-id="d6552-134">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="d6552-134">Text</span></span> | <span data-ttu-id="d6552-135">คุณสมบัตินี้จะระบุหัวเรื่องของข้อความสำหรับโมดูลรายการหีบ</span><span class="sxs-lookup"><span data-stu-id="d6552-135">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="d6552-136">โดยการเลือกภูมิภาคชื่อเรื่อง ผู้ใช้สามารถขยายหรือยุบส่วนได้</span><span class="sxs-lookup"><span data-stu-id="d6552-136">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="d6552-137">ขยายโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d6552-137">Expand by default</span></span> | <span data-ttu-id="d6552-138">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d6552-138">**True** or **False**</span></span> | <span data-ttu-id="d6552-139">ถ้ามีการตั้งค่าเป็น **จริง** จะมีการขยายรายการหีบโดยค่าเริ่มต้นเมื่อมีการโหลดหน้า</span><span class="sxs-lookup"><span data-stu-id="d6552-139">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="d6552-140">เพิ่มโมดูลหีบไปยังหน้า FAQ</span><span class="sxs-lookup"><span data-stu-id="d6552-140">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="d6552-141">การเพิ่มโมดูลหีบไปยังหน้า FAQ และตั้งค่าคุณสมบัติในตัวสร้างไซต์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d6552-141">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d6552-142">ไปที่ **หน้า** และใช้เท็มเพลตการตลาด Fabrikam (หรือเท็มเพลตที่ไม่มีข้อจำกัด) เพื่อสร้างหน้าใหม่ที่ชื่อ **FAQ ของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="d6552-142">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="d6552-143">ในช่อง **หลัก** ของ **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d6552-143">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6552-144">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d6552-144">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6552-145">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d6552-145">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6552-146">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หีบ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d6552-146">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6552-147">ในบานหน้าต่างคุณสมบัติของโมดูลหีบให้เลือก **ส่วนหัว** ถัดจากสัญลักษณ์ดินสอ</span><span class="sxs-lookup"><span data-stu-id="d6552-147">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="d6552-148">ในกล่องโต้ตอบ **ส่วนหัว** ภายใต้ **ข้อความหัวเรื่อง** ให้ป้อน **คำถามที่ถามบ่อย**</span><span class="sxs-lookup"><span data-stu-id="d6552-148">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="d6552-149">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d6552-149">Then select **OK**.</span></span>
1. <span data-ttu-id="d6552-150">ในบานหน้าต่างคุณสมบัติของโมดูลหีบ ให้เลือกกล่องกาเครื่องหมาย **แสดงขยายทั้งหมด** จากนั้นในฟิลด์ **ลักษณะการโต้ตอบ** ให้เลือก **อิสระ**</span><span class="sxs-lookup"><span data-stu-id="d6552-150">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="d6552-151">ในช่อง **หีบ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d6552-151">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6552-152">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายการหีบ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d6552-152">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6552-153">ในบานหน้าต่างคุณสมบัติของโมดูรายการหีบที่อยู่ภายใต้ **ชื่อเรื่อง** ให้ป้อนข้อความชื่อเรื่อง (ตัวอย่างเช่น **การส่งคืนทำงานอย่างไร**)</span><span class="sxs-lookup"><span data-stu-id="d6552-153">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="d6552-154">ในช่อง **รายการหีบ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d6552-154">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6552-155">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **บล็อกข้อความ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d6552-155">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6552-156">ในบานหน้าต่างคุณสมบัติของโมดูลบล็อกข้อความ ให้ป้อนย่อหน้าของข้อความ (ตัวอย่างเช่น **ต้องประมวลผลการส่งคืนผ่านทางศูนย์บริการ ติดต่อ 1-800-FABRIKAM สำหรับการส่งคืน ผลิตภัณฑ์มีนโยบายการส่งคืน 30 วัน ต้องเริ่มต้นการส่งคืนภายในกรอบเวลานี้**)</span><span class="sxs-lookup"><span data-stu-id="d6552-156">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="d6552-157">ในช่อง **หีบ** ให้เพิ่มโมดูลรายการหีบเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d6552-157">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="d6552-158">ในแต่ละโมดูลหีบรายการ ให้เพิ่มโมดูลบล็อกข้อความที่มีเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="d6552-158">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="d6552-159">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="d6552-159">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d6552-160">หน้าจะแสดงโมดูลหีบที่มีเนื้อหาที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d6552-160">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="d6552-161">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d6552-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6552-162">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d6552-162">Additional resources</span></span>

[<span data-ttu-id="d6552-163">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="d6552-163">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d6552-164">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="d6552-164">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d6552-165">โมดูลแท็บ</span><span class="sxs-lookup"><span data-stu-id="d6552-165">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="d6552-166">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="d6552-166">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]