---
title: โมดูลวงล้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลวงล้อ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025792"
---
# <a name="carousel-module"></a><span data-ttu-id="3a088-103">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="3a088-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3a088-104">หัวข้อนี้ครอบคลุมถึงโมดูลวงล้อ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3a088-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3a088-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="3a088-105">Overview</span></span>

<span data-ttu-id="3a088-106">โมดูลวงล้อจะใช้เพื่อจัดเก็บสินค้าที่มีการส่งเสริมการขายหลายรายการ (รวมถึงรูปภาพ) ในแถบวงล้อที่หมุนได้โดยลูกค้าสามารถเลือกดูได้</span><span class="sxs-lookup"><span data-stu-id="3a088-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="3a088-107">ตัวอย่างเช่น ผู้ค้าปลีกสามารถใช้โมดูลวงล้อบนโฮมเพจเพื่อแสดงผลิตภัณฑ์ใหม่ หรือโปรโมชั่นต่างๆได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="3a088-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="3a088-108">คุณสามารถเพิ่มบล็อกเนื้อหา ภายในโมดูลวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="3a088-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="3a088-109">คุณสมบัติของโมดูลวงล้อ แล้วกำหนดวิธีการแสดงผลโมดูล</span><span class="sxs-lookup"><span data-stu-id="3a088-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="3a088-110">ตัวอย่างของโมดูลคุณวงล้อในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="3a088-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="3a088-111">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="3a088-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="3a088-112">วงล้อที่มีหลายโมดูลการส่งเสริมการขายภายใน ที่สามารถใช้ได้บนหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3a088-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="3a088-113">วงล้อสามารถใช้ได้บนหน้าการตลาดใดๆ เพื่อส่งเสริมการส่งเสริมการขาย หรือผลิตภัณฑ์ หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="3a088-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="3a088-114">คุณสมบัติโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="3a088-114">Carousel module properties</span></span>

| <span data-ttu-id="3a088-115">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3a088-115">Property name</span></span>             | <span data-ttu-id="3a088-116">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="3a088-116">Value</span></span>                 | <span data-ttu-id="3a088-117">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3a088-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="3a088-118">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3a088-118">Autoplay</span></span>                  | <span data-ttu-id="3a088-119">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="3a088-119">**True** or **False**</span></span> | <span data-ttu-id="3a088-120">ถ้ามีการตั้งค่าเป็น **จริง** การเปลี่ยนแปลงระหว่างรายการภายในวงล้อจะเกิดขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3a088-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="3a088-121">ถ้าตั้งค่าเป็น **เท็จ** จะไม่มีการเปลี่ยนแปลงใดๆ เกิดขึ้นนอกจากลูกค้าจะใช้แป้นพิมพ์หรือเมาส์ เพื่อย้ายจากสินค้าหนึ่งไปยังรายการถัดไป</span><span class="sxs-lookup"><span data-stu-id="3a088-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="3a088-122">ช่วงเวลาของการเปลี่ยนภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="3a088-122">Slide transition interval</span></span> | <span data-ttu-id="3a088-123">ค่าในวินาที</span><span class="sxs-lookup"><span data-stu-id="3a088-123">A value in seconds</span></span>    | <span data-ttu-id="3a088-124">ช่วงเวลาสำหรับการเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a088-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="3a088-125">ชนิดการเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="3a088-125">Transition type</span></span>           | <span data-ttu-id="3a088-126">**สไลด์** หรือ **เฟด**</span><span class="sxs-lookup"><span data-stu-id="3a088-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="3a088-127">เอฟเฟกต์การเปลี่ยนระหว่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a088-127">The transition effect between items.</span></span> |
| <span data-ttu-id="3a088-128">ซ่อนฟลิปเปอร์วงล้อ</span><span class="sxs-lookup"><span data-stu-id="3a088-128">Hide carousel flipper</span></span>     | <span data-ttu-id="3a088-129">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="3a088-129">**True** or **False**</span></span> | <span data-ttu-id="3a088-130">ถ้าตั้งค่าเป็น **จริง** ตัวหมุนวงล้อและตัวบ่งชี้ลำดับจะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="3a088-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="3a088-131">อนุญาตการปิดวงล้อ</span><span class="sxs-lookup"><span data-stu-id="3a088-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="3a088-132">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="3a088-132">**True** or **False**</span></span> | <span data-ttu-id="3a088-133">หากค่าถูกตั้งเป็น **จริง** ผู้ใช้สามารถปิดวงล้อได้</span><span class="sxs-lookup"><span data-stu-id="3a088-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="3a088-134">เพิ่มโมดูลวงล้อไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="3a088-134">Add a carousel module to a page</span></span>

<span data-ttu-id="3a088-135">การเพิ่มโมดูลวงล้อไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3a088-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3a088-136">สร้างแม่แบบเพจซึ่งชื่อ **เท็มเพลตวงล้อ**</span><span class="sxs-lookup"><span data-stu-id="3a088-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="3a088-137">ในช่อง **Body** ให้เพิ่มโมดูล **หน้าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="3a088-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="3a088-138">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="3a088-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="3a088-139">ใช้เท็มเพลตวงล้อที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจวงล้อ**</span><span class="sxs-lookup"><span data-stu-id="3a088-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="3a088-140">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="3a088-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="3a088-141">ในบานหน้าต่างด้านขวา ให้ตั้งค่า **ความกว้าง** เป็น **เต็มหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="3a088-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="3a088-142">ภายใต้ **โครงร่างเพจ** ให้เพิ่มโมดูลวงล้อไปยังโมดูลตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a088-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="3a088-143">เพิ่มโมดูลบล็อคเนื้อหาไปยังโมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="3a088-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="3a088-144">ตั้งค่าคุณสมบัติของโมดูลบล็อคเนื้อหาโดยการให้ **หัวข้อ** **ลิงก์** **โครงร่าง** และคุณสมบัติอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="3a088-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="3a088-145">เพิ่มและตั้งค่าคอนฟิกโมดูลบล็อคเนื้อหาอื่น</span><span class="sxs-lookup"><span data-stu-id="3a088-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="3a088-146">ตั้งค่าคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้อ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="3a088-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="3a088-147">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="3a088-147">Save and preview the page.</span></span> <span data-ttu-id="3a088-148">หน้าควรแสดงวงล้อที่มีสองโมดูลที่อยู่ภายใน (โมดูลฮีโร่และโมดูลคุณลักษณะ)</span><span class="sxs-lookup"><span data-stu-id="3a088-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="3a088-149">คุณสามารถเปลี่ยนคุณสมบัติเพิ่มเติมสำหรับโมดูลวงล้ ฮีโร่ และคุณลักษณะ เพื่อให้บรรลุผลที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="3a088-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="3a088-150">แก้ไขหน้าให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="3a088-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a088-151">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3a088-151">Additional resources</span></span>

[<span data-ttu-id="3a088-152">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3a088-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3a088-153">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="3a088-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="3a088-154">โมดูลบล็อคข้อความ</span><span class="sxs-lookup"><span data-stu-id="3a088-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="3a088-155">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="3a088-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="3a088-156">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="3a088-156">Video player module</span></span>](add-video-player.md)
