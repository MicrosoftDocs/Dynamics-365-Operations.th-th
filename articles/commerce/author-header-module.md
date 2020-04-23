---
title: โมดูลหัวข้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce
author: anupamar
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261455"
---
# <a name="header-module"></a><span data-ttu-id="58653-103">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="58653-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="58653-104">หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="58653-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="58653-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="58653-105">Overview</span></span>

<span data-ttu-id="58653-106">ใน Dynamics 365 Commerce ส่วนหัวของหน้าประกอบด้วยหลายโมดูล เช่น ส่วนหัว เมนูนำทาง การค้นหา แบนเนอร์โปรโมชัน และโมดูลการยินยอมเก็บคุกกี้</span><span class="sxs-lookup"><span data-stu-id="58653-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="58653-107">โมดูลของส่วนหัวรวมถึงโลโก้ของไซต์ ลิงก์ไปยังลำดับชั้นการนำทาง ลิงก์ไปยังหน้าอื่น ๆ บนไซต์ สัญลักษณ์รถเข็น สัญลักษณ์สิ่งที่ต้องการ ตัวเลือกการลงชื่อเข้าใช้ และแถบค้นหา</span><span class="sxs-lookup"><span data-stu-id="58653-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="58653-108">โมดูลส่วนหัวจะถูกปรับให้เหมาะสมโดยอัตโนมัติสำหรับอุปกรณ์ที่ไซต์กำลังดู (อธิบายอีกอย่างคือ อุปกรณ์เดสก์ทอป หรืออุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="58653-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="58653-109">ตัวอย่างเช่น บนอุปกรณ์เคลื่อนที่ แถบนำทางจะถูกยุบลงในปุ่ม **เมนู** (ซึ่งบางครั้งเรียกว่า *เมนู hamburger*)</span><span class="sxs-lookup"><span data-stu-id="58653-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="58653-110">คุณสมบัติของโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="58653-110">Properties of a header module</span></span>

<span data-ttu-id="58653-111">โมดูลส่วนหัวสนับสนุนคุณสมบัติ **รูปโลโก้** **ลิงก์ของโลโก้** และ **ลิงก์บัญชีของฉัน**</span><span class="sxs-lookup"><span data-stu-id="58653-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="58653-112">คุณสมบัติ **รูปโลโก้** และ **ลิงค์โลโก้** ใช้เพื่อกำหนดโลโก้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="58653-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="58653-113">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เพิ่มโลโก้](add-logo.md)</span><span class="sxs-lookup"><span data-stu-id="58653-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="58653-114">คุณสมบัติ **ลิงก์บัญชีของฉัน** สามารถใช้ในการกำหนดหน้าบัญชีที่เจ้าของไซต์ต้องการแสดงลิงก์ด่วนในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="58653-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="58653-115">โมดูลที่มีอยู่ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="58653-115">Modules that are available in a header module</span></span>

<span data-ttu-id="58653-116">โมดูลต่อไปนี้สามารถใช้ได้ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="58653-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="58653-117">**เมนูนำทาง** – เมนูนำทางแสดงถึงลำดับชั้นการนำทางช่องทาง และลิงค์การนำทางแบบคงที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="58653-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="58653-118">ลำดับชั้นการนำทางของช่องทางสามารถตั้งค่าคอนฟิกใน Dynamics 365 Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="58653-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="58653-119">เมนูนำทางมีคุณสมบัติ **ต้นทางการนำทาง** ที่ใช้เพื่อระบุรายการเมนูการนำทางของ Retail Server และรายการเมนูแบบคงที่เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="58653-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="58653-120">ถ้ามีการระบุรายการเมนูแบบคงที่เป็นแหล่งที่มา จะสามารถระบุลิงก์ที่สัมพันธ์กับหน้าอื่น ๆ บนไซต์ได้</span><span class="sxs-lookup"><span data-stu-id="58653-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="58653-121">สินค้าที่จัดโครงแบบจะปรากฏเป็นการนำทางส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="58653-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="58653-122">**การค้นหา** - โมดูลการค้นหาจะช่วยให้ผู้ใช้ป้อนคำที่ใช้ค้นหา เพื่อค้นหาผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="58653-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="58653-123">URL เริ่มต้นของหน้าการค้นหา และต้องระบุพารามิเตอร์การสอบถามที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="58653-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="58653-124">โมดูลการค้นหาจะมีคุณสมบัติซึ่งช่วยให้คุณสามารถระงับปุ่มค้นหา หรือป้ายชื่อตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="58653-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="58653-125">โมดูลที่ใช้ในการค้นหายังสนับสนุนตัวเลือกการแนะนำอัตโนมัติ เช่น ผลิตภัณฑ์ คำสำคัญ และผลการค้นหาของประเภท</span><span class="sxs-lookup"><span data-stu-id="58653-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="58653-126">**ไอคอนรถเข็น** - โมดูลไอคอนรถเข็นแสดงถึงไอคอนรถเข็นซึ่งแสดงจำนวนของสินค้าในรถเข็นในเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="58653-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="58653-127">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลไอคอนรถเข็น](cart-icon-module.md)</span><span class="sxs-lookup"><span data-stu-id="58653-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="58653-128">สร้างโมดูลส่วนหัวของหน้า</span><span class="sxs-lookup"><span data-stu-id="58653-128">Create a header module for a page</span></span>

<span data-ttu-id="58653-129">เมื่อต้องการสร้างโมดูลส่วนหัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="58653-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="58653-130">สร้างส่วนย่อยที่มีชื่อว่า **ส่วนย่อยของส่วนหัว** และเพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="58653-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="58653-131">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลคอนเทนเนอร์ ตั้งค่า **ความกว้าง** เป็น **เต็มคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="58653-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="58653-132">เพิ่มแบนเนอร์โปรโมชั่นและโมดูลการยินยอมใช้คุกกี้ให้กับโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="58653-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="58653-133">เพิ่มโมดูลคอนเทนอร์อื่นไปยังส่วน และตั้งค่า **ความกว้าง** เป็น **เต็มคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="58653-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="58653-134">เพิ่มโมดูลส่วนหัวให้กับโมดูลคอนเทนเนอร์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="58653-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="58653-135">ในช่อง **เมนูนำทาง** ของโมดูลส่วนหัว ให้เพิ่มโมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="58653-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="58653-136">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูนำทาง ให้ตั้งค่าคอนฟิกคุณสมบัติของโมดูเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="58653-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="58653-137">ในช่อง **ค้นหา** ของโมดูลใหม่ ให้เพิ่มโมดูลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="58653-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="58653-138">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลค้นหา ให้ตั้งค่าคอนฟิกคุณสมบัติของโมดูค้นหา</span><span class="sxs-lookup"><span data-stu-id="58653-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="58653-139">ในช่อง **โมดูลไอคอนรถเข็น** ของโมดูลส่วนหัว ให้เพิ่มโมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="58653-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="58653-140">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลโมดูลไอคอนรถเข็น ให้ตั้งค่าคอนฟิกคุณสมบัติของโมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="58653-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="58653-141">ถ้าคุณต้องการให้ไอคอนรถเข็นแสดงรถเข็นแบบมินิเมื่อวางเมาส์ไว้เหนือ ให้เลือก **จริง** หรือ **แสดงรถเข็นแบบมินิ**</span><span class="sxs-lookup"><span data-stu-id="58653-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="58653-142">บันทึกส่วนของเพจ แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="58653-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="58653-143">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกเพจ ให้ทำตามขั้นตอนต่อไปนี้บนทุกแม่แบบเพจที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="58653-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="58653-144">ในช่อง **หลัก** ของเพจเริ่มต้น ให้เพิ่มส่วนหัวของเพจที่มีโมดูลส่วนหัวไปยังส่วนหัวในช่องหลัก</span><span class="sxs-lookup"><span data-stu-id="58653-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="58653-145">บันทึกเท็มเพลต แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="58653-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58653-146">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="58653-146">Additional resources</span></span>

[<span data-ttu-id="58653-147">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="58653-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="58653-148">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="58653-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="58653-149">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="58653-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="58653-150">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="58653-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="58653-151">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="58653-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="58653-152">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="58653-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="58653-153">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="58653-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="58653-154">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="58653-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="58653-155">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="58653-155">Footer module</span></span>](author-footer-module.md)
