---
title: โมดูลวงล้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลวงล้อ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: f09f3f98d174f965a75e27ee6a5c2ed8599042fc
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816997"
---
# <a name="carousel-module"></a><span data-ttu-id="f1e54-103">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="f1e54-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1e54-104">หัวข้อนี้ครอบคลุมถึงโมดูลวงล้อ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f1e54-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f1e54-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="f1e54-105">Overview</span></span>

<span data-ttu-id="f1e54-106">โมดูลวงล้อจะใช้เพื่อจัดเก็บสินค้าที่มีการส่งเสริมการขายหลายรายการ (รวมถึงรูปภาพ) ในแถบวงล้อที่หมุนได้โดยลูกค้าสามารถเลือกดูได้</span><span class="sxs-lookup"><span data-stu-id="f1e54-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="f1e54-107">ตัวอย่างเช่น ผู้ค้าปลีกสามารถใช้โมดูลวงล้อบนโฮมเพจเพื่อแสดงผลิตภัณฑ์ใหม่ หรือโปรโมชั่นต่างๆได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f1e54-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="f1e54-108">คุณสามารถเพิ่มบล็อกเนื้อหา ภายในโมดูลวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="f1e54-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="f1e54-109">คุณสมบัติของโมดูลวงล้อ แล้วกำหนดวิธีการแสดงผลโมดูล</span><span class="sxs-lookup"><span data-stu-id="f1e54-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="f1e54-110">ตัวอย่างของโมดูลคุณวงล้อในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f1e54-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="f1e54-111">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="f1e54-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="f1e54-112">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f1e54-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="f1e54-113">วงล้อสามารถใช้ได้บนหน้าการตลาดใดๆ เพื่อส่งเสริมการส่งเสริมการขาย หรือผลิตภัณฑ์ หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f1e54-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="f1e54-114">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลวงล้อที่ใช้ในโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="f1e54-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="f1e54-115">โมดูลวงล้อนี้มีรายการบล็อคเนื้อหาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f1e54-115">This carousel module contains multiple content block items.</span></span>

![ตัวอย่างของโมดูลวงล้อ](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="f1e54-117">คุณสมบัติโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="f1e54-117">Carousel module properties</span></span>

| <span data-ttu-id="f1e54-118">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="f1e54-118">Property name</span></span>             | <span data-ttu-id="f1e54-119">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="f1e54-119">Value</span></span>                 | <span data-ttu-id="f1e54-120">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f1e54-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f1e54-121">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f1e54-121">Autoplay</span></span>                  | <span data-ttu-id="f1e54-122">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f1e54-122">**True** or **False**</span></span> | <span data-ttu-id="f1e54-123">ถ้ามีการตั้งค่าเป็น **จริง** การเปลี่ยนแปลงระหว่างรายการภายในวงล้อจะเกิดขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f1e54-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="f1e54-124">ถ้าตั้งค่าเป็น **เท็จ** จะไม่มีการเปลี่ยนแปลงใดๆ เกิดขึ้นนอกจากลูกค้าจะใช้แป้นพิมพ์หรือเมาส์ เพื่อย้ายจากสินค้าหนึ่งไปยังรายการถัดไป</span><span class="sxs-lookup"><span data-stu-id="f1e54-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="f1e54-125">ช่วงเวลาของการเปลี่ยนภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="f1e54-125">Slide transition interval</span></span> | <span data-ttu-id="f1e54-126">ค่าในวินาที</span><span class="sxs-lookup"><span data-stu-id="f1e54-126">A value in seconds</span></span>    | <span data-ttu-id="f1e54-127">ช่วงเวลาสำหรับการเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="f1e54-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="f1e54-128">ชนิดการเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="f1e54-128">Transition type</span></span>           | <span data-ttu-id="f1e54-129">**สไลด์** หรือ **เฟด**</span><span class="sxs-lookup"><span data-stu-id="f1e54-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="f1e54-130">เอฟเฟกต์การเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="f1e54-130">The transition effect between items.</span></span> |
| <span data-ttu-id="f1e54-131">ซ่อนฟลิปเปอร์วงล้อ</span><span class="sxs-lookup"><span data-stu-id="f1e54-131">Hide carousel flipper</span></span>     | <span data-ttu-id="f1e54-132">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f1e54-132">**True** or **False**</span></span> | <span data-ttu-id="f1e54-133">ถ้าตั้งค่าเป็น **จริง** ตัวหมุนวงล้อและตัวบ่งชี้ลำดับจะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="f1e54-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="f1e54-134">อนุญาตการปิดวงล้อ</span><span class="sxs-lookup"><span data-stu-id="f1e54-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="f1e54-135">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f1e54-135">**True** or **False**</span></span> | <span data-ttu-id="f1e54-136">หากค่าถูกตั้งเป็น **จริง** ผู้ใช้สามารถปิดวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="f1e54-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="f1e54-137">เพิ่มโมดูลวงล้อไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="f1e54-137">Add a carousel module to a page</span></span>

<span data-ttu-id="f1e54-138">การเพิ่มโมดูลวงล้อไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f1e54-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f1e54-139">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="f1e54-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f1e54-140">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตวงล้อ** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f1e54-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f1e54-141">ในช่อง **Body** ให้เพิ่มโมดูล **หน้าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f1e54-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="f1e54-142">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f1e54-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="f1e54-143">ใช้เท็มเพลตวงล้อที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจวงล้อ**</span><span class="sxs-lookup"><span data-stu-id="f1e54-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="f1e54-144">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="f1e54-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="f1e54-145">ในบานหน้าต่างด้านขวา ให้ตั้งค่า **ความกว้าง** เป็น **เต็มหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="f1e54-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="f1e54-146">ภายใต้ **โครงร่างเพจ** ให้เพิ่มโมดูลวงล้อไปยังโมดูลตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="f1e54-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="f1e54-147">เพิ่มโมดูลบล็อคเนื้อหาไปยังโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="f1e54-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="f1e54-148">ตั้งค่าคุณสมบัติของโมดูลบล็อคเนื้อหาโดยการให้ **หัวข้อ** **ลิงก์** **โครงร่าง** และคุณสมบัติอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f1e54-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="f1e54-149">เพิ่มและตั้งค่าคอนฟิกโมดูลบล็อคเนื้อหาอื่น</span><span class="sxs-lookup"><span data-stu-id="f1e54-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="f1e54-150">ตั้งค่าคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้อ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f1e54-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="f1e54-151">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="f1e54-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f1e54-152">หน้าควรแสดงวงล้อที่มีสองโมดูลที่อยู่ภายใน (โมดูลฮีโร่และโมดูลคุณลักษณะ)</span><span class="sxs-lookup"><span data-stu-id="f1e54-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="f1e54-153">คุณสามารถเปลี่ยนคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้ ฮีโร่ และคุณลักษณะ เพื่อให้บรรลุผลที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="f1e54-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="f1e54-154">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f1e54-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1e54-155">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f1e54-155">Additional resources</span></span>

[<span data-ttu-id="f1e54-156">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="f1e54-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f1e54-157">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="f1e54-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f1e54-158">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="f1e54-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f1e54-159">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f1e54-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f1e54-160">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="f1e54-160">Video player module</span></span>](add-video-player.md)
