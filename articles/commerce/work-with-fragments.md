---
title: ใช้งานส่วนย่อย
description: หัวข้อนี้จะอธิบายถึงสาเหตุ เวลา และวิธีใช้ส่วนต่างๆ ใน Microsoft Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914711"
---
# <a name="work-with-fragments"></a><span data-ttu-id="378b0-103">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="378b0-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="378b0-104">หัวข้อนี้จะอธิบายถึงสาเหตุ เวลา และวิธีใช้ส่วนต่างๆ ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="378b0-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="378b0-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="378b0-105">Overview</span></span>

<span data-ttu-id="378b0-106">ส่วนที่อนุญาตให้ใช้สำหรับประสบการณ์การสร้างจากส่วนกลางสำหรับการกำหนดค่าโมดูลที่ต้องมีการนำมาใช้ใหม่ทั่วทั้งไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="378b0-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="378b0-107">ตัวอย่างเช่น ส่วนหัว ส่วนท้าย และแบนเนอร์มักจะมีการกำหนดค่าเป็นส่วนประกอบ เนื่องจากมีการใช้ร่วมกันในหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="378b0-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="378b0-108">คุณสามารถคิดส่วนที่เป็นเว็บเพจที่มีขนาดย่อซึ่งสามารถแทรกลงในหน้าอื่นๆ บนไซต์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="378b0-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="378b0-109">ชิ้นส่วนมีวงจรชีวิตของตนเอง</span><span class="sxs-lookup"><span data-stu-id="378b0-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="378b0-110">กล่าวคือมีการสร้าง อ้างอิง ปรับปรุง และลบออกเป็นเอนทิตี้อิสระในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="378b0-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="378b0-111">หลังจากที่มีการกำหนดค่าส่วนต่างๆ แล้ว ผู้ใช้จะสามารถใช้งานโมดูลใดก็ได้ในโครงสร้างไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="378b0-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="378b0-112">ส่วนต่างๆ สามารถอ้างอิงบนหน้า ในโครงร่าง ในเท็มเพลต และในส่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="378b0-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="378b0-113">ส่วนต่างๆ สามารถซ้อนกันได้สูงสุดเจ็ดระดับภายในชิ้นส่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="378b0-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="378b0-114">ตัวอย่างเช่น ถ้าคุณต้องการเลื่อนระดับเหตุการณ์ตามฤดูกาลข้ามหลายหน้าบนไซต์ของเรา คุณสามารถใช้ส่วนต่างๆได้</span><span class="sxs-lookup"><span data-stu-id="378b0-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="378b0-115">ขั้นตอนแรกในกระบวนการสร้างส่วนใหม่คือเลือกชนิดของโมดูลที่คุณต้องการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="378b0-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="378b0-116">ตัวอย่างเช่น คุณสามารถสร้างส่วนต่างๆ จากโมดูลฮีโร่</span><span class="sxs-lookup"><span data-stu-id="378b0-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="378b0-117">สามารถสร้างส่วนประกอบจากชนิดโมดูลใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="378b0-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="378b0-118">จากนั้นคุณจะสามารถกำหนดค่าส่วนของฮีโร่ที่มีเนื้อหาโปรโมชันเฉพาะของคุณได้</span><span class="sxs-lookup"><span data-stu-id="378b0-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="378b0-119">นอกจากนี้คุณยังสามารถแปลได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="378b0-119">You can also localize it as you require.</span></span> <span data-ttu-id="378b0-120">ส่วนของฮีโร่ที่ทำงานแยกต่างหากแบบใหม่สามารถใช้เป็นโมดูลที่ตั้งค่าคอนฟิกไว้ล่วงหน้าทั่วทั้งไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="378b0-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="378b0-121">คุณสามารถเพิ่มเข้าไปในเท็มเพลต ในหน้าเฉพาะ หรือส่วนอื่นๆ ที่สามารถประกอบด้วยโมดูลฮีโร่ก็ได้</span><span class="sxs-lookup"><span data-stu-id="378b0-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="378b0-122">สถานที่ทั้งหมดที่มีการเพิ่มส่วน เป็นการอ้างอิงไปยังส่วนของฮีโร่ศูนย์กลางที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="378b0-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="378b0-123">ถ้าคุณเผยแพร่การเปลี่ยนแปลงไปยังส่วนต่างๆ การเปลี่ยนแปลงเหล่านั้นจะสะท้อนให้เห็นในสถานที่ทั้งหมดที่มีการอ้างอิงส่วนต่างๆ ทั่วทั้งไซต์โดยทันที</span><span class="sxs-lookup"><span data-stu-id="378b0-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="378b0-124">ดังนั้นส่วนต่างๆ จึงเป็นวิธีการที่มีประสิทธิภาพและมีผลลัพธ์ดีในการนำมาใช้ใหม่และจัดการการตั้งค่าคอนฟิกโมดูลในไซต์โดยตรงจากส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="378b0-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="378b0-125">ด้วยการใช้อย่างมีประสิทธิภาพ คุณสามารถเพิ่มความคล่องตัวได้อย่างมาก และช่วยลดต้นทุนที่เกี่ยวข้องกับการจัดการเนื้อหาของไซต์</span><span class="sxs-lookup"><span data-stu-id="378b0-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="378b0-126">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าส่วนต่างๆ สามารถใช้เป็นศูนย์กลางการสร้างการตั้งค่าคอนฟิกโมดูลที่ใช้ร่วมกันระหว่างไซต์อีคอมเมิร์ซได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="378b0-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![ภาพประกอบต่อไปนี้แสดงให้เห็นว่าส่วนต่างๆ สามารถใช้เป็นศูนย์กลางการสร้างการตั้งค่าคอนฟิกโมดูลที่ใช้ร่วมกันระหว่างไซต์อีคอมเมิร์ซได้อย่างไร](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="378b0-128">การสร้างส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="378b0-128">Create a fragment</span></span>

<span data-ttu-id="378b0-129">คุณสามารถสร้างส่วนใหม่หรือบันทึกการตั้งค่าคอนฟิกโมดูลที่มีอยู่เป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="378b0-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="378b0-130">สร้างส่วนใหม่</span><span class="sxs-lookup"><span data-stu-id="378b0-130">Create a new fragment</span></span>

<span data-ttu-id="378b0-131">เมื่อต้องการสร้างส่วนใหม่ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="378b0-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="378b0-132">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วนต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="378b0-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="378b0-133">เลือก **ส่วนของหน้าใหม่**</span><span class="sxs-lookup"><span data-stu-id="378b0-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="378b0-134">กล่องโต้ตอบจะปรากฏขึ้นเพื่อแสดงชนิดของโมดูลที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="378b0-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="378b0-135">ตามที่กล่าวถึงก่อนหน้านี้ ส่วนต่างๆ อาจสร้างจากชนิดโมดูลใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="378b0-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="378b0-136">เลือกชนิดโมดูลสำหรับส่วนของคุณแล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="378b0-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="378b0-137">ในการเลือกชนิดโมดูลคอนเทนเนอร์ทั่วไป คุณจะได้รับความยืดหยุ่นมากที่สุดเมื่อคุณต้องปรับปรุงและตั้งค่าคอนฟิกส่วนของคุณในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="378b0-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="378b0-138">บันทึกการตั้งค่าคอนฟิกโมดูลที่มีอยู่เป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="378b0-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="378b0-139">เมื่อต้องการแปลงโมดูลที่ตั้งค่าคอนฟิกก่อนหน้านี้เป็นส่วนที่ใช้งานได้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="378b0-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="378b0-140">เปิดหน้าหรือเท็มเพลตที่มีโมดูลที่คุณต้องการแปลงเป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="378b0-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="378b0-141">ในบานหน้าต่างเค้าร่างทางด้านซ้ายให้เลือกปุ่มจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อของโมดูล แล้วเลือก **บันทึกเป็นส่วน**</span><span class="sxs-lookup"><span data-stu-id="378b0-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="378b0-142">กล่องโต้ตอบจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="378b0-142">A dialog box appears.</span></span>
1. <span data-ttu-id="378b0-143">ป้อนชื่อและข้อมูลเมตาสำหรับส่วน</span><span class="sxs-lookup"><span data-stu-id="378b0-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="378b0-144">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าคอนฟิกโมดูลเป็นส่วนที่สามารถเพิ่มเข้าไปในหน้าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="378b0-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="378b0-145">การเพิ่ม ลบ หรือแก้ไขส่วนต่างๆ ที่อยู่บนหน้า</span><span class="sxs-lookup"><span data-stu-id="378b0-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="378b0-146">ขั้นตอนต่อไปนี้จะอธิบายวิธีการเพิ่ม ลบ และแก้ไขส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="378b0-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="378b0-147">เพิ่มส่วน</span><span class="sxs-lookup"><span data-stu-id="378b0-147">Add a fragment</span></span>

<span data-ttu-id="378b0-148">เมื่อต้องการเพิ่มส่วนไปยังหน้า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="378b0-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="378b0-149">ในบานหน้าต่างเค้าร่างด้านซ้าย ให้เลือกตู้คอนเทนเนอร์หรือช่องเสียบที่สามารถเพิ่มโมดูลรองได้</span><span class="sxs-lookup"><span data-stu-id="378b0-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="378b0-150">เลือกปุ่มจุดไข่ปลาที่อยู่ถัดจากชื่อคอนเทนเนอร์หรือช่องเสียบ แล้วเลือก **เพิ่มส่วน**</span><span class="sxs-lookup"><span data-stu-id="378b0-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="378b0-151">กล่องโต้ตอบจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="378b0-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="378b0-152">ถ้าคอนเทนเนอร์หรือช่องเสียบไม่สนับสนุนโมดูลรอง ตัวเลือก **เพิ่มส่วน** จะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="378b0-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="378b0-153">ในกล่องโต้ตอบ ให้ค้นหาและเลือกส่วนที่จะเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="378b0-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="378b0-154">ถ้าไม่มีการระบุส่วนที่มีอยู่ คุณอาจต้องสร้างส่วนใดส่วนหนึ่งจากชนิดโมดูลที่มีการสนับสนุนคอนเทนเนอร์หรือช่องเสียบที่เลือกก่อน</span><span class="sxs-lookup"><span data-stu-id="378b0-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="378b0-155">เลือก **ตกลง** เพื่อเพิ่มส่วนที่เลือกลงในคอนเทนเนอร์ที่เลือกหรือช่องเสียบบนหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="378b0-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="378b0-156">โมดูลที่ได้รับอนุญาตในคอนเทนเนอร์หรือช่องเสียบจะถูกกำหนดโดยเท็มเพลตของหน้าหรือข้อกำหนดของตัวเอง</span><span class="sxs-lookup"><span data-stu-id="378b0-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="378b0-157">ลบส่วน</span><span class="sxs-lookup"><span data-stu-id="378b0-157">Remove a fragment</span></span>

<span data-ttu-id="378b0-158">เมื่อต้องการลบส่วนใดส่วนหนึ่งออกจากช่องเสียบหรือคอนเทนเนอร์บนหน้าให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="378b0-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="378b0-159">ในบานหน้าต่างเค้าร่างทางด้านซ้ายให้เลือกปุ่มจุดไข่ปลา (...) ที่อยู่ถัดจากชื่อส่วนที่ต้องการลบ แล้วเลือกปุ่มถังขยะ</span><span class="sxs-lookup"><span data-stu-id="378b0-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="378b0-160">เมื่อคุณได้รับพร้อมต์ให้ยืนยันว่าคุณต้องการลบส่วนต่างๆ ให้เลอก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="378b0-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="378b0-161">เมื่อคุณลบส่วนใดส่วนหนึ่งออกจากหน้าคุณจะลบส่วนการอ้างอิงนั้นออกจากหน้านั้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="378b0-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="378b0-162">คุณ **ไม่ได้** ลบส่วนออกจากไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="378b0-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="378b0-163">เมื่อต้องการลบส่วนจากไซต์ของคุณ คุณต้องใช้อินเทอร์เฟสผู้ใช้ตรวจสอบส่วน (UI)</span><span class="sxs-lookup"><span data-stu-id="378b0-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="378b0-164">คุณสามารถลบส่วนต่างๆ จากไซต์ได้เฉพาะเมื่อไม่มีการอ้างอิงโดยหน้า เท็มเพลต หรือส่วนอื่นๆ ที่มีการอ้างอิงในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="378b0-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="378b0-165">แก้ไขส่วน</span><span class="sxs-lookup"><span data-stu-id="378b0-165">Edit a fragment</span></span>

<span data-ttu-id="378b0-166">เมื่อต้องการแก้ไขส่วนคุณต้องใช้ UI ของตัวแก้ไขส่วน</span><span class="sxs-lookup"><span data-stu-id="378b0-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="378b0-167">ข้อจำกัดนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="378b0-167">This restriction is by design.</span></span> <span data-ttu-id="378b0-168">ซึ่งจะช่วยรับประกันว่าผู้เขียนไม่สับสนกระบวนการในการแก้ไขโมดูลสำหรับหน้าที่ระบุ ที่มีขั้นตอนในการแก้ไขชิ้นส่วนต่างๆ ที่อาจมีการใช้ร่วมกันในหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="378b0-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="378b0-169">เมื่อต้องการแก้ไขส่วน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="378b0-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="378b0-170">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วนต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="378b0-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="378b0-171">ภายใต้ **ส่วน** ให้เลือกส่วนที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="378b0-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="378b0-172">แก้ไขคุณสมบัติของโมดูลและโครงสร้างของส่วนที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="378b0-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="378b0-173">กระบวนการคล้ายกับกระบวนการของการแก้ไขโมดูลที่ถูกแก้ไขในมุมมองตัวแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="378b0-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="378b0-174">นอกจากนี้คุณยังสามารถแก้ไขส่วนต่างๆ ได้ด้วยการเลือกส่วนบนหน้าในเท็มเพลต หรือในส่วนหลัก แล้วเลือก **แก้ไขส่วนต่างๆ** ในบานหน้าต่างคุณสมบัติทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="378b0-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="378b0-175">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="378b0-175">Additional resources</span></span>

[<span data-ttu-id="378b0-176">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="378b0-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="378b0-177">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="378b0-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="378b0-178">ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="378b0-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="378b0-179">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="378b0-179">Work with publish groups</span></span>](publish-groups.md)
