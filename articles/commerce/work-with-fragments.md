---
title: ใช้งานส่วนย่อย
description: หัวข้อนี้จะอธิบายถึงสาเหตุ เวลา และวิธีใช้ส่วนต่างๆ ใน Microsoft Dynamics 365 Commerce
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793956"
---
# <a name="work-with-fragments"></a><span data-ttu-id="5664a-103">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="5664a-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="5664a-104">หัวข้อนี้จะอธิบายถึงสาเหตุ เวลา และวิธีใช้ส่วนต่างๆ ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5664a-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5664a-105">ส่วนที่อนุญาตให้ใช้สำหรับประสบการณ์การสร้างจากส่วนกลางสำหรับการกำหนดค่าโมดูลที่ต้องมีการนำมาใช้ใหม่ทั่วทั้งไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5664a-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="5664a-106">ตัวอย่างเช่น ส่วนหัว ส่วนท้าย และแบนเนอร์มักจะมีการกำหนดค่าเป็นส่วนประกอบ เนื่องจากมีการใช้ร่วมกันในหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="5664a-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="5664a-107">คุณสามารถคิดส่วนที่เป็นเว็บเพจที่มีขนาดย่อซึ่งสามารถแทรกลงในหน้าอื่นๆ บนไซต์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="5664a-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="5664a-108">ชิ้นส่วนมีวงจรชีวิตของตนเอง</span><span class="sxs-lookup"><span data-stu-id="5664a-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="5664a-109">กล่าวคือมีการสร้าง อ้างอิง ปรับปรุง และลบออกเป็นเอนทิตี้อิสระในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="5664a-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="5664a-110">หลังจากที่มีการกำหนดค่าส่วนต่างๆ แล้ว ผู้ใช้จะสามารถใช้งานโมดูลใดก็ได้ในโครงสร้างไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5664a-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="5664a-111">ส่วนต่างๆ สามารถอ้างอิงบนหน้า ในโครงร่าง ในเท็มเพลต และในส่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5664a-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="5664a-112">ส่วนต่างๆ สามารถซ้อนกันได้สูงสุดเจ็ดระดับภายในชิ้นส่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5664a-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="5664a-113">ตัวอย่างเช่น ถ้าคุณต้องการเลื่อนระดับเหตุการณ์ตามฤดูกาลข้ามหลายหน้าบนไซต์ของเรา คุณสามารถใช้ส่วนต่างๆได้</span><span class="sxs-lookup"><span data-stu-id="5664a-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="5664a-114">ขั้นตอนแรกในกระบวนการสร้างส่วนใหม่คือเลือกชนิดของโมดูลที่คุณต้องการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5664a-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="5664a-115">ตัวอย่างเช่น คุณสามารถสร้างส่วนต่างๆ จากโมดูลฮีโร่</span><span class="sxs-lookup"><span data-stu-id="5664a-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="5664a-116">สามารถสร้างส่วนประกอบจากชนิดโมดูลใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="5664a-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="5664a-117">จากนั้นคุณจะสามารถกำหนดค่าส่วนของฮีโร่ที่มีเนื้อหาโปรโมชันเฉพาะของคุณได้</span><span class="sxs-lookup"><span data-stu-id="5664a-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="5664a-118">นอกจากนี้คุณยังสามารถแปลได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="5664a-118">You can also localize it as you require.</span></span> <span data-ttu-id="5664a-119">ส่วนของฮีโร่ที่ทำงานแยกต่างหากแบบใหม่สามารถใช้เป็นโมดูลที่ตั้งค่าคอนฟิกไว้ล่วงหน้าทั่วทั้งไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5664a-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="5664a-120">คุณสามารถเพิ่มเข้าไปในเท็มเพลต ในหน้าเฉพาะ หรือส่วนอื่นๆ ที่สามารถประกอบด้วยโมดูลฮีโร่ก็ได้</span><span class="sxs-lookup"><span data-stu-id="5664a-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="5664a-121">สถานที่ทั้งหมดที่มีการเพิ่มส่วน เป็นการอ้างอิงไปยังส่วนของฮีโร่ศูนย์กลางที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5664a-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="5664a-122">ถ้าคุณเผยแพร่การเปลี่ยนแปลงไปยังส่วนต่างๆ การเปลี่ยนแปลงเหล่านั้นจะสะท้อนให้เห็นในสถานที่ทั้งหมดที่มีการอ้างอิงส่วนต่างๆ ทั่วทั้งไซต์โดยทันที</span><span class="sxs-lookup"><span data-stu-id="5664a-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="5664a-123">ดังนั้นส่วนต่างๆ จึงเป็นวิธีการที่มีประสิทธิภาพและมีผลลัพธ์ดีในการนำมาใช้ใหม่และจัดการการตั้งค่าคอนฟิกโมดูลในไซต์โดยตรงจากส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="5664a-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="5664a-124">ด้วยการใช้อย่างมีประสิทธิภาพ คุณสามารถเพิ่มความคล่องตัวได้อย่างมาก และช่วยลดต้นทุนที่เกี่ยวข้องกับการจัดการเนื้อหาของไซต์</span><span class="sxs-lookup"><span data-stu-id="5664a-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="5664a-125">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าส่วนต่างๆ สามารถใช้เป็นศูนย์กลางการสร้างการตั้งค่าคอนฟิกโมดูลที่ใช้ร่วมกันระหว่างไซต์อีคอมเมิร์ซได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="5664a-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![ภาพประกอบต่อไปนี้แสดงให้เห็นว่าส่วนต่างๆ สามารถใช้เป็นศูนย์กลางการสร้างการตั้งค่าคอนฟิกโมดูลที่ใช้ร่วมกันระหว่างไซต์อีคอมเมิร์ซได้อย่างไร](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="5664a-127">การสร้างส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5664a-127">Create a fragment</span></span>

<span data-ttu-id="5664a-128">คุณสามารถสร้างส่วนใหม่หรือบันทึกการตั้งค่าคอนฟิกโมดูลที่มีอยู่เป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5664a-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="5664a-129">บันทึกการตั้งค่าคอนฟิกโมดูลที่มีอยู่เป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5664a-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="5664a-130">เมื่อต้องการแปลงโมดูลที่ตั้งค่าคอนฟิกก่อนหน้านี้เป็นส่วนที่ใช้งานซ้ำได้ในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5664a-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5664a-131">เปิดหน้าหรือเท็มเพลตที่มีโมดูลที่คุณต้องการแปลงเป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5664a-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="5664a-132">ในบานหน้าต่างเค้าร่างทางด้านซ้าย หรือโดยตรงในตัวสร้างหน้าการแสดงผลด้วยภาพ ให้เลือกโมดูลที่ตั้งค่าคอนฟิกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="5664a-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="5664a-133">เลือกจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อของโมดูลในบานหน้าต่างเค้าร่าง หรือแถบเครื่องมือของโมดูลที่เลือกในตัวสร้างหน้าการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="5664a-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="5664a-134">เลือก **ใช้ร่วมกันเป็นส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="5664a-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="5664a-135">ในกล่องโต้ตอบ **บันทึกเป็นส่วน** ให้ป้อนชื่อของส่วน</span><span class="sxs-lookup"><span data-stu-id="5664a-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="5664a-136">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าคอนฟิกโมดูลเป็นส่วนที่สามารถเพิ่มเข้าไปในหน้าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5664a-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="5664a-137">สร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="5664a-137">Create a new fragment</span></span>

<span data-ttu-id="5664a-138">เมื่อต้องการสร้างส่วนใหม่ในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5664a-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5664a-139">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วนต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="5664a-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="5664a-140">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="5664a-140">Select **New**.</span></span> <span data-ttu-id="5664a-141">กล่องโต้ตอบ **ส่วนใหม่** จะปรากฏขึ้นเพื่อแสดงชนิดของโมดูลที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5664a-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="5664a-142">ตามที่กล่าวถึงก่อนหน้านี้ ส่วนต่างๆ อาจสร้างจากชนิดโมดูลใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="5664a-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="5664a-143">เลือกชนิดโมดูลสำหรับส่วนย่อยของคุณ</span><span class="sxs-lookup"><span data-stu-id="5664a-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="5664a-144">โดยการเลือกชนิดโมดูลของคอนเทนเนอร์ทั่วไป คุณจะได้รับความยืดหยุ่นมากที่สุดเมื่อคุณต้องปรับปรุงและตั้งค่าคอนฟิกส่วนย่อยของคุณในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="5664a-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="5664a-145">การเพิ่ม ลบ หรือแก้ไขส่วนต่างๆ ที่อยู่บนหน้า</span><span class="sxs-lookup"><span data-stu-id="5664a-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="5664a-146">ขั้นตอนต่อไปนี้จะอธิบายวิธีการเพิ่ม ลบ และแก้ไขส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5664a-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="5664a-147">เพิ่มส่วน</span><span class="sxs-lookup"><span data-stu-id="5664a-147">Add a fragment</span></span>

<span data-ttu-id="5664a-148">เมื่อต้องการเพิ่มส่วนในหน้าในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5664a-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5664a-149">ในบานหน้าต่างเค้าร่างทางด้านซ้าย หรือโดยตรงในตัวสร้างหน้าการแสดงผลด้วยภาพ ให้เลือกคอนเทนเนอร์หรือช่องที่สามารถเพิ่มโมดูลรองได้</span><span class="sxs-lookup"><span data-stu-id="5664a-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="5664a-150">เลือกจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อคอนเทนเนอร์หรือช่อง</span><span class="sxs-lookup"><span data-stu-id="5664a-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="5664a-151">อีกทางหนึ่งคือ ถ้าใช้ตัวสร้างหน้าการแสดงผลด้วยภาพ ให้เลือกสัญลักษณ์บวก (**+**)</span><span class="sxs-lookup"><span data-stu-id="5664a-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="5664a-152">เลือก **เพิ่มส่วน**</span><span class="sxs-lookup"><span data-stu-id="5664a-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="5664a-153">ถ้าคอนเทนเนอร์หรือช่องเสียบไม่สนับสนุนโมดูลรอง ตัวเลือก **เพิ่มส่วน** จะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5664a-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="5664a-154">ในกล่องโต้ตอบ **เลือกส่วน** ให้ค้นหาและเลือกส่วนที่จะเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5664a-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="5664a-155">ถ้าไม่มีการระบุส่วนที่มีอยู่ คุณอาจต้องสร้างส่วนใดส่วนหนึ่งจากชนิดโมดูลที่มีการสนับสนุนคอนเทนเนอร์หรือช่องเสียบที่เลือกก่อน</span><span class="sxs-lookup"><span data-stu-id="5664a-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="5664a-156">เลือกส่วนย่อยที่ต้องการของคุณเพื่อเพิ่มลงในคอนเทนเนอร์หรือช่องบนหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="5664a-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="5664a-157">โมดูลที่ได้รับอนุญาตในคอนเทนเนอร์หรือช่องเสียบจะถูกกำหนดโดยเท็มเพลตของหน้าหรือข้อกำหนดของตัวเอง</span><span class="sxs-lookup"><span data-stu-id="5664a-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="5664a-158">ลบส่วน</span><span class="sxs-lookup"><span data-stu-id="5664a-158">Remove a fragment</span></span>

<span data-ttu-id="5664a-159">เมื่อต้องการลบส่วนใดส่วนหนึ่งออกจากช่องหรือคอนเทนเนอร์บนหน้าในตัวสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5664a-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5664a-160">ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้เลือกปุ่มจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อส่วนที่ต้องการลบ แล้วเลือกสัญลักษณ์ถังขยะ</span><span class="sxs-lookup"><span data-stu-id="5664a-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="5664a-161">อีกทางหนึ่งคือ คุณสามารถเลือกส่วนในตัวสร้างหน้าการแสดงผลด้วยภาพ และเลือกสัญลักษณ์ถังขยะได้ในแถบเครื่องมือของส่วน</span><span class="sxs-lookup"><span data-stu-id="5664a-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="5664a-162">เมื่อคุณได้รับพร้อมต์ให้ยืนยันว่าคุณต้องการลบส่วนต่างๆ ให้เลอก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5664a-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="5664a-163">เมื่อคุณลบส่วนใดส่วนหนึ่งออกจากหน้าคุณจะลบส่วนการอ้างอิงนั้นออกจากหน้านั้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5664a-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="5664a-164">คุณ **ไม่ได้** ลบส่วนออกจากไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5664a-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="5664a-165">เมื่อต้องการลบส่วนจากไซต์ของคุณ คุณต้องใช้อินเทอร์เฟสผู้ใช้ตรวจสอบส่วน (UI)</span><span class="sxs-lookup"><span data-stu-id="5664a-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="5664a-166">คุณสามารถลบส่วนต่างๆ จากไซต์ได้เฉพาะเมื่อไม่มีการอ้างอิงโดยหน้า เท็มเพลต หรือส่วนอื่นๆ ที่มีการอ้างอิงในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="5664a-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="5664a-167">แก้ไขส่วน</span><span class="sxs-lookup"><span data-stu-id="5664a-167">Edit a fragment</span></span>

<span data-ttu-id="5664a-168">เมื่อต้องการแก้ไขส่วนคุณต้องใช้ UI ของตัวแก้ไขส่วน</span><span class="sxs-lookup"><span data-stu-id="5664a-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="5664a-169">ข้อจำกัดนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="5664a-169">This restriction is by design.</span></span> <span data-ttu-id="5664a-170">ซึ่งจะช่วยรับประกันว่าผู้เขียนไม่สับสนกระบวนการในการแก้ไขโมดูลสำหรับหน้าที่ระบุ ที่มีขั้นตอนในการแก้ไขชิ้นส่วนต่างๆ ที่อาจมีการใช้ร่วมกันในหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="5664a-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="5664a-171">เมื่อต้องการแก้ไขส่วนในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5664a-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5664a-172">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วนต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="5664a-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="5664a-173">ภายใต้ **ส่วน** ให้เลือกส่วนที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="5664a-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="5664a-174">แก้ไขคุณสมบัติของโมดูลและโครงสร้างของส่วนที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="5664a-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="5664a-175">กระบวนการคล้ายกับกระบวนการของการแก้ไขโมดูลที่ถูกแก้ไขในมุมมองตัวแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="5664a-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="5664a-176">นอกจากนี้คุณยังสามารถแก้ไขส่วนต่างๆ ได้ด้วยการเลือกส่วนบนหน้าในเท็มเพลต หรือในส่วนหลัก แล้วเลือก **แก้ไขส่วนต่างๆ** ในบานหน้าต่างคุณสมบัติทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="5664a-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5664a-177">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5664a-177">Additional resources</span></span>

[<span data-ttu-id="5664a-178">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="5664a-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="5664a-179">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="5664a-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="5664a-180">ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5664a-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="5664a-181">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5664a-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
