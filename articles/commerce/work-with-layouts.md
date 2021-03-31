---
title: ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า
description: หัวข้อนี้อธิบายวิธีการทำงานกับเค้าโครงที่กำหนดไว้ล่วงหน้าใน Microsoft Dynamics 365 Commerce
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a2539880e76ffb1861e0d18227a935a2ef35c120
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210886"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="9aa60-103">ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9aa60-104">หัวข้อนี้อธิบายวิธีการทำงานกับเค้าโครงที่กำหนดไว้ล่วงหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9aa60-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9aa60-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="9aa60-105">Overview</span></span>

<span data-ttu-id="9aa60-106">ก่อนที่คุณจะดำเนินตามกระบวนงานในหัวข้อนี้จนเสร็จสิ้น ขอให้มั่นใจว่าได้อ่าน [เค้าโครงที่กำหนดไว้ล่วงหน้าและที่กำหนดเอง](templates-layouts-overview.md#preset-and-custom-layouts) แล้ว</span><span class="sxs-lookup"><span data-stu-id="9aa60-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="9aa60-107">สำหรับภาพรวมทั่วไป โปรดดูที่ [ดูภาพรวมของเท็มเพลตและโครงร่าง](templates-layouts-overview.md)</span><span class="sxs-lookup"><span data-stu-id="9aa60-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="9aa60-108">สร้างเค้าโครงที่กำหนดไว้ล่วงหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="9aa60-108">Create a new preset layout</span></span>

<span data-ttu-id="9aa60-109">มีวิธีการสองวิธีในการสร้างเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="9aa60-110">คุณสามารถบันทึกเค้าโครงที่กำหนดเองที่มีอยู่เป็นเค้าโครงที่กำหนดไว้ล่วงหน้าใหม่ได้ หรือคุณจะสร้างเค้าโครงที่กำหนดไว้ล่วงหน้าใหม่ตั้งแต่ต้นก็ได้</span><span class="sxs-lookup"><span data-stu-id="9aa60-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="9aa60-111">สร้างเค้าโครงร่างที่กำหนดไว้ล่วงหน้าจากเค้าโครงที่กำหนดเองที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="9aa60-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="9aa60-112">เมื่อต้องการสร้างเค้าโครงที่กำหนดไว้ล่วงหน้าจากเค้าโครงที่กำหนดเองที่มีอยู่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9aa60-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="9aa60-113">เปิดหน้าที่มีอยู่ ที่ไม่ใช้เค้าโครงที่กำหนดไว้ล่วงหน้าในตอนนี้และมีโครงสร้างโมดูลที่คุณต้องการนำมาใช้ใหม่สำหรับหน้าอื่น ๆ ในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="9aa60-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="9aa60-114">เลือก **แก้ไข** เพื่อตรวจสอบหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="9aa60-115">เลือก **บันทึกเป็นเค้าโครงใหม่**</span><span class="sxs-lookup"><span data-stu-id="9aa60-115">Select **Save as new layout**.</span></span> <span data-ttu-id="9aa60-116">กล่องโต้ตอบ **บันทึกเป็นโครงร่างใหม่** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="9aa60-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="9aa60-117">ป้อนชื่อและคำอธิบายสำหรับเค้าโครงที่กำหนดไว้ล่วงหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="9aa60-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="9aa60-118">ค่าที่คุณป้อนจะแสดงให้ผู้สร้างคนอื่นเห็นเมื่อพวกเขาสร้างหน้าใหม่จากเค้าโครงของคุณหรือเปลี่ยนไปใช้เค้าโครงนั้น</span><span class="sxs-lookup"><span data-stu-id="9aa60-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="9aa60-119">ดังนั้น ป้อนค่าที่จะเป็นประโยชน์ต่อผู้สร้างหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="9aa60-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9aa60-120">Select **OK**.</span></span>

<span data-ttu-id="9aa60-121">ตอนนี้เค้าโครงที่กำหนดไว้ล่วงหน้าจะพร้อมใช้งานเมื่อคุณสร้างหน้าใหม่หรือเลือกเค้าโครงอื่นสำหรับหน้าใดหน้าหนึ่งที่อยู่ในลำดับชั้นเท็มเพลตเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="9aa60-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="9aa60-122">เมื่อต้องการดูอย่างเร็วว่าหน้าใดหน้าหนึ่งโดยเฉพาะถูกผูกไว้กับเค้าโครงที่กำหนดไว้ล่วงหน้าในขณะนี้หรือไม่ ให้เลือกหน้านั้นจากมุมมองรายการหน้า และตรวจสอบข้อมูลเมตาของเค้าโครงในบานหน้าต่างคุณสมบัติทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="9aa60-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="9aa60-123">สร้างเค้าโครงที่กำหนดไว้ล่วงหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="9aa60-123">Create a new preset layout</span></span>

<span data-ttu-id="9aa60-124">เมื่อต้องการสร้างเค้าโครงร่างที่กำหนดไว้ล่วงหน้าใหม่ตั้งแต่ต้น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9aa60-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="9aa60-125">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **เค้าโครง**</span><span class="sxs-lookup"><span data-stu-id="9aa60-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="9aa60-126">เลือก **เค้าโครงใหม่**</span><span class="sxs-lookup"><span data-stu-id="9aa60-126">Select **New Layout**.</span></span> <span data-ttu-id="9aa60-127">กล่องโต้ตอบ **เค้าโครงใหม่** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="9aa60-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="9aa60-128">เลือกเท็มเพลตที่จะใช้สำหรับเค้าโครงที่กำหนดไว้ล่วงหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="9aa60-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="9aa60-129">ป้อนชื่อและคำอธิบายสำหรับเค้าโครงที่กำหนดไว้ล่วงหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="9aa60-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="9aa60-130">ค่าที่คุณป้อนจะแสดงให้ผู้สร้างคนอื่นเห็นเมื่อพวกเขาสร้างหน้าใหม่จากเค้าโครงของคุณหรือเปลี่ยนไปใช้เค้าโครงนั้น</span><span class="sxs-lookup"><span data-stu-id="9aa60-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="9aa60-131">ดังนั้น ป้อนค่าที่จะเป็นประโยชน์ต่อผู้สร้างหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="9aa60-132">เลือก **ตกลง** เพื่อสร้างเค้าโครงที่กำหนดไว้ล่วงหน้าใหม่ และเปิดโปรแกรมแก้ไขเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="9aa60-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="9aa60-133">ในโปรแกรมแก้ไขเค้าโครง เพิ่มและตั้งค่าโมดูลโดยใช้แผนภูมิเค้าร่างทางด้านซ้ายและบานหน้าต่างคุณสมบัติทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="9aa60-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="9aa60-134">(กระบวนการนี้คล้ายกับกระบวนการเพิ่มและตั้งค่าโมดูลสำหรับเท็มเพลตในโปรแกรมแก้ไขเท็มเพลต) การจัดเรียงโมดูลและการตั้งค่าเริ่มต้นที่ล็อคใด ๆ จะกลายเป็นการตั้งค่าโมดูลแบบรวมศูนย์สำหรับหน้าใด ๆ ที่ใช้เค้าโครงที่กำหนดไว้ล่วงหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9aa60-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="9aa60-135">แก้ไขเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-135">Modify a preset layout</span></span>

<span data-ttu-id="9aa60-136">เมื่อต้องการแก้ไขเค้าโครงที่กำหนดไว้ล่วงหน้า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9aa60-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="9aa60-137">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **เค้าโครง**</span><span class="sxs-lookup"><span data-stu-id="9aa60-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="9aa60-138">ในโปรแกรมแก้ไขเค้าโครง ที่แผนภูมิเค้าร่างทางด้านซ้าย ให้เลือกโมดูลที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="9aa60-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="9aa60-139">จากนั้นทำตามขั้นตอนใด ๆ ที่เกี่ยวข้องต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9aa60-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="9aa60-140">เมื่อต้องการย้ายโมดูลขึ้นหรือลงภายในเค้าโครงหลัก ให้เลือกปุ่มจุดไข่ปลา (**...**) ของโมดูลนั้น แล้วเลือก **ย้ายขึ้น** หรือ **ย้ายลง**</span><span class="sxs-lookup"><span data-stu-id="9aa60-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="9aa60-141">เมื่อต้องการเปลี่ยนการตั้งค่าเริ่มต้นของโมดูล ให้ใช้บานหน้าต่างคุณสมบัติเพื่อป้อนค่าเริ่มต้นและอาจเลือกที่จะล็อคค่าสำหรับหน้าระดับล่างลงไปทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9aa60-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="9aa60-142">เมื่อต้องการเพิ่มโมดูลหรือส่วนย่อยใหม่ให้กับโมดูลคอนเทนเนอร์ ให้เลือกปุ่มจุดไข่ปลา แล้วเลือก **เพิ่มโมดูล** หรือ **เพิ่มส่วน**</span><span class="sxs-lookup"><span data-stu-id="9aa60-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="9aa60-143">เมื่อต้องการลบโมดูลออกจากเค้าโครง ให้เลือกปุ่มจุดไข่ปลา แล้วเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="9aa60-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="9aa60-144">เปลี่ยนธีมของโครงร่างที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-144">Change a preset layout theme</span></span>

<span data-ttu-id="9aa60-145">แนวทางปฏิบัติทั่วไป คือ ตั้งค่าธีมเริ่มต้นสำหรับทุกหน้าที่ใช้เค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="9aa60-146">เมื่อต้องการตั้งค่าหรือเปลี่ยนธีมสำหรับหน้ารองทั้งหมดที่ใช้ในเค้าโครงที่กำหนดไว้ล่วงหน้าของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9aa60-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="9aa60-147">ในโปรแกรมแก้ไขเค้าโครง ที่แผนภูมิเค้าร่างทางด้านซ้าย ให้เลือกโมดูลคอนเทนเนอร์ของหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="9aa60-148">(โดยทั่วไปแล้ว โมดูลนี้จะเป็นโหนดที่สอง และใช้ชื่อ **หน้าเริ่มต้น**)</span><span class="sxs-lookup"><span data-stu-id="9aa60-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="9aa60-149">ในบานหน้าต่างคุณสมบัติทางด้านขวา ในฟิลด์ **ธีม** ให้เลือกธีม</span><span class="sxs-lookup"><span data-stu-id="9aa60-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="9aa60-150">บันทึก เช็คอิน แสดงตัวอย่าง และเผยแพร่เค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="9aa60-151">เมื่อต้องการบันทึกและเช็คอินเค้าโครงที่กำหนดไว้ล่วงหน้าของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9aa60-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="9aa60-152">เลือก **บันทึก** ที่ด้านบนของโปรแกรมแก้ไขเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="9aa60-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="9aa60-153">การเปลี่ยนแปลงที่บันทึกจะยังไม่มีผลต่อหน้าระดับล่างลงไปจนกว่าจะมีการเช็คอิน</span><span class="sxs-lookup"><span data-stu-id="9aa60-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="9aa60-154">เลือก **เสร็จสิ้นการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="9aa60-154">Select **Finish editing**.</span></span> <span data-ttu-id="9aa60-155">ขณะนี้ การเปลี่ยนแปลงของคุณสามารถมองเห็นได้ในลำดับงานระดับล่างลงไป</span><span class="sxs-lookup"><span data-stu-id="9aa60-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="9aa60-156">เมื่อต้องการให้แสดงตัวอย่างการเปลี่ยนแปลงของคุณ ให้เปิดหน้าที่มีอยู่ที่ใช้เค้าโครงที่กำหนดไว้ล่วงหน้านั้น หรือสร้างหน้าใหม่จากเค้าโครงนั้น</span><span class="sxs-lookup"><span data-stu-id="9aa60-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="9aa60-157">หลังจากที่คุณดูตัวอย่างการเปลี่ยนแปลงของเค้าโครงที่กำหนดไว้ล่วงหน้าแล้ว ให้ทำตามขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้เพื่อเผยแพร่เค้าโครงไปยังไซต์ที่ใช้งานจริงของคุณ</span><span class="sxs-lookup"><span data-stu-id="9aa60-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="9aa60-158">ไปที่ **เค้าโครง** แล้วเลือกเค้าโครง จากนั้นเลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="9aa60-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="9aa60-159">เลือกชื่อโครงร่างเพื่อเปิดโปรแกรมแก้ไขโครงร่าง และจากนั้น เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="9aa60-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="9aa60-160">เผยแพร่หน้าที่อ้างอิงถึงเค้าโครงที่ยังไม่ได้เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="9aa60-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="9aa60-161">เค้าโครงจะถูกเผยแพร่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9aa60-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="9aa60-162">เค้าโครงที่กำหนดไว้ล่วงหน้าสามารถอ้างอิงไปใช้ได้หลายหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="9aa60-163">เมื่อคุณเผยแพร่เค้าโครงที่กำหนดไว้ล่วงหน้าแล้ว ควรตระหนักว่าคุณอาจสร้างผลกระทบต่อเค้าโครงของหน้าหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="9aa60-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9aa60-164">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9aa60-164">Additional resources</span></span>

[<span data-ttu-id="9aa60-165">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="9aa60-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9aa60-166">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="9aa60-166">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]