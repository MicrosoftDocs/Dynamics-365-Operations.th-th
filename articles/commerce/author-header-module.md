---
title: โมดูลหัวข้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce
author: anupamar
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: eb440a8fb67888c9411ad5998fead4d00982b436
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761235"
---
# <a name="header-module"></a><span data-ttu-id="19747-103">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="19747-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="19747-104">หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="19747-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="19747-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="19747-105">Overview</span></span>

<span data-ttu-id="19747-106">ใน Dynamics 365 Commerce ส่วนหัวของหน้าจะมีการตั้งค่าคอนฟิกเป็นส่วนย่อยซึ่งมีโมดูลส่วนหัว แบนเนอร์โปรโมชัน และโมดูลการยินยอมใช้คุกกี้</span><span class="sxs-lookup"><span data-stu-id="19747-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="19747-107">โมดูลของส่วนหัวรวมถึงโลโก้ของไซต์ ลิงก์ไปยังลำดับชั้นการนำทาง ลิงก์ไปยังหน้าอื่น ๆ บนไซต์ โมดูลไอคอนรถเข็น สัญลักษณ์สิ่งที่ต้องการ ตัวเลือกการลงชื่อเข้าใช้ และแถบค้นหา</span><span class="sxs-lookup"><span data-stu-id="19747-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="19747-108">โมดูลส่วนหัวจะถูกปรับให้เหมาะสมโดยอัตโนมัติสำหรับอุปกรณ์ที่ไซต์กำลังดู (อธิบายอีกอย่างคือ อุปกรณ์เดสก์ทอป หรืออุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="19747-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="19747-109">ตัวอย่างเช่น บนอุปกรณ์เคลื่อนที่ แถบนำทางจะถูกยุบลงในปุ่ม **เมนู** (ซึ่งบางครั้งเรียกว่า *เมนู hamburger*)</span><span class="sxs-lookup"><span data-stu-id="19747-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="19747-110">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลส่วนหัวบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="19747-110">The following image shows an example of a header module on a home page.</span></span>

![ตัวอย่างของโมดูลส่วนหัว](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="19747-112">คุณสมบัติของโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="19747-112">Properties of a header module</span></span>

<span data-ttu-id="19747-113">โมดูลส่วนหัวสนับสนุนคุณสมบัติ **รูปโลโก้** **ลิงก์ของโลโก้** และ **ลิงก์บัญชีของฉัน**</span><span class="sxs-lookup"><span data-stu-id="19747-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="19747-114">คุณสมบัติ **รูปโลโก้** และ **ลิงค์โลโก้** ใช้เพื่อกำหนดโลโก้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="19747-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="19747-115">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เพิ่มโลโก้](add-logo.md)</span><span class="sxs-lookup"><span data-stu-id="19747-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="19747-116">คุณสมบัติ **ลิงก์บัญชีของฉัน** สามารถใช้ในการกำหนดหน้าบัญชีที่เจ้าของไซต์ต้องการแสดงลิงก์ด่วนในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="19747-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="19747-117">โมดูลที่มีอยู่ในโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="19747-117">Modules that are available within a header module</span></span>

<span data-ttu-id="19747-118">โมดูลต่อไปนี้สามารถใช้ได้ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="19747-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="19747-119">**เมนูนำทาง** – เมนูนำทางแสดงถึงลำดับชั้นการนำทางช่องทาง และลิงค์การนำทางแบบคงที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="19747-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="19747-120">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลเมนูนำทาง](nav-menu-module.md)</span><span class="sxs-lookup"><span data-stu-id="19747-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="19747-121">**การค้นหา** - โมดูลการค้นหาจะช่วยให้ผู้ใช้ป้อนคำที่ใช้ค้นหา เพื่อค้นหาผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="19747-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="19747-122">URL เริ่มต้นของหน้าการค้นหา และต้องระบุพารามิเตอร์การสอบถามที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="19747-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="19747-123">โมดูลการค้นหาจะมีคุณสมบัติซึ่งช่วยให้คุณสามารถระงับปุ่มค้นหา หรือป้ายชื่อตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="19747-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="19747-124">โมดูลที่ใช้ในการค้นหายังสนับสนุนตัวเลือกการแนะนำอัตโนมัติ เช่น ผลิตภัณฑ์ คำสำคัญ และผลการค้นหาของประเภท</span><span class="sxs-lookup"><span data-stu-id="19747-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="19747-125">**ไอคอนรถเข็น** - โมดูลไอคอนรถเข็นแสดงถึงไอคอนรถเข็นซึ่งแสดงจำนวนของสินค้าในรถเข็นในเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="19747-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="19747-126">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลไอคอนรถเข็น](cart-icon-module.md)</span><span class="sxs-lookup"><span data-stu-id="19747-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="19747-127">สร้างส่วนย่อยของส่วนหัวของหน้า</span><span class="sxs-lookup"><span data-stu-id="19747-127">Create a header fragment for a page</span></span>

<span data-ttu-id="19747-128">เมื่อต้องการสร้างส่วนย่อยของส่วนหัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="19747-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="19747-129">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="19747-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="19747-130">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **คอนเทนเนอร์** ป้อนชื่อสำหรับส่วนย่อย แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19747-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="19747-131">เลือก **คอนเทนเนอร์เริ่มต้น** จากนั้นในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคุณสมบัติของ **ความกว้าง** เป็น **เติมหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="19747-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="19747-132">ในช่อง **คอนเทนเนอร์เริ่มต้น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="19747-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="19747-133">ในกล่องโต้ตอบ **เพิ่มโมดูล** เลือกโมดูล **การยินยอมใช้คุกกี้**, **ส่วนหัว** และ **แบนเนอร์โปรโมชัน** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19747-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="19747-134">ในบานหน้าต่างคุณสมบัติของโมดูล **แบนเนอร์โปรโมชัน** ให้เลือก **เพิ่มข้อความ** แล้วเลือก **ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="19747-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="19747-135">ในกล่องโต้ตอบ **ข้อความ** เพิ่มข้อความและลิงก์สำหรับเนื้อหาโปรโมชัน แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19747-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="19747-136">ในบานหน้าต่างคุณสมบัติของโมดูล **การยินยอมใช้คุกกี้** ให้เพิ่มและตั้งค่าคอนฟิกข้อความและลิงก์ไปยังหน้าความเป็นส่วนตัวของไซต์</span><span class="sxs-lookup"><span data-stu-id="19747-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="19747-137">ในช่อง **เมนูการนำทาง** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="19747-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="19747-138">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **เมนูการนำทาง** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19747-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="19747-139">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูนำทางภายใต้ **ที่มาของเมนูนำทาง** ให้เลือก **Retail Server**</span><span class="sxs-lookup"><span data-stu-id="19747-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="19747-140">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูนำทางภายใต้ **รายการเมนูแบบคงที่** ให้เลือก **เพิ่มรายการเมนู** แล้วเลือก **รายการเมนู**</span><span class="sxs-lookup"><span data-stu-id="19747-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="19747-141">ในกล่องโต้ตอบ **รายการเมนู** ภายใต้ **ข้อความรายการเมนู** ป้อน "การติดต่อ"</span><span class="sxs-lookup"><span data-stu-id="19747-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="19747-142">ในกล่องโต้ตอบ **รายการเมนู** ภายใต้ **เป้าหมายลิงก์รายการเมนู** ให้เลือก **เพิ่มลิงก์**</span><span class="sxs-lookup"><span data-stu-id="19747-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="19747-143">ในกล่องโต้ตอบ **เพิ่มลิงก์** ให้เลือก URL สำหรับหน้า "การติดต่อ" ของไซต์ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19747-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="19747-144">ในกล่องโต้ตอบ **รายการเมนู** ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19747-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="19747-145">ในช่อง **ค้นหา** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="19747-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="19747-146">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ค้นหา** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19747-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="19747-147">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลค้นหา ให้ตั้งค่าคอนฟิกคุณสมบัติตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="19747-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="19747-148">ในช่อง **ไอคอนรถเข็น** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="19747-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="19747-149">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ไอคอนรถเข็น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19747-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="19747-150">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูไอคอนรถเข็น ให้ตั้งค่าคอนฟิกคุณสมบัติตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="19747-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="19747-151">ถ้าคุณต้องการให้ไอคอนรถเข็นแสดงสรุปรถเข็น (หรือที่เรียกอีกอย่างหนึ่งว่ารถเข็นมินิ) เมื่อผู้ใช้เลื่อนเมาส์ไปวางไว้ เลือก **แสดงมินิรถเข็น**</span><span class="sxs-lookup"><span data-stu-id="19747-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="19747-152">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="19747-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="19747-153">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกหน้า ให้ทำตามขั้นตอนต่อไปนี้บนทุกเท็มเพลตหน้าที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="19747-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="19747-154">ในช่อง **ส่วนหัว** ของโมดูล **หน้าเริ่มต้น** ให้เพิ่มส่วนย่อยที่เป็นส่วนท้ายที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="19747-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="19747-155">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="19747-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19747-156">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="19747-156">Additional resources</span></span>

[<span data-ttu-id="19747-157">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="19747-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="19747-158">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="19747-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="19747-159">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="19747-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="19747-160">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="19747-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="19747-161">โมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="19747-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="19747-162">การยอมรับคุกกี้</span><span class="sxs-lookup"><span data-stu-id="19747-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="19747-163">โมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="19747-163">Footer module</span></span>](author-footer-module.md)
