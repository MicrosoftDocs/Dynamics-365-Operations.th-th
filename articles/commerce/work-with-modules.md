---
title: ใช้งานโมดูล
description: หัวข้อนี้จะอธิบายว่าจะใช้โมดูลเมื่อไรและอย่างไรใน Microsoft Dynamics 365 Commerce
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 301eb6206fb9e02c3aa7d3c07cf368ba800a1ab9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416146"
---
# <a name="work-with-modules"></a><span data-ttu-id="30537-103">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="30537-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="30537-104">หัวข้อนี้จะอธิบายว่าจะใช้โมดูลเมื่อไรและอย่างไรใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="30537-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30537-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="30537-105">Overview</span></span>

<span data-ttu-id="30537-106">โมดูลเป็นบล็อกส่วนประกอบเชิงตรรกะที่ประกอบขึ้นเป็นโครงสร้างหน้าของคุณ และมีวัตถุประสงค์และขอบเขตที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="30537-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="30537-107">โมดูลบางโมดูลเป็นคอนเทนเนอร์ระดับสูง และวัตถุประสงค์ของโมดูลคือรองรับและจัดระเบียบโมดูลอื่น ๆ (โมดูลรอง) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="30537-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="30537-108">โมดูลอื่น ๆ เช่น โมดูลการจัดวางภาพอย่างง่าย มีวัตถุประสงค์ที่เฉพาะเจาะจงมาก</span><span class="sxs-lookup"><span data-stu-id="30537-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="30537-109">โมดูลอื่น ๆ เช่น โมดูลแบบวงล้อ จะอยู่ระหว่างโมดูลสองประเภทนั้น</span><span class="sxs-lookup"><span data-stu-id="30537-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="30537-110">โดยค่าเริ่มต้น ไซต์ Dynamics 365 Commerce ของคุณจะมีไลบรารีโมดูลที่ช่วยให้คุณสามารถบรรลุในสถานการณ์อีคอมเมิร์ซขั้นพื้นฐานส่วนใหญ่ได้</span><span class="sxs-lookup"><span data-stu-id="30537-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="30537-111">คุณควรจะสามารถสร้างไซต์อีคอมเมิร์ซแบบครอบคลุมตั้งแต่ต้นจนจบได้โดยใช้เพียงโมดูลเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="30537-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="30537-112">อย่างไรก็ตาม คุณอาจต้องการเลือกกำหนดโมดูลเหล่านี้หรือสร้างโมดูลที่กำหนดเองใหม่สำหรับความต้องการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="30537-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="30537-113">ถ้าคุณต้องการสร้างโมดูลที่กำหนดเอง ชุดพัฒนาซอฟต์แวร์ (SDK) การออกแบบโมดูลมีพร้อมให้คุณใช้งานเพื่อช่วยคุณสร้างไลบรารีโมดูลที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="30537-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="30537-114">โมดูลคอนเทนเนอร์และช่อง</span><span class="sxs-lookup"><span data-stu-id="30537-114">Container modules and slots</span></span>

<span data-ttu-id="30537-115">ดังที่ได้กล่าวถึงก่อนหน้านี้ บางโมดูลถูกออกแบบมาเพื่อรองรับโมดูลรองไว้</span><span class="sxs-lookup"><span data-stu-id="30537-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="30537-116">โมดูลเหล่านี้เรียกว่า *คอนเทนเนอร์* ซึ่งอนุญาตให้มีลำดับชั้นของโมดูลที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="30537-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="30537-117">โมดูลคอนเทนเนอร์จะมี *ช่อง*</span><span class="sxs-lookup"><span data-stu-id="30537-117">Container modules include *slots*.</span></span> <span data-ttu-id="30537-118">ช่องจะใช้ในการจัดการเค้าโครงและวัตถุประสงค์ของโมดูลรองในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="30537-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="30537-119">ตัวอย่างต่อไปนี้คือโมดูลคอนเทนเนอร์ของหน้าพื้นฐาน (โมดูลระดับบนสุดสำหรับหน้าใด ๆ) ที่กำหนดช่องสำคัญหลายช่อง:</span><span class="sxs-lookup"><span data-stu-id="30537-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="30537-120">ช่องส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="30537-120">A header slot</span></span>
- <span data-ttu-id="30537-121">ช่องส่วนหัวย่อย</span><span class="sxs-lookup"><span data-stu-id="30537-121">A sub-header slot</span></span>
- <span data-ttu-id="30537-122">ช่องหลัก</span><span class="sxs-lookup"><span data-stu-id="30537-122">A main slot</span></span>
- <span data-ttu-id="30537-123">ช่องส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="30537-123">A footer slot</span></span>
- <span data-ttu-id="30537-124">ช่องส่วนท้ายย่อย</span><span class="sxs-lookup"><span data-stu-id="30537-124">A sub-footer slot</span></span>

<span data-ttu-id="30537-125">นักพัฒนาโมดูลจะกำหนดช่องเหล่านี้ และกำหนดว่ามีโมดูลรองใดบ้างและมีโมดูลรองกี่โมดูลที่จะสามารถอยู่ในโมดูลนี้ได้</span><span class="sxs-lookup"><span data-stu-id="30537-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="30537-126">ตัวอย่างเช่น ช่องส่วนหัวอาจสนับสนุนโมดูลเดียวเท่านั้นในประเภท **โมดูลส่วนหัว** ในขณะที่ช่องเนื้อหาอาจสนับสนุนโมดูลได้ไม่จำกัดจำนวนในประเภทใดก็ได้ (ยกเว้นโมดูลคอนเทนเนอร์ของหน้าอื่น)</span><span class="sxs-lookup"><span data-stu-id="30537-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="30537-127">ในเครื่องมือการสร้าง ผู้สร้างหน้าไม่จำเป็นต้องทราบมาก่อนล่วงหน้าว่าโมดูลใดสามารถและไม่สามารถใส่ในช่องแต่ละช่องได้</span><span class="sxs-lookup"><span data-stu-id="30537-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="30537-128">เมื่อผู้สร้างหน้าเลือกช่องแล้วลองเลือกโมดูลที่จะเพิ่มเข้าไป พวกเขาจะเห็นมุมมองที่มีการกรองชนิดของโมดูลที่ได้รับการสนับสนุนในช่องนั้น</span><span class="sxs-lookup"><span data-stu-id="30537-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="30537-129">โมดูลเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="30537-129">Content modules</span></span>

<span data-ttu-id="30537-130">โมดูลเนื้อหามีองค์ประกอบที่เป็นเนื้อหาและสื่อ เช่น ข้อความ (ตัวอย่างเช่น พาดหัว ย่อหน้า และลิงก์) หรือข้อมูลอ้างอิงของสินทรัพย์ (ตัวอย่างเช่น รูปภาพ วิดีโอ และ PDF)</span><span class="sxs-lookup"><span data-stu-id="30537-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="30537-131">ชนิดโมดูเนื้อหาโดยทั่วไปรวมถึงบล็อกเนื้อหา บล็อกข้อความ และโมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="30537-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="30537-132">โมดูลของสามชนิดนี้อาจประกอบด้วยข้อความหรือสื่อ และไม่ได้ต้องการโมดูลรองใด ๆ เพื่อให้บางสิ่งแสดงขึ้นบนหน้า</span><span class="sxs-lookup"><span data-stu-id="30537-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="30537-133">ส่วนมาก กิจกรรมการสร้างหน้าและเนื้อหาวันต่อวันโดยทั่วไปจะเกี่ยวข้องกับโมดูลเนื้อหา โดยส่วนใหญ่แล้วเนื่องจากโมดูลเหล่านี้จะกำหนดเนื้อหาจริงที่จะแสดงขึ้นในโมดูลคอนเทนเนอร์หลัก</span><span class="sxs-lookup"><span data-stu-id="30537-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="30537-134">มีโมดูลเนื้อหาจำนวนมากที่พร้อมใช้งาน และโดยทั่วไปแล้ว โมดูลเหล่านี้จะเป็นส่วนสุดท้ายที่คุณจะเพิ่มลงในลำดับชั้นของหน้าของโมดูลที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="30537-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="30537-135">แผนภาพต่อไปนี้แสดงว่าโมดูลซ้อนกันอยู่อย่างไรในช่องโมดูลคอนเทนเนอร์หลัก</span><span class="sxs-lookup"><span data-stu-id="30537-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![โมดูลที่ซ้อนกัน](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="30537-137">เพิ่มหรือลบโมดูล</span><span class="sxs-lookup"><span data-stu-id="30537-137">Add or remove modules</span></span>

<span data-ttu-id="30537-138">กระบวนงานต่อไปนี้จะอธิบายวิธีการเพิ่มและลบโมดูล</span><span class="sxs-lookup"><span data-stu-id="30537-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="30537-139">เพิ่มโมดูล</span><span class="sxs-lookup"><span data-stu-id="30537-139">Add a module</span></span>

<span data-ttu-id="30537-140">เมื่อต้องการเพิ่มโมดูลไปที่ช่องหรือคอนเทนเนอร์ในหน้าหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="30537-141">ในบานหน้าต่างเค้าร่างทางด้านซ้ายหรือโดยตรงในพื้นที่ทำงานหลัก ให้เลือกคอนเทนเนอร์หรือช่องที่สามารถเพิ่มโมดูลรองได้</span><span class="sxs-lookup"><span data-stu-id="30537-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="30537-142">ผู้ออกแบบโมดูลจะกำหนดรายการของชนิดโมดูลที่สามารถเพิ่มเข้าไปในช่องโมดูลเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="30537-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="30537-143">ผู้สร้างแม่แบบจะสามารถจำกัดตัวเลือกโมดูลที่อนุญาตเพื่อช่วยรับประกันประสิทธิภาพโปรแกรมค้นหา (SEO) และประสิทธิภาพของการสร้างให้สอดคล้องกันระหว่างหน้าทั้งหมดที่สร้างขึ้นจากแม่แบบแต่ละแม่แบบโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="30537-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="30537-144">เมื่อเพิ่มโมดูลที่ไปช่อง กล่องโต้ตอบ **เพิ่มโมดูล** นี้จะถูกกรองโดยอัตโนมัติ เพื่อให้แสดงเฉพาะโมดูลที่สนับสนุนในคอนเทนเนอร์หรือช่องที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="30537-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="30537-145">รายการของโมดูลที่อนุญาตนี้จะถูกกำหนดโดยแม่แบบของหน้าหรือข้อกำหนดของโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="30537-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="30537-146">ถ้าใช้บานหน้าต่างเค้าร่าง ให้เลือกจุดไข่ปลา (**...**) ถัดจากชื่อโมดูล แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="30537-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="30537-147">ถ้าใช้ตัวควบคุมโดยตรงภายในพื้นที่ทำงาน ให้เลือกสัญลักษณ์เครื่องหมายบวก (**+**) ในช่องว่างเปล่าหรือที่อยู่ติดกับโมดูลที่เลือกในปัจจุบัน แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="30537-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="30537-148">ถ้าคอนเทนเนอร์หรือช่องไม่สนับสนุนโมดูลรองใหม่ ตัวเลือก **เพิ่มโมดูล** จะใช้งานไม่ได้</span><span class="sxs-lookup"><span data-stu-id="30537-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="30537-149">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้ค้นหาและเลือกโมดูลที่จะเพิ่มในหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="30537-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="30537-150">**บล็อกเนื้อหา** เป็นชนิดโมดูลที่ดีสำหรับผู้เริ่มต้นที่จะทำงาน</span><span class="sxs-lookup"><span data-stu-id="30537-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="30537-151">เลือก **ตกลง** เพื่อเพิ่มโมดูลที่เลือกลงในคอนเทนเนอร์หรือช่องที่เลือกไว้บนหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="30537-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="30537-152">ลบโมดูล</span><span class="sxs-lookup"><span data-stu-id="30537-152">Remove a module</span></span>

<span data-ttu-id="30537-153">เมื่อต้องการลบโมดูลใดโมดูลหนึ่งออกจากช่องหรือคอนเทนเนอร์บนหน้า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="30537-154">ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้เลือกปุ่มจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อโมดูลที่ต้องการลบ แล้วเลือกสัญลักษณ์ถังขยะ</span><span class="sxs-lookup"><span data-stu-id="30537-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="30537-155">อีกทางหนึ่งคือ ในพื้นที่ทำงานหลัก คุณสามารถเลือกสัญลักษณ์ถังขยะบนแถบเครื่องมือของโมดูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="30537-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="30537-156">เมื่อพร้อมต์ให้ยืนยันว่าคุณต้องการลบโมดูลหรือไม่ ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="30537-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="30537-157">ย้ายโมดูลไปตำแหน่งใหม่</span><span class="sxs-lookup"><span data-stu-id="30537-157">Move a module to a new position</span></span>

<span data-ttu-id="30537-158">เมื่อต้องการย้ายโมดูลไปตำแหน่งใหม่ภายในหน้าของคุณ ให้ใช้วิธีการใดวิธีการหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="30537-159">ย้ายโมดูลโดยใช้บานหน้าต่างเค้าร่าง</span><span class="sxs-lookup"><span data-stu-id="30537-159">Move a module using the outline pane</span></span>

<span data-ttu-id="30537-160">เมื่อต้องการย้ายโมดูลโดยใช้บานหน้าต่างเค้าร่าง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="30537-161">เลือกและกดโมดูลที่คุณต้องการย้ายในบานหน้าต่างเค้าร่างค้างไว้ แล้วลากโมดูลไปยังตำแหน่งใหม่ในเค้าร่าง</span><span class="sxs-lookup"><span data-stu-id="30537-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="30537-162">เส้นสีน้ำเงินในเค้าร่างและบนพื้นที่ทำงานจะบ่งชี้ว่าสามารถวางโมดูลได้ที่ใด</span><span class="sxs-lookup"><span data-stu-id="30537-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="30537-163">ปล่อยโมดูลลงในตำแหน่งใหม่</span><span class="sxs-lookup"><span data-stu-id="30537-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="30537-164">ย้ายโมดูลในภายในพื้นที่ทำงานโดยตรง</span><span class="sxs-lookup"><span data-stu-id="30537-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="30537-165">เมื่อต้องการย้ายโมดูลโดยตรงภายในพื้นที่ทำงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="30537-166">เลือกโมดูลที่คุณต้องการย้ายในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="30537-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="30537-167">เลือกสัญลักษณ์ลูกศรชี้ขึ้นหรือลงในแถบเครื่องมือของโมดูล แล้วลากลูกศรไปยังตำแหน่งใหม่บนหน้า</span><span class="sxs-lookup"><span data-stu-id="30537-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="30537-168">เส้นสีน้ำเงินในพื้นที่ทำงานและเค้าร่างจะบ่งชี้ว่าสามารถวางโมดูลได้ที่ใด</span><span class="sxs-lookup"><span data-stu-id="30537-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="30537-169">ถ้าโมดูลไม่สามารถย้ายขึ้นหรือลงได้ สัญลักษณ์ลูกศรจะเป็นสีเทา</span><span class="sxs-lookup"><span data-stu-id="30537-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="30537-170">ปล่อยโมดูลลงในตำแหน่งใหม่</span><span class="sxs-lookup"><span data-stu-id="30537-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="30537-171">ย้ายโมดูลโดยใช้เมนูจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="30537-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="30537-172">เมื่อต้องการย้ายโมดูลโดยใช้เมนูจุดไข่ปลา ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="30537-173">เลือกโมดูลในเค้าร่างหรือพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="30537-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="30537-174">เลือกจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อของโมดูลในบานหน้าต่างเค้าร่าง หรือแถบเครื่องมือของโมดูลในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="30537-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="30537-175">ถ้าโมดูลสามารถเคลื่อนย้ายขึ้นหรือลงภายในคอนเทนเนอร์หรือช่อง คุณจะเห็นตัวเลือกสำหรับ **เลื่อนขึ้น** หรือ **เลื่อนลง**</span><span class="sxs-lookup"><span data-stu-id="30537-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="30537-176">เลือกตัวเลือกการย้ายที่ต้องการ เพื่อย้ายโมดูลขึ้นหรือลงที่สัมพันธ์กับระดับเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="30537-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="30537-177">ตั้งค่าโมดูล</span><span class="sxs-lookup"><span data-stu-id="30537-177">Configure modules</span></span>

<span data-ttu-id="30537-178">กระบวนงานต่อไปนี้จะอธิบายวิธีการตั้งค่าโมดูลเนื้อหาและโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="30537-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="30537-179">ตั้งค่าโมดูลเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="30537-179">Configure a content module</span></span>

<span data-ttu-id="30537-180">เมื่อต้องการตั้งค่าโมดูลเนื้อหาบนหน้าใดหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="30537-181">ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้ขยายแผนภูมิและเลือกโมดูลเนื้อหาใดๆ (ตัวอย่างเช่น **บล็อกเนื้อหา**)</span><span class="sxs-lookup"><span data-stu-id="30537-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="30537-182">อีกทางหนึ่งคือ คุณสามารถเลือกโมดูลในพื้นที่ทำงานหลักได้</span><span class="sxs-lookup"><span data-stu-id="30537-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="30537-183">ในบานหน้าต่างคุณสมบัติโมดูลที่ด้านขวา ให้ป้อนคุณสมบัติสำหรับตัวควบคุมโมดูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="30537-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="30537-184">บนแถบคำสั่ง ให้เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="30537-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="30537-185">การทำเช่นนี้จะเป็นการรีเฟรชพื้นที่ทำงานของการแสดงตัวอย่างด้วย</span><span class="sxs-lookup"><span data-stu-id="30537-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="30537-186">แก้ไขคุณสมบัติข้อความของโมดูล</span><span class="sxs-lookup"><span data-stu-id="30537-186">Edit module text properties</span></span>

<span data-ttu-id="30537-187">คุณสมบัติข้อความของโมดูลที่ไม่ใช่แบบอ่านอย่างเดียวสามารถแก้ไขได้โดยตรงในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="30537-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="30537-188">เมื่อต้องการแก้ไขคุณสมบัติข้อความของโมดูล ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="30537-189">เลือกตัวควบคุมข้อความในพื้นที่ทำงาน แล้ววางเคอร์เซอร์ไว้ตรงจุดที่คุณต้องการแก้ไขข้อความ</span><span class="sxs-lookup"><span data-stu-id="30537-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="30537-190">ป้อนเนื้อหาข้อความของคุณ</span><span class="sxs-lookup"><span data-stu-id="30537-190">Enter your text content.</span></span>
1. <span data-ttu-id="30537-191">เลือกที่ใดก็ได้ภายนอกเนื้อหาของข้อความ เพื่อแก้ไขเนื้อหาอื่นๆ ต่อไป</span><span class="sxs-lookup"><span data-stu-id="30537-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="30537-192">การเลือกรูปแบบอินไลน์</span><span class="sxs-lookup"><span data-stu-id="30537-192">Inline image selection</span></span>

<span data-ttu-id="30537-193">รูปภาพของโมดูลที่ไม่ใช่แบบอ่านอย่างเดียวสามารถเปลี่ยนได้โดยตรงจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="30537-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="30537-194">เมื่อต้องการเลือกรูปภาพใหม่สำหรับโมดูลเนื้อหา ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="30537-195">ในพื้นที่ทำงาน ให้คลิกรูปภาพสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="30537-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="30537-196">การทำเช่นนี้จะเรีบกหน้าต่างตัวเลือกสื่อ</span><span class="sxs-lookup"><span data-stu-id="30537-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="30537-197">ค้นหาและเลือกรูปภาพใหม่ที่คุณต้องการใช้ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="30537-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="30537-198">ขณะนี้มีการแสดงรูปภาพใหม่ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="30537-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="30537-199">การตั้งค่าโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="30537-199">Configure a container module</span></span>

<span data-ttu-id="30537-200">เมื่อต้องการตั้งค่าคอนเทนเนอร์บนหน้าใดหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30537-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="30537-201">เลือกโมดูลคอนเทนเนอร์โมดูลหนึ่งบนหน้าของคุณ (ตัวอย่างเช่น โมดูลคอนเทนเนอร์แบบวงล้อหรือแบบลื่นไหล)</span><span class="sxs-lookup"><span data-stu-id="30537-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="30537-202">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ขยายตัวควบคุมที่ซ้อนกันอยู่ โดยเลือกหัวข้อและตั้งค่าการควบคุมใด ๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="30537-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="30537-203">ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้เลือกปุ่มจุดไข่ปลาที่อยู่ถัดจากชื่อคอนเทนเนอร์หรือชื่อของช่องใด ๆ ในคอนเทนเนอร์ แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="30537-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="30537-204">จากนั้น เพิ่มโมดูลรองให้กับคอนเทนเนอร์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="30537-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="30537-205">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ส่วน [ทำงานกับโมดูล](#add-a-module) ที่กล่าวถึงก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="30537-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="30537-206">ถ้ามีโมดูลรองหลายโมดูลอยู่ระดับเดียวกันในคอนเทนเนอร์หลัก คุณสามารถเปลี่ยนลำดับการแสดงผลในคอนเทนเนอร์หลักได้</span><span class="sxs-lookup"><span data-stu-id="30537-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="30537-207">เลือกปุ่มจุดไข่ปลาสำหรับโมดูล แล้วใช้ปุ่มลูกศรขึ้นและปุ่มลูกศรลง</span><span class="sxs-lookup"><span data-stu-id="30537-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30537-208">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="30537-208">Additional resources</span></span>

[<span data-ttu-id="30537-209">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="30537-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="30537-210">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="30537-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="30537-211">ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="30537-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="30537-212">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="30537-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="30537-213">เพิ่มโมดูลคอนเทนเนอร์ไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="30537-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="30537-214">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="30537-214">Work with publish groups</span></span>](publish-groups.md)

