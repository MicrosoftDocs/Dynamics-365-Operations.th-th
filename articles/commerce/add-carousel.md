---
title: โมดูลวงล้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลวงล้อ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269739"
---
# <a name="carousel-module"></a><span data-ttu-id="f8459-103">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="f8459-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f8459-104">หัวข้อนี้ครอบคลุมถึงโมดูลวงล้อ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8459-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8459-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="f8459-105">Overview</span></span>

<span data-ttu-id="f8459-106">โมดูลวงล้อจะใช้เพื่อจัดเก็บสินค้าที่มีการส่งเสริมการขายหลายรายการ (รวมถึงรูปภาพ) ในแถบวงล้อที่หมุนได้โดยลูกค้าสามารถเลือกดูได้</span><span class="sxs-lookup"><span data-stu-id="f8459-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="f8459-107">ตัวอย่างเช่น ผู้ค้าปลีกสามารถใช้โมดูลวงล้อบนโฮมเพจเพื่อแสดงผลิตภัณฑ์ใหม่ หรือโปรโมชั่นต่างๆได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f8459-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="f8459-108">คุณสามารถเพิ่มบล็อกเนื้อหา ภายในโมดูลวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="f8459-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="f8459-109">คุณสมบัติของโมดูลวงล้อ แล้วกำหนดวิธีการแสดงผลโมดูล</span><span class="sxs-lookup"><span data-stu-id="f8459-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="f8459-110">ตัวอย่างของโมดูลคุณวงล้อในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f8459-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="f8459-111">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="f8459-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="f8459-112">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f8459-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="f8459-113">วงล้อสามารถใช้ได้บนหน้าการตลาดใดๆ เพื่อส่งเสริมการส่งเสริมการขาย หรือผลิตภัณฑ์ หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f8459-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="f8459-114">คุณสมบัติโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="f8459-114">Carousel module properties</span></span>

| <span data-ttu-id="f8459-115">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="f8459-115">Property name</span></span>             | <span data-ttu-id="f8459-116">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="f8459-116">Value</span></span>                 | <span data-ttu-id="f8459-117">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f8459-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f8459-118">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f8459-118">Autoplay</span></span>                  | <span data-ttu-id="f8459-119">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f8459-119">**True** or **False**</span></span> | <span data-ttu-id="f8459-120">ถ้ามีการตั้งค่าเป็น **จริง** การเปลี่ยนแปลงระหว่างรายการภายในวงล้อจะเกิดขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f8459-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="f8459-121">ถ้าตั้งค่าเป็น **เท็จ** จะไม่มีการเปลี่ยนแปลงใดๆ เกิดขึ้นนอกจากลูกค้าจะใช้แป้นพิมพ์หรือเมาส์ เพื่อย้ายจากสินค้าหนึ่งไปยังรายการถัดไป</span><span class="sxs-lookup"><span data-stu-id="f8459-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="f8459-122">ช่วงเวลาของการเปลี่ยนภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="f8459-122">Slide transition interval</span></span> | <span data-ttu-id="f8459-123">ค่าในวินาที</span><span class="sxs-lookup"><span data-stu-id="f8459-123">A value in seconds</span></span>    | <span data-ttu-id="f8459-124">ช่วงเวลาสำหรับการเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="f8459-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="f8459-125">ชนิดการเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="f8459-125">Transition type</span></span>           | <span data-ttu-id="f8459-126">**สไลด์** หรือ **เฟด**</span><span class="sxs-lookup"><span data-stu-id="f8459-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="f8459-127">เอฟเฟกต์การเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="f8459-127">The transition effect between items.</span></span> |
| <span data-ttu-id="f8459-128">ซ่อนฟลิปเปอร์วงล้อ</span><span class="sxs-lookup"><span data-stu-id="f8459-128">Hide carousel flipper</span></span>     | <span data-ttu-id="f8459-129">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f8459-129">**True** or **False**</span></span> | <span data-ttu-id="f8459-130">ถ้าตั้งค่าเป็น **จริง** ตัวหมุนวงล้อและตัวบ่งชี้ลำดับจะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="f8459-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="f8459-131">อนุญาตการปิดวงล้อ</span><span class="sxs-lookup"><span data-stu-id="f8459-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="f8459-132">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f8459-132">**True** or **False**</span></span> | <span data-ttu-id="f8459-133">หากค่าถูกตั้งเป็น **จริง** ผู้ใช้สามารถปิดวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="f8459-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="f8459-134">เพิ่มโมดูลวงล้อไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="f8459-134">Add a carousel module to a page</span></span>

<span data-ttu-id="f8459-135">การเพิ่มโมดูลวงล้อไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f8459-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f8459-136">เลือก **สร้าง** เพื่อสร้างเท็มเพลตของหน้า</span><span class="sxs-lookup"><span data-stu-id="f8459-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="f8459-137">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตวงล้อ** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f8459-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f8459-138">ในช่อง **Body** ให้เพิ่มโมดูล **หน้าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f8459-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="f8459-139">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f8459-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="f8459-140">ใช้เท็มเพลตวงล้อที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจวงล้อ**</span><span class="sxs-lookup"><span data-stu-id="f8459-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="f8459-141">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="f8459-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="f8459-142">ในบานหน้าต่างด้านขวา ให้ตั้งค่า **ความกว้าง** เป็น **เต็มหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="f8459-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="f8459-143">ภายใต้ **โครงร่างเพจ** ให้เพิ่มโมดูลวงล้อไปยังโมดูลตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="f8459-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="f8459-144">เพิ่มโมดูลบล็อคเนื้อหาไปยังโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="f8459-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="f8459-145">ตั้งค่าคุณสมบัติของโมดูลบล็อคเนื้อหาโดยการให้ **หัวข้อ** **ลิงก์** **โครงร่าง** และคุณสมบัติอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f8459-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="f8459-146">เพิ่มและตั้งค่าคอนฟิกโมดูลบล็อคเนื้อหาอื่น</span><span class="sxs-lookup"><span data-stu-id="f8459-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="f8459-147">ตั้งค่าคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้อ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f8459-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="f8459-148">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="f8459-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f8459-149">หน้าควรแสดงวงล้อที่มีสองโมดูลที่อยู่ภายใน (โมดูลฮีโร่และโมดูลคุณลักษณะ)</span><span class="sxs-lookup"><span data-stu-id="f8459-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="f8459-150">คุณสามารถเปลี่ยนคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้ ฮีโร่ และคุณลักษณะ เพื่อให้บรรลุผลที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="f8459-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="f8459-151">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f8459-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8459-152">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f8459-152">Additional resources</span></span>

[<span data-ttu-id="f8459-153">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f8459-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f8459-154">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="f8459-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f8459-155">โมดูลบล็อคข้อความ</span><span class="sxs-lookup"><span data-stu-id="f8459-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f8459-156">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f8459-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f8459-157">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="f8459-157">Video player module</span></span>](add-video-player.md)
