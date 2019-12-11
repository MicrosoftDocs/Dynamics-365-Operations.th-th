---
title: โมดูลวงล้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลวงล้อ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785248"
---
# <a name="carousel-module"></a><span data-ttu-id="e977a-103">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e977a-104">หัวข้อนี้ครอบคลุมถึงโมดูลวงล้อ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e977a-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e977a-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e977a-105">Overview</span></span>

<span data-ttu-id="e977a-106">โมดูลวงล้อจะใช้เพื่อจัดเก็บสินค้าที่มีการส่งเสริมการขายหลายรายการในวงล้อที่ลูกค้าสามารถเลือกดูได้</span><span class="sxs-lookup"><span data-stu-id="e977a-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="e977a-107">โมดูลคอนเทนเนอร์พิเศษที่โฮสต์โมดูลอื่นๆไว้</span><span class="sxs-lookup"><span data-stu-id="e977a-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="e977a-108">ตัวอย่างเช่น ผู้ค้าปลีกสามารถใช้โมดูลวงล้อบนโฮมเพจเพื่อแสดงผลิตภัณฑ์ใหม่ หรือโปรโมชั่นต่างๆได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="e977a-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="e977a-109">คุณสามารถเพิ่มฮีโร่และโมดูลคุณลักษณะภายในโมดูลวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="e977a-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="e977a-110">คุณสมบัติของโมดูลวงล้อ แล้วกำหนดวิธีการแสดงผลโมดูล</span><span class="sxs-lookup"><span data-stu-id="e977a-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="e977a-111">ตัวอย่างของโมดูลคุณวงล้อในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e977a-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="e977a-112">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="e977a-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="e977a-113">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e977a-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="e977a-114">วงล้อสามารถใช้ได้บนหน้าการตลาดใดๆ เพื่อส่งเสริมการส่งเสริมการขาย หรือผลิตภัณฑ์ หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="e977a-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="e977a-115">คุณสมบัติโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-115">Carousel module properties</span></span>

| <span data-ttu-id="e977a-116">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="e977a-116">Property name</span></span>             | <span data-ttu-id="e977a-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="e977a-117">Value</span></span>                                | <span data-ttu-id="e977a-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e977a-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="e977a-119">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e977a-119">Autoplay</span></span>                  | <span data-ttu-id="e977a-120">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="e977a-120">**True** or **False**</span></span>                | <span data-ttu-id="e977a-121">ถ้ามีการตั้งค่าเป็น **จริง** การเปลี่ยนแปลงระหว่างรายการภายในวงล้อจะเกิดขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e977a-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="e977a-122">ถ้าตั้งค่าเป็น **เท็จ** จะไม่มีการเปลี่ยนแปลงใดๆ เกิดขึ้นนอกจากลูกค้าจะใช้แป้นพิมพ์หรือเมาส์ เพื่อย้ายจากสินค้าหนึ่งไปยังรายการถัดไป</span><span class="sxs-lookup"><span data-stu-id="e977a-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="e977a-123">ช่วงเวลาของการเปลี่ยนภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="e977a-123">Slide transition interval</span></span> | <span data-ttu-id="e977a-124">ค่าในวินาที</span><span class="sxs-lookup"><span data-stu-id="e977a-124">A value in seconds</span></span>                   | <span data-ttu-id="e977a-125">ช่วงเวลาสำหรับการเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="e977a-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="e977a-126">ภาพเคลื่อนไหวของการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="e977a-126">Transition animation</span></span>      | <span data-ttu-id="e977a-127">**สไลด์** หรือ **เฟด**</span><span class="sxs-lookup"><span data-stu-id="e977a-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="e977a-128">ผลการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="e977a-128">The transition effect.</span></span> |
| <span data-ttu-id="e977a-129">ความกว้าง</span><span class="sxs-lookup"><span data-stu-id="e977a-129">Width</span></span>                     | <span data-ttu-id="e977a-130">**พอดีกับคอนเทนเนอร์** หรือ **เต็มหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="e977a-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="e977a-131">ถ้ามีการตั้งค่าให้ **พอดีคอนเทนเนอร์** สินค้าที่อยู่ภายในวงล้อจะถูกจำกัดโดยความกว้างของวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="e977a-132">ถ้ามีการตั้งค่าให้ **เต็มหน้าจอ** สินค้าจะไม่ถูกจำกัดไว้ที่ความกว้างของวงล้อ แต่สามารถไปที่โหมดเต็มหน้าจอได้</span><span class="sxs-lookup"><span data-stu-id="e977a-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="e977a-133">คุณสามารถเปลี่ยนค่าเพื่อให้บรรลุโครงร่างที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="e977a-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="e977a-134">เพิ่มโมดูลวงล้อไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="e977a-134">Add a carousel module to a page</span></span>

<span data-ttu-id="e977a-135">การเพิ่มโมดูลวงล้อไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e977a-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e977a-136">สร้างแม่แบบเพจซึ่งชื่อ **เท็มเพลตวงล้อ**</span><span class="sxs-lookup"><span data-stu-id="e977a-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="e977a-137">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="e977a-138">เพิ่มโมดูลฮีโร่ให้กับโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="e977a-139">เพิ่มโมดูลคุณลักษณะให้กับโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="e977a-140">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="e977a-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="e977a-141">ใช้เท็มเพลตวงล้อที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจวงล้อ**</span><span class="sxs-lookup"><span data-stu-id="e977a-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="e977a-142">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="e977a-143">ตั้งค่าคุณสมบัติ **ความกว้าง** ของโมดูลวงล้อ เป็น **เต็มหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="e977a-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="e977a-144">ตั้งค่าคุณสมบัติ **การเปลี่ยนภาพ** **สไลด์**</span><span class="sxs-lookup"><span data-stu-id="e977a-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="e977a-145">เพิ่มโมดูลฮีโร่ให้กับโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="e977a-146">ในโมดูลฮีโร่ ให้เพิ่มรูปภาพและหัวข้อ แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e977a-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="e977a-147">เพิ่มโมดูลคุณลักษณะให้กับโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e977a-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="e977a-148">ในโมดูลคุณลักษณะ เพิ่มรูปภาพ ส่วนหัว และย่อหน้าของข้อความ</span><span class="sxs-lookup"><span data-stu-id="e977a-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="e977a-149">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="e977a-149">Save and preview the page.</span></span> <span data-ttu-id="e977a-150">หน้าควรแสดงวงล้อที่มีสองโมดูลที่อยู่ภายใน (โมดูลฮีโร่และโมดูลคุณลักษณะ)</span><span class="sxs-lookup"><span data-stu-id="e977a-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="e977a-151">คุณสามารถเปลี่ยนคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้ ฮีโร่ และคุณลักษณะ เพื่อให้บรรลุผลที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="e977a-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="e977a-152">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="e977a-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e977a-153">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e977a-153">Additional resources</span></span>

[<span data-ttu-id="e977a-154">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e977a-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e977a-155">โมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e977a-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="e977a-156">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="e977a-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e977a-157">โมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="e977a-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e977a-158">โมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e977a-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="e977a-159">โมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="e977a-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="e977a-160">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="e977a-160">Video player module</span></span>](add-video-player.md)
