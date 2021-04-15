---
title: โมดูลวงล้อ
description: หัวข้อนี้ครอบคลุมโมดูลสายพานและอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797898"
---
# <a name="carousel-module"></a><span data-ttu-id="ed161-103">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="ed161-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed161-104">หัวข้อนี้ครอบคลุมโมดูลสายพานและอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ed161-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ed161-105">โมดูลวงล้อจะใช้เพื่อจัดเก็บสินค้าที่มีการส่งเสริมการขายหลายรายการ (รวมถึงรูปภาพ) ในแถบวงล้อที่หมุนได้โดยลูกค้าสามารถเลือกดูได้</span><span class="sxs-lookup"><span data-stu-id="ed161-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="ed161-106">ตัวอย่างเช่น ผู้ค้าปลีกสามารถใช้โมดูลวงล้อบนโฮมเพจเพื่อแสดงผลิตภัณฑ์ใหม่ หรือโปรโมชั่นต่างๆได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="ed161-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="ed161-107">คุณสามารถเพิ่มบล็อกเนื้อหา ภายในโมดูลวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="ed161-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="ed161-108">คุณสมบัติของโมดูลวงล้อ แล้วกำหนดวิธีการแสดงผลโมดูล</span><span class="sxs-lookup"><span data-stu-id="ed161-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="ed161-109">ตัวอย่างของโมดูลคุณวงล้อในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="ed161-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="ed161-110">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="ed161-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="ed161-111">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ed161-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="ed161-112">วงล้อสามารถใช้ได้บนหน้าการตลาดใดๆ เพื่อส่งเสริมการส่งเสริมการขาย หรือผลิตภัณฑ์ หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="ed161-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="ed161-113">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลวงล้อที่ใช้ในโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="ed161-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="ed161-114">โมดูลวงล้อนี้มีรายการบล็อคเนื้อหาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="ed161-114">This carousel module contains multiple content block items.</span></span>

![ตัวอย่างของโมดูลวงล้อ](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="ed161-116">คุณสมบัติโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="ed161-116">Carousel module properties</span></span>

| <span data-ttu-id="ed161-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="ed161-117">Property name</span></span>             | <span data-ttu-id="ed161-118">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="ed161-118">Value</span></span>                 | <span data-ttu-id="ed161-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="ed161-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="ed161-120">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ed161-120">Autoplay</span></span>                  | <span data-ttu-id="ed161-121">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="ed161-121">**True** or **False**</span></span> | <span data-ttu-id="ed161-122">ถ้ามีการตั้งค่าเป็น **จริง** การเปลี่ยนแปลงระหว่างรายการภายในวงล้อจะเกิดขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ed161-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="ed161-123">ถ้าตั้งค่าเป็น **เท็จ** จะไม่มีการเปลี่ยนแปลงใดๆ เกิดขึ้นนอกจากลูกค้าจะใช้แป้นพิมพ์หรือเมาส์ เพื่อย้ายจากสินค้าหนึ่งไปยังรายการถัดไป</span><span class="sxs-lookup"><span data-stu-id="ed161-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="ed161-124">ช่วงเวลาของการเปลี่ยนภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="ed161-124">Slide transition interval</span></span> | <span data-ttu-id="ed161-125">ค่าในวินาที</span><span class="sxs-lookup"><span data-stu-id="ed161-125">A value in seconds</span></span>    | <span data-ttu-id="ed161-126">ช่วงเวลาสำหรับการเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="ed161-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="ed161-127">ชนิดการเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="ed161-127">Transition type</span></span>           | <span data-ttu-id="ed161-128">**สไลด์** หรือ **เฟด**</span><span class="sxs-lookup"><span data-stu-id="ed161-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="ed161-129">เอฟเฟกต์การเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="ed161-129">The transition effect between items.</span></span> |
| <span data-ttu-id="ed161-130">ซ่อนฟลิปเปอร์วงล้อ</span><span class="sxs-lookup"><span data-stu-id="ed161-130">Hide carousel flipper</span></span>     | <span data-ttu-id="ed161-131">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="ed161-131">**True** or **False**</span></span> | <span data-ttu-id="ed161-132">ถ้าตั้งค่าเป็น **จริง** ตัวหมุนวงล้อและตัวบ่งชี้ลำดับจะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="ed161-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="ed161-133">อนุญาตการปิดวงล้อ</span><span class="sxs-lookup"><span data-stu-id="ed161-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="ed161-134">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="ed161-134">**True** or **False**</span></span> | <span data-ttu-id="ed161-135">หากค่าถูกตั้งเป็น **จริง** ผู้ใช้สามารถปิดวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="ed161-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="ed161-136">เพิ่มโมดูลวงล้อไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="ed161-136">Add a carousel module to a page</span></span>

<span data-ttu-id="ed161-137">การเพิ่มโมดูลวงล้อไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ed161-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ed161-138">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="ed161-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="ed161-139">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตวงล้อ** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ed161-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="ed161-140">ในช่อง **Body** ให้เพิ่มโมดูล **หน้าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ed161-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="ed161-141">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="ed161-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="ed161-142">ใช้เท็มเพลตวงล้อที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจวงล้อ**</span><span class="sxs-lookup"><span data-stu-id="ed161-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="ed161-143">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="ed161-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="ed161-144">ในบานหน้าต่างด้านขวา ให้ตั้งค่า **ความกว้าง** เป็น **เต็มหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="ed161-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="ed161-145">ภายใต้ **โครงร่างเพจ** ให้เพิ่มโมดูลวงล้อไปยังโมดูลตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="ed161-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="ed161-146">เพิ่มโมดูลบล็อคเนื้อหาไปยังโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="ed161-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="ed161-147">ตั้งค่าคุณสมบัติของโมดูลบล็อคเนื้อหาโดยการให้ **หัวข้อ** **ลิงก์** **โครงร่าง** และคุณสมบัติอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="ed161-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="ed161-148">เพิ่มและตั้งค่าคอนฟิกโมดูลบล็อคเนื้อหาอื่น</span><span class="sxs-lookup"><span data-stu-id="ed161-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="ed161-149">ตั้งค่าคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้อ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="ed161-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="ed161-150">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="ed161-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="ed161-151">หน้าควรแสดงวงล้อที่มีสองโมดูลที่อยู่ภายใน (โมดูลฮีโร่และโมดูลคุณลักษณะ)</span><span class="sxs-lookup"><span data-stu-id="ed161-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="ed161-152">คุณสามารถเปลี่ยนคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้ ฮีโร่ และคุณลักษณะ เพื่อให้บรรลุผลที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="ed161-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="ed161-153">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="ed161-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed161-154">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ed161-154">Additional resources</span></span>

[<span data-ttu-id="ed161-155">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="ed161-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ed161-156">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="ed161-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="ed161-157">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="ed161-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="ed161-158">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="ed161-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="ed161-159">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="ed161-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]