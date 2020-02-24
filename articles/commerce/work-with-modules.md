---
title: ใช้งานโมดูล
description: หัวข้อนี้จะอธิบายว่าจะใช้โมดูลเมื่อไรและอย่างไรใน Microsoft Dynamics 365 Commerce
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
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025890"
---
# <a name="work-with-modules"></a><span data-ttu-id="4ab5b-103">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="4ab5b-103">Work with modules</span></span>

<span data-ttu-id="4ab5b-104">หัวข้อนี้จะอธิบายว่าจะใช้โมดูลเมื่อไรและอย่างไรใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4ab5b-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>


[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="4ab5b-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="4ab5b-105">Overview</span></span>

<span data-ttu-id="4ab5b-106">โมดูลเป็นบล็อกส่วนประกอบเชิงตรรกะที่ประกอบขึ้นเป็นโครงสร้างหน้าของคุณ และมีวัตถุประสงค์และขอบเขตที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="4ab5b-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="4ab5b-107">โมดูลบางโมดูลเป็นคอนเทนเนอร์ระดับสูง และวัตถุประสงค์ของโมดูลคือรองรับและจัดระเบียบโมดูลอื่น ๆ (โมดูลรอง) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4ab5b-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="4ab5b-108">โมดูลอื่น ๆ เช่น โมดูลการจัดวางภาพอย่างง่าย มีวัตถุประสงค์ที่เฉพาะเจาะจงมาก</span><span class="sxs-lookup"><span data-stu-id="4ab5b-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="4ab5b-109">โมดูลอื่น ๆ เช่น โมดูลแบบวงล้อ จะอยู่ระหว่างโมดูลสองประเภทนั้น</span><span class="sxs-lookup"><span data-stu-id="4ab5b-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="4ab5b-110">โดยค่าเริ่มต้น ไซต์ Dynamics 365 Commerce ของคุณจะมีไลบรารีโมดูลชุดเริ่มต้นที่ช่วยให้คุณสามารถบรรลุในสถานการณ์อีคอมเมิร์ซขั้นพื้นฐานส่วนใหญ่ได้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="4ab5b-111">คุณควรจะสามารถสร้างไซต์อีคอมเมิร์ซแบบครอบคลุมตั้งแต่ต้นจนจบได้โดยใช้เพียงโมดูลเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="4ab5b-112">อย่างไรก็ตาม คุณอาจต้องการเลือกกำหนดโมดูลเหล่านี้หรือสร้างโมดูลที่กำหนดเองใหม่สำหรับความต้องการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="4ab5b-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="4ab5b-113">ถ้าคุณต้องการสร้างโมดูลที่กำหนดเอง ชุดพัฒนาซอฟต์แวร์ (SDK) การออกแบบโมดูลมีพร้อมให้คุณใช้งานเพื่อช่วยคุณสร้างไลบรารีโมดูลที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4ab5b-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="4ab5b-114">โมดูลคอนเทนเนอร์และช่อง</span><span class="sxs-lookup"><span data-stu-id="4ab5b-114">Container modules and slots</span></span>

<span data-ttu-id="4ab5b-115">ดังที่ได้กล่าวถึงก่อนหน้านี้ บางโมดูลถูกออกแบบมาเพื่อรองรับโมดูลรองไว้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="4ab5b-116">โมดูลเหล่านี้เรียกว่า *คอนเทนเนอร์* ซึ่งอนุญาตให้มีลำดับชั้นของโมดูลที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="4ab5b-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="4ab5b-117">โมดูลคอนเทนเนอร์จะมี *ช่อง*</span><span class="sxs-lookup"><span data-stu-id="4ab5b-117">Container modules include *slots*.</span></span> <span data-ttu-id="4ab5b-118">ช่องจะใช้ในการจัดการเค้าโครงและวัตถุประสงค์ของโมดูลรองในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="4ab5b-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="4ab5b-119">ตัวอย่างต่อไปนี้คือโมดูลคอนเทนเนอร์ของหน้าพื้นฐาน (โมดูลระดับบนสุดสำหรับหน้าใด ๆ) ที่กำหนดช่องสำคัญหลายช่อง:</span><span class="sxs-lookup"><span data-stu-id="4ab5b-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="4ab5b-120">ช่องส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="4ab5b-120">A header slot</span></span>
- <span data-ttu-id="4ab5b-121">ช่องเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="4ab5b-121">A body slot</span></span>
- <span data-ttu-id="4ab5b-122">ช่องส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="4ab5b-122">A footer slot</span></span>

<span data-ttu-id="4ab5b-123">นักพัฒนาโมดูลจะกำหนดช่องเหล่านี้ และกำหนดว่ามีโมดูลรองใดบ้างและมีโมดูลรองกี่โมดูลที่จะสามารถอยู่ในโมดูลนี้ได้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="4ab5b-124">ตัวอย่างเช่น ช่องส่วนหัวอาจสนับสนุนโมดูลเดียวเท่านั้นในประเภท **โมดูลส่วนหัว** ในขณะที่ช่องเนื้อหาอาจสนับสนุนโมดูลได้ไม่จำกัดจำนวนในประเภทใดก็ได้ (ยกเว้นโมดูลคอนเทนเนอร์ของหน้าอื่น)</span><span class="sxs-lookup"><span data-stu-id="4ab5b-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="4ab5b-125">ในเครื่องมือการสร้าง ผู้สร้างหน้าไม่จำเป็นต้องทราบมาก่อนล่วงหน้าว่าโมดูลใดสามารถและไม่สามารถใส่ในช่องแต่ละช่องได้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="4ab5b-126">เมื่อผู้สร้างหน้าเลือกช่องแล้วลองเลือกโมดูลที่จะเพิ่มเข้าไป พวกเขาจะเห็นมุมมองที่มีการกรองชนิดของโมดูลที่ได้รับการสนับสนุนในช่องนั้น</span><span class="sxs-lookup"><span data-stu-id="4ab5b-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="4ab5b-127">โมดูลเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="4ab5b-127">Content modules</span></span>

<span data-ttu-id="4ab5b-128">โมดูลเนื้อหามีองค์ประกอบที่เป็นเนื้อหาและสื่อ เช่น ข้อความ (ตัวอย่างเช่น พาดหัว ย่อหน้า และลิงก์) หรือข้อมูลอ้างอิงของสินทรัพย์ (ตัวอย่างเช่น รูปภาพ วิดีโอ และ PDF)</span><span class="sxs-lookup"><span data-stu-id="4ab5b-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="4ab5b-129">ตัวอย่างของชนิดโมดูลเนื้อหาโดยทั่วไป ได้แก่ **ฮีโร่** **คุณลักษณะ** และ **แบนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="4ab5b-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="4ab5b-130">โมดูลของสามชนิดนี้อาจประกอบด้วยข้อความหรือสื่อ และไม่ได้ต้องการโมดูลรองใด ๆ เพื่อให้บางสิ่งแสดงขึ้นบนหน้า</span><span class="sxs-lookup"><span data-stu-id="4ab5b-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="4ab5b-131">ส่วนมาก กิจกรรมการสร้างหน้าและเนื้อหาวันต่อวันโดยทั่วไปจะเกี่ยวข้องกับโมดูลเนื้อหา โดยส่วนใหญ่แล้วเนื่องจากโมดูลเหล่านี้จะกำหนดเนื้อหาจริงที่จะแสดงขึ้นในโมดูลคอนเทนเนอร์หลัก</span><span class="sxs-lookup"><span data-stu-id="4ab5b-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="4ab5b-132">มีโมดูลเนื้อหาจำนวนมากที่พร้อมใช้งาน และโดยทั่วไปแล้ว โมดูลเหล่านี้จะเป็นส่วนสุดท้ายที่คุณจะเพิ่มลงในลำดับชั้นของหน้าของโมดูลที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="4ab5b-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="4ab5b-133">แผนภาพต่อไปนี้แสดงว่าโมดูลซ้อนกันอยู่อย่างไรในช่องโมดูลคอนเทนเนอร์หลัก</span><span class="sxs-lookup"><span data-stu-id="4ab5b-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![โมดูลที่ซ้อนกัน](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="4ab5b-135">เพิ่มหรือลบโมดูล</span><span class="sxs-lookup"><span data-stu-id="4ab5b-135">Add or remove modules</span></span>

<span data-ttu-id="4ab5b-136">กระบวนงานต่อไปนี้จะอธิบายวิธีการเพิ่มและลบโมดูล</span><span class="sxs-lookup"><span data-stu-id="4ab5b-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="4ab5b-137">เพิ่มโมดูล</span><span class="sxs-lookup"><span data-stu-id="4ab5b-137">Add a module</span></span>

<span data-ttu-id="4ab5b-138">เมื่อต้องการเพิ่มโมดูลไปที่ช่องหรือคอนเทนเนอร์ในหน้าหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="4ab5b-139">ในบานหน้าต่างเค้าร่างด้านซ้าย ให้เลือกคอนเทนเนอร์หรือช่องที่สามารถเพิ่มโมดูลรองได้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4ab5b-140">ผู้ออกแบบโมดูลจะกำหนดรายการของชนิดโมดูลที่สามารถเพิ่มเข้าไปในช่องโมดูลเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="4ab5b-141">ผู้สร้างเท็มเพลตจะสามารถจำกัดตัวเลือกโมดูลที่อนุญาตเพื่อช่วยรับประกันประสิทธิภาพโปรแกรมค้นหา (SEO) และประสิทธิภาพของการสร้างให้สอดคล้องกันระหว่างหน้าทั้งหมดที่สร้างขึ้นจากเท็มเพลตแต่ละเท็มเพลตโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="4ab5b-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="4ab5b-142">เลือกปุ่มจุดไข่ปลา (**...**) สำหรับโมดูล แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4ab5b-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="4ab5b-143">กล่องโต้ตอบ **เพิ่มโมดูล** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="4ab5b-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="4ab5b-144">กล่องโต้ตอบนี้จะถูกกรองโดยอัตโนมัติเพื่อให้แสดงเฉพาะโมดูลที่สนับสนุนในคอนเทนเนอร์หรือช่องที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4ab5b-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="4ab5b-145">รายการของโมดูลจะถูกกำหนดโดยเท็มเพลตของหน้าหรือข้อกำหนดของโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="4ab5b-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4ab5b-146">ถ้าคอนเทนเนอร์หรือช่องไม่สนับสนุนโมดูลรองใหม่ ตัวเลือก **เพิ่มโมดูล** จะใช้งานไม่ได้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="4ab5b-147">ในกล่องโต้ตอบ ให้ค้นหาและเลือกโมดูลที่จะเพิ่มในหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="4ab5b-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="4ab5b-148">**คุณลักษณะ** และ **ฮีโร่** เป็นชนิดโมดูลที่ดีสำหรับผู้เริ่มต้นในการทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="4ab5b-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="4ab5b-149">เลือก **ตกลง** เพื่อเพิ่มโมดูลที่เลือกลงในคอนเทนเนอร์หรือช่องที่เลือกไว้บนหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="4ab5b-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="4ab5b-150">ลบโมดูล</span><span class="sxs-lookup"><span data-stu-id="4ab5b-150">Remove a module</span></span>

<span data-ttu-id="4ab5b-151">เมื่อต้องการลบโมดูลใดโมดูลหนึ่งออกจากช่องหรือคอนเทนเนอร์บนหน้า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="4ab5b-152">ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้เลือกปุ่มจุดไข่ปลาที่อยู่ถัดจากชื่อโมดูลที่ต้องการลบ แล้วเลือกปุ่มถังขยะ</span><span class="sxs-lookup"><span data-stu-id="4ab5b-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="4ab5b-153">เมื่อคุณต้องยืนยันว่าคุณต้องการลบโมดูลหรือไม่ ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4ab5b-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="4ab5b-154">ตั้งค่าโมดูล</span><span class="sxs-lookup"><span data-stu-id="4ab5b-154">Configure modules</span></span>

<span data-ttu-id="4ab5b-155">กระบวนงานต่อไปนี้จะอธิบายวิธีการตั้งค่าโมดูลเนื้อหาและโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="4ab5b-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="4ab5b-156">ตั้งค่าโมดูลเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="4ab5b-156">Configure a content module</span></span>

<span data-ttu-id="4ab5b-157">เมื่อต้องการตั้งค่าโมดูลเนื้อหาบนหน้าใดหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="4ab5b-158">ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้ขยายแผนภูมิและเลือกโมดูลเนื้อหาใดๆ (ตัวอย่างเช่น **คุณลักษณะ** **ฮีโร่** หรือ **แบนเนอร์**)</span><span class="sxs-lookup"><span data-stu-id="4ab5b-158">In the outline pane on the left, expand the tree and select any content module (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="4ab5b-159">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ค้นหาเนื้อหาของโมดูลและตัวควบคุมการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="4ab5b-159">In the properties pane on the right, find the module's content and settings controls.</span></span>
1. <span data-ttu-id="4ab5b-160">ป้อนคุณสมบัติสำหรับการควบคุมโมดูลที่ต้องการใดๆ</span><span class="sxs-lookup"><span data-stu-id="4ab5b-160">Enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="4ab5b-161">ให้เลือก **บันทึก** ในแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="4ab5b-161">Select **Save** in the command bar.</span></span> <span data-ttu-id="4ab5b-162">การทำเช่นนี้จะเป็นการรีเฟรชพื้นที่ทำงานของการแสดงตัวอย่างด้วย</span><span class="sxs-lookup"><span data-stu-id="4ab5b-162">This will also refresh the preview canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="4ab5b-163">การตั้งค่าโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="4ab5b-163">Configure a container module</span></span>

<span data-ttu-id="4ab5b-164">เมื่อต้องการตั้งค่าคอนเทนเนอร์บนหน้าใดหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-164">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="4ab5b-165">เลือกโมดูลคอนเทนเนอร์โมดูลหนึ่งบนหน้าของคุณ (ตัวอย่างเช่น โมดูลคอนเทนเนอร์แบบวงล้อหรือแบบลื่นไหล)</span><span class="sxs-lookup"><span data-stu-id="4ab5b-165">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="4ab5b-166">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ขยายตัวควบคุมที่ซ้อนกันอยู่ โดยเลือกหัวข้อและตั้งค่าการควบคุมใด ๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="4ab5b-166">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="4ab5b-167">ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้เลือกปุ่มจุดไข่ปลาที่อยู่ถัดจากชื่อคอนเทนเนอร์หรือชื่อของช่องใด ๆ ในคอนเทนเนอร์ แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4ab5b-167">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="4ab5b-168">จากนั้น เพิ่มโมดูลรองให้กับคอนเทนเนอร์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4ab5b-168">Then, add child modules to the selected container.</span></span> <span data-ttu-id="4ab5b-169">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ส่วน [ทำงานกับโมดูล](#add-a-module) ที่กล่าวถึงก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-169">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="4ab5b-170">ถ้ามีโมดูลรองหลายโมดูลอยู่ระดับเดียวกันในคอนเทนเนอร์หลัก คุณสามารถเปลี่ยนลำดับการแสดงผลในคอนเทนเนอร์หลักได้</span><span class="sxs-lookup"><span data-stu-id="4ab5b-170">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="4ab5b-171">เลือกปุ่มจุดไข่ปลาสำหรับโมดูล แล้วใช้ปุ่มลูกศรขึ้นและปุ่มลูกศรลง</span><span class="sxs-lookup"><span data-stu-id="4ab5b-171">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ab5b-172">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4ab5b-172">Additional resources</span></span>

[<span data-ttu-id="4ab5b-173">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="4ab5b-173">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="4ab5b-174">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="4ab5b-174">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="4ab5b-175">ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="4ab5b-175">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="4ab5b-176">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="4ab5b-176">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="4ab5b-177">เพิ่มโมดูลคอนเทนเนอร์ไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="4ab5b-177">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="4ab5b-178">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="4ab5b-178">Work with publish groups</span></span>](publish-groups.md)

