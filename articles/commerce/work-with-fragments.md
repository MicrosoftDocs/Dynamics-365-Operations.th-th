---
title: ใช้งานส่วนย่อย
description: หัวข้อนี้จะอธิบายถึงสาเหตุ เวลา และวิธีใช้ส่วนต่างๆ ใน Microsoft Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: f29046ded47ed9c49a2cc841aa7c1f6492b49aec
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026051"
---
# <a name="work-with-fragments"></a><span data-ttu-id="dbf21-103">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="dbf21-103">Work with fragments</span></span> 


[!include [banner](includes/banner.md)]

<span data-ttu-id="dbf21-104">หัวข้อนี้จะอธิบายถึงสาเหตุ เวลา และวิธีใช้ส่วนต่างๆ ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dbf21-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dbf21-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="dbf21-105">Overview</span></span>

<span data-ttu-id="dbf21-106">ส่วนที่อนุญาตให้ใช้สำหรับประสบการณ์การสร้างจากส่วนกลางสำหรับการกำหนดค่าโมดูลที่ต้องมีการนำมาใช้ใหม่ทั่วทั้งไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="dbf21-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="dbf21-107">ตัวอย่างเช่น ส่วนหัว ส่วนท้าย และแบนเนอร์มักจะมีการกำหนดค่าเป็นส่วนประกอบ เนื่องจากมีการใช้ร่วมกันในหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="dbf21-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="dbf21-108">คุณสามารถคิดส่วนที่เป็นเว็บเพจที่มีขนาดย่อซึ่งสามารถแทรกลงในหน้าอื่นๆ บนไซต์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="dbf21-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="dbf21-109">ชิ้นส่วนมีวงจรชีวิตของตนเอง</span><span class="sxs-lookup"><span data-stu-id="dbf21-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="dbf21-110">กล่าวคือมีการสร้าง อ้างอิง ปรับปรุง และลบออกเป็นเอนทิตี้อิสระในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="dbf21-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="dbf21-111">หลังจากที่มีการกำหนดค่าส่วนต่างๆ แล้ว ผู้ใช้จะสามารถใช้งานโมดูลใดก็ได้ในโครงสร้างไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="dbf21-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="dbf21-112">ส่วนต่างๆ สามารถอ้างอิงบนหน้า ในโครงร่าง ในเท็มเพลต และในส่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="dbf21-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="dbf21-113">ส่วนต่างๆ สามารถซ้อนกันได้สูงสุดเจ็ดระดับภายในชิ้นส่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="dbf21-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="dbf21-114">ตัวอย่างเช่น ถ้าคุณต้องการเลื่อนระดับเหตุการณ์ตามฤดูกาลข้ามหลายหน้าบนไซต์ของเรา คุณสามารถใช้ส่วนต่างๆได้</span><span class="sxs-lookup"><span data-stu-id="dbf21-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="dbf21-115">ขั้นตอนแรกในกระบวนการสร้างส่วนใหม่คือเลือกชนิดของโมดูลที่คุณต้องการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dbf21-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="dbf21-116">ตัวอย่างเช่น คุณสามารถสร้างส่วนต่างๆ จากโมดูลฮีโร่</span><span class="sxs-lookup"><span data-stu-id="dbf21-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="dbf21-117">สามารถสร้างส่วนประกอบจากชนิดโมดูลใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="dbf21-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="dbf21-118">จากนั้นคุณจะสามารถกำหนดค่าส่วนของฮีโร่ที่มีเนื้อหาโปรโมชันเฉพาะของคุณได้</span><span class="sxs-lookup"><span data-stu-id="dbf21-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="dbf21-119">นอกจากนี้คุณยังสามารถแปลได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="dbf21-119">You can also localize it as you require.</span></span> <span data-ttu-id="dbf21-120">ส่วนของฮีโร่ที่ทำงานแยกต่างหากแบบใหม่สามารถใช้เป็นโมดูลที่ตั้งค่าคอนฟิกไว้ล่วงหน้าทั่วทั้งไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="dbf21-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="dbf21-121">คุณสามารถเพิ่มเข้าไปในเท็มเพลต ในหน้าเฉพาะ หรือส่วนอื่นๆ ที่สามารถประกอบด้วยโมดูลฮีโร่ก็ได้</span><span class="sxs-lookup"><span data-stu-id="dbf21-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="dbf21-122">สถานที่ทั้งหมดที่มีการเพิ่มส่วน เป็นการอ้างอิงไปยังส่วนของฮีโร่ศูนย์กลางที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="dbf21-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="dbf21-123">ถ้าคุณเผยแพร่การเปลี่ยนแปลงไปยังส่วนต่างๆ การเปลี่ยนแปลงเหล่านั้นจะสะท้อนให้เห็นในสถานที่ทั้งหมดที่มีการอ้างอิงส่วนต่างๆ ทั่วทั้งไซต์โดยทันที</span><span class="sxs-lookup"><span data-stu-id="dbf21-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="dbf21-124">ดังนั้นส่วนต่างๆ จึงเป็นวิธีการที่มีประสิทธิภาพและมีผลลัพธ์ดีในการนำมาใช้ใหม่และจัดการการตั้งค่าคอนฟิกโมดูลในไซต์โดยตรงจากส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="dbf21-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="dbf21-125">ด้วยการใช้อย่างมีประสิทธิภาพ คุณสามารถเพิ่มความคล่องตัวได้อย่างมาก และช่วยลดต้นทุนที่เกี่ยวข้องกับการจัดการเนื้อหาของไซต์</span><span class="sxs-lookup"><span data-stu-id="dbf21-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="dbf21-126">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าส่วนต่างๆ สามารถใช้เป็นศูนย์กลางการสร้างการตั้งค่าคอนฟิกโมดูลที่ใช้ร่วมกันระหว่างไซต์อีคอมเมิร์ซได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="dbf21-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![ภาพประกอบต่อไปนี้แสดงให้เห็นว่าส่วนต่างๆ สามารถใช้เป็นศูนย์กลางการสร้างการตั้งค่าคอนฟิกโมดูลที่ใช้ร่วมกันระหว่างไซต์อีคอมเมิร์ซได้อย่างไร](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="dbf21-128">การสร้างส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="dbf21-128">Create a fragment</span></span>

<span data-ttu-id="dbf21-129">คุณสามารถสร้างส่วนใหม่หรือบันทึกการตั้งค่าคอนฟิกโมดูลที่มีอยู่เป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dbf21-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="dbf21-130">บันทึกการตั้งค่าคอนฟิกโมดูลที่มีอยู่เป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dbf21-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="dbf21-131">เมื่อต้องการแปลงโมดูลที่ตั้งค่าคอนฟิกก่อนหน้านี้เป็นส่วนที่ใช้งานได้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dbf21-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="dbf21-132">เปิดหน้าหรือเท็มเพลตที่มีโมดูลที่คุณต้องการแปลงเป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dbf21-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="dbf21-133">ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้เลือกปุ่มจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อของโมดูล</span><span class="sxs-lookup"><span data-stu-id="dbf21-133">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module.</span></span> 
1. <span data-ttu-id="dbf21-134">เลือก **ใช้ร่วมกันเป็นส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="dbf21-134">Select **Share as Fragment**.</span></span> 
1. <span data-ttu-id="dbf21-135">กล่องโต้ตอบจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="dbf21-135">A dialog box appears.</span></span> <span data-ttu-id="dbf21-136">ป้อนชื่อและข้อมูลเมตาสำหรับส่วน</span><span class="sxs-lookup"><span data-stu-id="dbf21-136">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="dbf21-137">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าคอนฟิกโมดูลเป็นส่วนที่สามารถเพิ่มเข้าไปในหน้าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="dbf21-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="dbf21-138">รูปภาพต่อไปนี้แสดงวิธีการบันทึกการตั้งค่าคอนฟิกโมดูลเป็นส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="dbf21-138">The following image shows how to save a module configuration as a fragment.</span></span>

![การจับภาพหน้าจอของวิธีการตั้งค่าคอนฟิกโมดูลเป็นส่วนย่อย](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="dbf21-140">สร้างส่วนใหม่</span><span class="sxs-lookup"><span data-stu-id="dbf21-140">Create a new fragment</span></span>

<span data-ttu-id="dbf21-141">เมื่อต้องการสร้างส่วนใหม่ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dbf21-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="dbf21-142">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วนต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="dbf21-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="dbf21-143">เลือก **ส่วนของหน้าใหม่**</span><span class="sxs-lookup"><span data-stu-id="dbf21-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="dbf21-144">กล่องโต้ตอบจะปรากฏขึ้นเพื่อแสดงชนิดของโมดูลที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="dbf21-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="dbf21-145">ตามที่กล่าวถึงก่อนหน้านี้ ส่วนต่างๆ อาจสร้างจากชนิดโมดูลใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="dbf21-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="dbf21-146">เลือกชนิดโมดูลสำหรับส่วนย่อยของคุณ</span><span class="sxs-lookup"><span data-stu-id="dbf21-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="dbf21-147">รูปภาพต่อไปนี้แสดงตำแหน่งที่จะสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="dbf21-147">The following image shows where to create a new fragment.</span></span>

![การจับภาพหน้าจอของสถานที่ที่จะสร้างส่วนย่อยใหม่](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="dbf21-149">โดยการเลือกชนิดโมดูลของคอนเทนเนอร์ทั่วไป คุณจะได้รับความยืดหยุ่นมากที่สุดเมื่อคุณต้องปรับปรุงและตั้งค่าคอนฟิกส่วนย่อยของคุณในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="dbf21-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="dbf21-150">การเพิ่ม ลบ หรือแก้ไขส่วนต่างๆ ที่อยู่บนหน้า</span><span class="sxs-lookup"><span data-stu-id="dbf21-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="dbf21-151">ขั้นตอนต่อไปนี้จะอธิบายวิธีการเพิ่ม ลบ และแก้ไขส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="dbf21-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="dbf21-152">เพิ่มส่วน</span><span class="sxs-lookup"><span data-stu-id="dbf21-152">Add a fragment</span></span>

<span data-ttu-id="dbf21-153">เมื่อต้องการเพิ่มส่วนไปยังหน้า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dbf21-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="dbf21-154">ในบานหน้าต่างเค้าร่างด้านซ้าย ให้เลือกตู้คอนเทนเนอร์หรือช่องเสียบที่สามารถเพิ่มโมดูลรองได้</span><span class="sxs-lookup"><span data-stu-id="dbf21-154">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="dbf21-155">เลือกปุ่มจุดไข่ปลาที่อยู่ถัดจากชื่อคอนเทนเนอร์หรือช่องเสียบ แล้วเลือก **เพิ่มส่วน**</span><span class="sxs-lookup"><span data-stu-id="dbf21-155">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="dbf21-156">กล่องโต้ตอบจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="dbf21-156">A dialog box appears.</span></span>

    ![การจับภาพหน้าจอของวิธีการเพิ่มส่วนย่อยที่มีอยู่ลงในช่องหรือคอนเทนเนอร์](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="dbf21-158">ถ้าคอนเทนเนอร์หรือช่องเสียบไม่สนับสนุนโมดูลรอง ตัวเลือก **เพิ่มส่วน** จะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="dbf21-158">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="dbf21-159">ในกล่องโต้ตอบ ให้ค้นหาและเลือกส่วนที่จะเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dbf21-159">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="dbf21-160">ถ้าไม่มีการระบุส่วนที่มีอยู่ คุณอาจต้องสร้างส่วนใดส่วนหนึ่งจากชนิดโมดูลที่มีการสนับสนุนคอนเทนเนอร์หรือช่องเสียบที่เลือกก่อน</span><span class="sxs-lookup"><span data-stu-id="dbf21-160">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="dbf21-161">เลือกส่วนย่อยที่ต้องการของคุณเพื่อเพิ่มลงในคอนเทนเนอร์หรือช่องบนหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="dbf21-161">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![การจับภาพหน้าจอของหน้าต่างโมดอลของตัวเลือกส่วนย่อย](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="dbf21-163">โมดูลที่ได้รับอนุญาตในคอนเทนเนอร์หรือช่องเสียบจะถูกกำหนดโดยเท็มเพลตของหน้าหรือข้อกำหนดของตัวเอง</span><span class="sxs-lookup"><span data-stu-id="dbf21-163">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="dbf21-164">ลบส่วน</span><span class="sxs-lookup"><span data-stu-id="dbf21-164">Remove a fragment</span></span>

<span data-ttu-id="dbf21-165">เมื่อต้องการลบส่วนใดส่วนหนึ่งออกจากช่องเสียบหรือคอนเทนเนอร์บนหน้าให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dbf21-165">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="dbf21-166">ในบานหน้าต่างเค้าร่างทางด้านซ้ายให้เลือกปุ่มจุดไข่ปลา (...) ที่อยู่ถัดจากชื่อส่วนที่ต้องการลบ แล้วเลือกปุ่มถังขยะ</span><span class="sxs-lookup"><span data-stu-id="dbf21-166">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="dbf21-167">เมื่อคุณได้รับพร้อมต์ให้ยืนยันว่าคุณต้องการลบส่วนต่างๆ ให้เลอก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="dbf21-167">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="dbf21-168">เมื่อคุณลบส่วนใดส่วนหนึ่งออกจากหน้าคุณจะลบส่วนการอ้างอิงนั้นออกจากหน้านั้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="dbf21-168">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="dbf21-169">คุณ **ไม่ได้** ลบส่วนออกจากไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="dbf21-169">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="dbf21-170">เมื่อต้องการลบส่วนจากไซต์ของคุณ คุณต้องใช้อินเทอร์เฟสผู้ใช้ตรวจสอบส่วน (UI)</span><span class="sxs-lookup"><span data-stu-id="dbf21-170">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="dbf21-171">คุณสามารถลบส่วนต่างๆ จากไซต์ได้เฉพาะเมื่อไม่มีการอ้างอิงโดยหน้า เท็มเพลต หรือส่วนอื่นๆ ที่มีการอ้างอิงในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="dbf21-171">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="dbf21-172">แก้ไขส่วน</span><span class="sxs-lookup"><span data-stu-id="dbf21-172">Edit a fragment</span></span>

<span data-ttu-id="dbf21-173">เมื่อต้องการแก้ไขส่วนคุณต้องใช้ UI ของตัวแก้ไขส่วน</span><span class="sxs-lookup"><span data-stu-id="dbf21-173">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="dbf21-174">ข้อจำกัดนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="dbf21-174">This restriction is by design.</span></span> <span data-ttu-id="dbf21-175">ซึ่งจะช่วยรับประกันว่าผู้เขียนไม่สับสนกระบวนการในการแก้ไขโมดูลสำหรับหน้าที่ระบุ ที่มีขั้นตอนในการแก้ไขชิ้นส่วนต่างๆ ที่อาจมีการใช้ร่วมกันในหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="dbf21-175">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="dbf21-176">เมื่อต้องการแก้ไขส่วน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dbf21-176">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="dbf21-177">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วนต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="dbf21-177">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="dbf21-178">ภายใต้ **ส่วน** ให้เลือกส่วนที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="dbf21-178">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="dbf21-179">แก้ไขคุณสมบัติของโมดูลและโครงสร้างของส่วนที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="dbf21-179">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="dbf21-180">กระบวนการคล้ายกับกระบวนการของการแก้ไขโมดูลที่ถูกแก้ไขในมุมมองตัวแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="dbf21-180">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="dbf21-181">นอกจากนี้คุณยังสามารถแก้ไขส่วนต่างๆ ได้ด้วยการเลือกส่วนบนหน้าในเท็มเพลต หรือในส่วนหลัก แล้วเลือก **แก้ไขส่วนต่างๆ** ในบานหน้าต่างคุณสมบัติทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="dbf21-181">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbf21-182">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dbf21-182">Additional resources</span></span>

[<span data-ttu-id="dbf21-183">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="dbf21-183">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="dbf21-184">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="dbf21-184">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="dbf21-185">ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="dbf21-185">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="dbf21-186">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="dbf21-186">Work with publish groups</span></span>](publish-groups.md)
