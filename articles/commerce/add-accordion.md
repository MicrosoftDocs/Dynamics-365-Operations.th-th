---
title: โมดูลหีบ
description: หัวข้อนี้ครอบคลุมถึงโมดูลหีบ และอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: e06a0e0289e8c0c718aff4beab2c7a6ceb0a8cb1
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417265"
---
# <a name="accordion-module"></a><span data-ttu-id="39cfb-103">โมดูลหีบ</span><span class="sxs-lookup"><span data-stu-id="39cfb-103">Accordion module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="39cfb-104">หัวข้อนี้ครอบคลุมถึงโมดูลหีบ และอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39cfb-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="39cfb-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="39cfb-105">Overview</span></span>

<span data-ttu-id="39cfb-106">โมดูหีบเป็นโมดูลที่คล้ายกับคอนเทนเนอร์ที่ใช้ในการจัดระเบียบข้อมูลหรือโมดูลในหน้าโดยมีความสามารถในการพับเก็บแบบลิ้นชัก</span><span class="sxs-lookup"><span data-stu-id="39cfb-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="39cfb-107">โมดูลหีบสามารถใช้ในหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="39cfb-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="39cfb-108">ภายในโมดูลหีบทั้งหมด คุณสามารถเพิ่มโมดูลหีบหนึ่งรายการขึ้นไปได้</span><span class="sxs-lookup"><span data-stu-id="39cfb-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="39cfb-109">แต่ละโมดูลรายการหีบจะแสดงถึงลิ้นชักแบบยุบได้</span><span class="sxs-lookup"><span data-stu-id="39cfb-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="39cfb-110">ภายในโมดูลรายการหีบทั้งหมด คุณสามารถเพิ่มโมดูลได้ตั้งแต่หนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="39cfb-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="39cfb-111">ไม่มีข้อจำกัดสำหรับชนิดของโมดูลที่สามารถเพิ่มเข้าในโมดูลรายการหีบได้</span><span class="sxs-lookup"><span data-stu-id="39cfb-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="39cfb-112">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูหีบที่ใช้ในการจัดระเบียบข้อมูลบนหน้าคำถามที่ถามบ่อย (FAQ) ของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="39cfb-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![ตัวอย่างของโมดูลหีบ](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="39cfb-114">คุณสมบัติโมดูลหีบ</span><span class="sxs-lookup"><span data-stu-id="39cfb-114">Accordion module properties</span></span>

| <span data-ttu-id="39cfb-115">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="39cfb-115">Property name</span></span> | <span data-ttu-id="39cfb-116">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="39cfb-116">Values</span></span> | <span data-ttu-id="39cfb-117">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="39cfb-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="39cfb-118">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="39cfb-118">Heading</span></span> | <span data-ttu-id="39cfb-119">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="39cfb-119">Text</span></span> | <span data-ttu-id="39cfb-120">คุณสมบัตินี้จะระบุส่วนหัวของข้อความที่ไม่บังคับสำหรับโมดูลหีบ</span><span class="sxs-lookup"><span data-stu-id="39cfb-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="39cfb-121">ขยายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="39cfb-121">Expand All</span></span> | <span data-ttu-id="39cfb-122">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="39cfb-122">**True** or **False**</span></span> | <span data-ttu-id="39cfb-123">ถ้ามีการตั้งค่าเป็น **จริง** ฟังก์ชันขยาย/ยุบจะเปิดอยู่เพื่อให้สามารถขยายและยุบรายการทั้งหมดในโมดูลหีบ</span><span class="sxs-lookup"><span data-stu-id="39cfb-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="39cfb-124">ลักษณะการโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="39cfb-124">Interaction Style</span></span> | <span data-ttu-id="39cfb-125">**อิสระ** หรือ **ขยายรายการเดียวเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="39cfb-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="39cfb-126">คุณสมบัตินี้จะกำหนดลักษณะของการโต้ตอบสำหรับรายการหีบ</span><span class="sxs-lookup"><span data-stu-id="39cfb-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="39cfb-127">ถ้ามีการตั้งค่าเป็น **อิสระ** รายการหีบแต่ละรายการจะถูกขยายหรือยุบโดยอิสระ</span><span class="sxs-lookup"><span data-stu-id="39cfb-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="39cfb-128">ถ้ามีการตั้งค่าให้ **ขยายหนึ่งรายการเท่านั้น** จะสามารถขยายรายการได้เพียงรายการเดียวเท่านั้นในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="39cfb-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="39cfb-129">เมื่อมีการขยายรายการแล้ว จะมีการยุบรายการที่ขยายไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="39cfb-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="39cfb-130">คุณสมบัติโมดูลรายการหีบ</span><span class="sxs-lookup"><span data-stu-id="39cfb-130">Accordion item module properties</span></span>

| <span data-ttu-id="39cfb-131">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="39cfb-131">Property name</span></span> | <span data-ttu-id="39cfb-132">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="39cfb-132">Values</span></span> | <span data-ttu-id="39cfb-133">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="39cfb-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="39cfb-134">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="39cfb-134">Title</span></span> | <span data-ttu-id="39cfb-135">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="39cfb-135">Text</span></span> | <span data-ttu-id="39cfb-136">คุณสมบัตินี้จะระบุหัวเรื่องของข้อความสำหรับโมดูลรายการหีบ</span><span class="sxs-lookup"><span data-stu-id="39cfb-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="39cfb-137">โดยการเลือกภูมิภาคชื่อเรื่อง ผู้ใช้สามารถขยายหรือยุบส่วนได้</span><span class="sxs-lookup"><span data-stu-id="39cfb-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="39cfb-138">ขยายโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="39cfb-138">Expand by default</span></span> | <span data-ttu-id="39cfb-139">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="39cfb-139">**True** or **False**</span></span> | <span data-ttu-id="39cfb-140">ถ้ามีการตั้งค่าเป็น **จริง** จะมีการขยายรายการหีบโดยค่าเริ่มต้นเมื่อมีการโหลดหน้า</span><span class="sxs-lookup"><span data-stu-id="39cfb-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="39cfb-141">เพิ่มโมดูลหีบไปยังหน้า FAQ</span><span class="sxs-lookup"><span data-stu-id="39cfb-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="39cfb-142">การเพิ่มโมดูลหีบไปยังหน้า FAQ และตั้งค่าคุณสมบัติในตัวสร้างไซต์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="39cfb-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="39cfb-143">ไปที่ **หน้า** และใช้เท็มเพลตการตลาด Fabrikam (หรือเท็มเพลตที่ไม่มีข้อจำกัด) เพื่อสร้างหน้าใหม่ที่ชื่อ **FAQ ของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="39cfb-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="39cfb-144">ในช่อง **หลัก** ของ **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39cfb-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39cfb-145">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39cfb-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39cfb-146">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39cfb-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39cfb-147">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หีบ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39cfb-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39cfb-148">ในบานหน้าต่างคุณสมบัติของโมดูลหีบให้เลือก **ส่วนหัว** ถัดจากสัญลักษณ์ดินสอ</span><span class="sxs-lookup"><span data-stu-id="39cfb-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="39cfb-149">ในกล่องโต้ตอบ **ส่วนหัว** ภายใต้ **ข้อความหัวเรื่อง** ให้ป้อน **คำถามที่ถามบ่อย**</span><span class="sxs-lookup"><span data-stu-id="39cfb-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="39cfb-150">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39cfb-150">Then select **OK**.</span></span>
1. <span data-ttu-id="39cfb-151">ในบานหน้าต่างคุณสมบัติของโมดูลหีบ ให้เลือกกล่องกาเครื่องหมาย **แสดงขยายทั้งหมด** จากนั้นในฟิลด์ **ลักษณะการโต้ตอบ** ให้เลือก **อิสระ**</span><span class="sxs-lookup"><span data-stu-id="39cfb-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="39cfb-152">ในช่อง **หีบ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39cfb-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39cfb-153">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายการหีบ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39cfb-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39cfb-154">ในบานหน้าต่างคุณสมบัติของโมดูรายการหีบที่อยู่ภายใต้ **ชื่อเรื่อง** ให้ป้อนข้อความชื่อเรื่อง (ตัวอย่างเช่น **การส่งคืนทำงานอย่างไร**)</span><span class="sxs-lookup"><span data-stu-id="39cfb-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="39cfb-155">ในช่อง **รายการหีบ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39cfb-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39cfb-156">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **บล็อกข้อความ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39cfb-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39cfb-157">ในบานหน้าต่างคุณสมบัติของโมดูลบล็อกข้อความ ให้ป้อนย่อหน้าของข้อความ (ตัวอย่างเช่น **ต้องประมวลผลการส่งคืนผ่านทางศูนย์บริการ ติดต่อ 1-800-FABRIKAM สำหรับการส่งคืน ผลิตภัณฑ์มีนโยบายการส่งคืน 30 วัน ต้องเริ่มต้นการส่งคืนภายในกรอบเวลานี้**)</span><span class="sxs-lookup"><span data-stu-id="39cfb-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="39cfb-158">ในช่อง **หีบ** ให้เพิ่มโมดูลรายการหีบเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="39cfb-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="39cfb-159">ในแต่ละโมดูลหีบรายการ ให้เพิ่มโมดูลบล็อกข้อความที่มีเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="39cfb-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="39cfb-160">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="39cfb-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="39cfb-161">หน้าจะแสดงโมดูลหีบที่มีเนื้อหาที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="39cfb-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="39cfb-162">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="39cfb-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39cfb-163">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="39cfb-163">Additional resources</span></span>

[<span data-ttu-id="39cfb-164">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="39cfb-164">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="39cfb-165">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="39cfb-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="39cfb-166">โมดูลแท็บ</span><span class="sxs-lookup"><span data-stu-id="39cfb-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="39cfb-167">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="39cfb-167">Text block module</span></span>](add-content-rich-block.md)
