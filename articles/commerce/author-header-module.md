---
title: โมดูลหัวข้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025714"
---
# <a name="header-module"></a><span data-ttu-id="da3be-103">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="da3be-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="da3be-104">หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="da3be-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da3be-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="da3be-105">Overview</span></span>

<span data-ttu-id="da3be-106">ใน Dynamics 365 Commerce ส่วนหัวของหน้าประกอบด้วยหลายโมดูล เช่น ส่วนหัว เมนูนำทาง การค้นหา แบนเนอร์โปรโมชัน และโมดูลการยินยอมเก็บคุกกี้</span><span class="sxs-lookup"><span data-stu-id="da3be-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="da3be-107">โมดูลของส่วนหัวรวมถึงโลโก้ของไซต์ ลิงก์ไปยังลำดับชั้นการนำทาง ลิงก์ไปยังหน้าอื่น ๆ บนไซต์ สัญลักษณ์รถเข็น สัญลักษณ์สิ่งที่ต้องการ ตัวเลือกการลงชื่อเข้าใช้ และแถบค้นหา</span><span class="sxs-lookup"><span data-stu-id="da3be-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="da3be-108">โมดูลส่วนหัวจะถูกปรับให้เหมาะสมโดยอัตโนมัติสำหรับอุปกรณ์ที่ไซต์กำลังดู (อธิบายอีกอย่างคือ อุปกรณ์เดสก์ทอป หรืออุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="da3be-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="da3be-109">ตัวอย่างเช่น บนอุปกรณ์เคลื่อนที่ แถบนำทางจะถูกยุบลงในปุ่ม **เมนู** (ซึ่งบางครั้งเรียกว่า *เมนู hamburger*)</span><span class="sxs-lookup"><span data-stu-id="da3be-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="da3be-110">คุณสมบัติของโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="da3be-110">Properties of a header module</span></span>

<span data-ttu-id="da3be-111">โมดูลส่วนหัวสนับสนุนคุณสมบัติ **รูปโลโก้** **ลิงก์ของโลโก้** และ **ลิงก์บัญชีของฉัน**</span><span class="sxs-lookup"><span data-stu-id="da3be-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="da3be-112">คุณสมบัติ **รูปโลโก้** และ **ลิงค์โลโก้** ใช้เพื่อกำหนดโลโก้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="da3be-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="da3be-113">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เพิ่มโลโก้](add-logo.md)</span><span class="sxs-lookup"><span data-stu-id="da3be-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="da3be-114">คุณสมบัติ **ลิงก์บัญชีของฉัน** สามารถใช้ในการกำหนดหน้าบัญชีที่เจ้าของไซต์ต้องการแสดงลิงก์ด่วนในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="da3be-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="da3be-115">โมดูลที่มีอยู่ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="da3be-115">Modules that are available in a header module</span></span>

<span data-ttu-id="da3be-116">โมดูลต่อไปนี้สามารถใช้ได้ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="da3be-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="da3be-117">**เมนูนำทาง** – เมนูนำทางแสดงถึงลำดับชั้นการนำทางช่องทาง และลิงค์การนำทางแบบคงที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="da3be-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="da3be-118">ลำดับชั้นการนำทางของช่องทางสามารถตั้งค่าคอนฟิกใน Dynamics 365 Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="da3be-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="da3be-119">เมนูนำทางมีคุณสมบัติ **ต้นทางการนำทาง** ที่ใช้เพื่อระบุรายการเมนูการนำทางของ Retail Server และรายการเมนูแบบคงที่เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="da3be-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="da3be-120">ถ้ามีการระบุรายการเมนูแบบคงที่เป็นแหล่งที่มา จะสามารถระบุลิงก์ที่สัมพันธ์กับหน้าอื่น ๆ บนไซต์ได้</span><span class="sxs-lookup"><span data-stu-id="da3be-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="da3be-121">สินค้าที่จัดโครงแบบจะปรากฏเป็นการนำทางส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="da3be-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="da3be-122">**การค้นหา** - โมดูลการค้นหาจะช่วยให้ผู้ใช้ป้อนคำที่ใช้ค้นหา เพื่อค้นหาผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="da3be-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="da3be-123">URL เริ่มต้นของหน้าการค้นหา และต้องระบุพารามิเตอร์การสอบถามที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="da3be-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="da3be-124">โมดูลการค้นหาจะมีคุณสมบัติซึ่งช่วยให้คุณสามารถระงับปุ่มค้นหา หรือป้ายชื่อตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="da3be-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="da3be-125">โมดูลที่ใช้ในการค้นหายังสนับสนุนตัวเลือกการแนะนำอัตโนมัติ เช่น ผลิตภัณฑ์ คำสำคัญ และผลการค้นหาของประเภท</span><span class="sxs-lookup"><span data-stu-id="da3be-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="da3be-126">สร้างโมดูลส่วนหัวของหน้า</span><span class="sxs-lookup"><span data-stu-id="da3be-126">Create a header module for a page</span></span>

<span data-ttu-id="da3be-127">เมื่อต้องการสร้างโมดูลส่วนหัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="da3be-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="da3be-128">สร้างส่วนย่อยที่มีชื่อว่า **ส่วนย่อยของส่วนหัว** และเพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="da3be-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="da3be-129">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลคอนเทนเนอร์ ตั้งค่า **ความกว้าง** เป็น **เต็มคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="da3be-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="da3be-130">เพิ่มแบนเนอร์โปรโมชั่น และโมดูลการยินยอมใช้คุกกี้ให้กับโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="da3be-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="da3be-131">เพิ่มโมดูลคอนเทนอร์อื่นไปยังส่วน และตั้งค่า **ความกว้าง** เป็น **เต็มคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="da3be-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="da3be-132">เพิ่มโมดูลส่วนหัวให้กับโมดูลคอนเทนเนอร์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="da3be-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="da3be-133">ในช่อง **เมนูนำทาง** ของโมดูลส่วนหัว ให้เพิ่มโมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="da3be-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="da3be-134">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูนำทาง ให้ตั้งค่าคอนฟิกคุณสมบัติของโมดูเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="da3be-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="da3be-135">ในช่อง **ค้นหา** ของโมดูลใหม่ ให้เพิ่มโมดูลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="da3be-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="da3be-136">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลค้นหา ให้ตั้งค่าคอนฟิกคุณสมบัติของโมดูค้นหา</span><span class="sxs-lookup"><span data-stu-id="da3be-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="da3be-137">บันทึกส่วนของหน้า แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="da3be-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="da3be-138">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกเพจ ให้ทำตามขั้นตอนต่อไปนี้บนทุกแม่แบบเพจที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="da3be-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="da3be-139">ในช่อง **หลัก** ของเพจเริ่มต้น ให้เพิ่มส่วนหัวของเพจที่มีโมดูลส่วนหัวไปยังส่วนหัวในช่องหลัก</span><span class="sxs-lookup"><span data-stu-id="da3be-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="da3be-140">บันทึกแม่แบบ แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="da3be-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da3be-141">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="da3be-141">Additional resources</span></span>

[<span data-ttu-id="da3be-142">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="da3be-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="da3be-143">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="da3be-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="da3be-144">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="da3be-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="da3be-145">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="da3be-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="da3be-146">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="da3be-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="da3be-147">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="da3be-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="da3be-148">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="da3be-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="da3be-149">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="da3be-149">Footer module</span></span>](author-footer-module.md)
