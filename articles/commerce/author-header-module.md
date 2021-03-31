---
title: โมดูลหัวข้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลส่วนหัวและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 569fb5ac3d30be30044ef9b928ecf1f6dde20aab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211435"
---
# <a name="header-module"></a><span data-ttu-id="f9fc0-103">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="f9fc0-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f9fc0-104">หัวข้อนี้ครอบคลุมถึงโมดูลส่วนหัวและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f9fc0-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f9fc0-105">ใน Dynamics 365 Commerce ส่วนหัวของหน้าจะมีการตั้งค่าคอนฟิกเป็นส่วนย่อยซึ่งมีโมดูลส่วนหัว แบนเนอร์โปรโมชัน และโมดูลการยินยอมใช้คุกกี้</span><span class="sxs-lookup"><span data-stu-id="f9fc0-105">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="f9fc0-106">โมดูลของส่วนหัวรวมถึงโลโก้ของไซต์ ลิงก์ไปยังลำดับชั้นการนำทาง ลิงก์ไปยังหน้าอื่น ๆ บนไซต์ โมดูลไอคอนรถเข็น สัญลักษณ์สิ่งที่ต้องการ ตัวเลือกการลงชื่อเข้าใช้ และแถบค้นหา</span><span class="sxs-lookup"><span data-stu-id="f9fc0-106">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="f9fc0-107">โมดูลส่วนหัวจะถูกปรับให้เหมาะสมโดยอัตโนมัติสำหรับอุปกรณ์ที่ไซต์กำลังดู (อธิบายอีกอย่างคือ อุปกรณ์เดสก์ทอป หรืออุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-107">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="f9fc0-108">ตัวอย่างเช่น บนอุปกรณ์เคลื่อนที่ แถบนำทางจะถูกยุบลงในปุ่ม **เมนู** (ซึ่งบางครั้งเรียกว่า *เมนู hamburger*)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-108">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="f9fc0-109">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลส่วนหัวบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-109">The following image shows an example of a header module on a home page.</span></span>

![ตัวอย่างของโมดูลส่วนหัว](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="f9fc0-111">คุณสมบัติของโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="f9fc0-111">Properties of a header module</span></span>

<span data-ttu-id="f9fc0-112">โมดูลส่วนหัวสนับสนุนคุณสมบัติ **รูปโลโก้** **ลิงก์ของโลโก้** และ **ลิงก์บัญชีของฉัน**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-112">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="f9fc0-113">คุณสมบัติ **รูปโลโก้** และ **ลิงค์โลโก้** ใช้เพื่อกำหนดโลโก้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="f9fc0-113">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="f9fc0-114">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เพิ่มโลโก้](add-logo.md)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-114">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="f9fc0-115">คุณสมบัติ **ลิงก์บัญชีของฉัน** สามารถใช้ในการกำหนดหน้าบัญชีที่เจ้าของไซต์ต้องการแสดงลิงก์ด่วนในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="f9fc0-115">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="f9fc0-116">โมดูลที่มีอยู่ในโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="f9fc0-116">Modules that are available within a header module</span></span>

<span data-ttu-id="f9fc0-117">โมดูลต่อไปนี้สามารถใช้ได้ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="f9fc0-118">**เมนูนำทาง** – เมนูนำทางแสดงถึงลำดับชั้นการนำทางช่องทาง และลิงค์การนำทางแบบคงที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="f9fc0-119">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลเมนูนำทาง](nav-menu-module.md)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-119">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="f9fc0-120">**การค้นหา** - โมดูลการค้นหาจะช่วยให้ผู้ใช้ป้อนคำที่ใช้ค้นหา เพื่อค้นหาผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="f9fc0-120">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="f9fc0-121">URL เริ่มต้นของหน้าการค้นหา และต้องระบุพารามิเตอร์การสอบถามที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-121">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="f9fc0-122">โมดูลการค้นหาจะมีคุณสมบัติซึ่งช่วยให้คุณสามารถระงับปุ่มค้นหา หรือป้ายชื่อตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-122">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="f9fc0-123">โมดูลที่ใช้ในการค้นหายังสนับสนุนตัวเลือกการแนะนำอัตโนมัติ เช่น ผลิตภัณฑ์ คำสำคัญ และผลการค้นหาของประเภท</span><span class="sxs-lookup"><span data-stu-id="f9fc0-123">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="f9fc0-124">**ไอคอนรถเข็น** - โมดูลไอคอนรถเข็นแสดงถึงไอคอนรถเข็นซึ่งแสดงจำนวนของสินค้าในรถเข็นในเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="f9fc0-124">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="f9fc0-125">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลไอคอนรถเข็น](cart-icon-module.md)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-125">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="f9fc0-126">**ตัวเลือกไซต์** - โมดูลตัวเลือกไซต์จะช่วยให้ผู้ใช้สามารถเรียกดูไซต์ที่กำหนดไว้ล่วงหน้าต่างๆ ได้ตามตลาด ภูมิภาค และตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="f9fc0-126">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="f9fc0-127">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลตัวเลือกไซต์](site-selector.md)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-127">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="f9fc0-128">**ตัวเลือกร้านค้า** - โมดูลตัวเลือกร้านค้าสามารถรวมอยู่ในช่องตัวเลือกร้านค้าของโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="f9fc0-128">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="f9fc0-129">นี่จะช่วยให้ผู้ใช้สามารถเลือกดูและค้นหาร้านค้าใกล้เคียงได้</span><span class="sxs-lookup"><span data-stu-id="f9fc0-129">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="f9fc0-130">นอกจากนี้ ผู้ใช้ยังสามารถระบุร้านค้าที่ต้องการได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="f9fc0-130">Users can also specify a preferred store.</span></span> <span data-ttu-id="f9fc0-131">หลังจากนั้น จะมีการแสดงร้านค้าดังกล่าวในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="f9fc0-131">That store will then be shown in the header.</span></span> <span data-ttu-id="f9fc0-132">เมื่อโมดูลตัวเลือกร้านค้ารวมอยู่ในโมดูลส่วนหัว คุณสมบัติของของ **โหมด** ดังกล่าวจะต้องถูกตั้งค่าเป็น **ค้นหาร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-132">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="f9fc0-133">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลตัวเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-133">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="f9fc0-134">การสนับสนุนสำหรับการใช้โมดูลไอคอนรถเข็นในโมดูลส่วนหัวมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.11</span><span class="sxs-lookup"><span data-stu-id="f9fc0-134">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="f9fc0-135">การสนับสนุนสำหรับการใช้โมดูลตัวเลือกไซต์ในโมดูลส่วนหัวมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.14</span><span class="sxs-lookup"><span data-stu-id="f9fc0-135">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="f9fc0-136">การสนับสนุนสำหรับการใช้โมดูลตัวเลือกร้านค้าในโมดูลส่วนหัวมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.15</span><span class="sxs-lookup"><span data-stu-id="f9fc0-136">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="f9fc0-137">สร้างส่วนย่อยของส่วนหัวของหน้า</span><span class="sxs-lookup"><span data-stu-id="f9fc0-137">Create a header fragment for a page</span></span>

<span data-ttu-id="f9fc0-138">เมื่อต้องการสร้างส่วนย่อยของส่วนหัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f9fc0-138">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="f9fc0-139">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="f9fc0-139">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="f9fc0-140">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **คอนเทนเนอร์** ป้อนชื่อสำหรับส่วนย่อย แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-140">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f9fc0-141">เลือก **คอนเทนเนอร์เริ่มต้น** จากนั้นในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคุณสมบัติของ **ความกว้าง** เป็น **เติมหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-141">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="f9fc0-142">ในช่อง **คอนเทนเนอร์เริ่มต้น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-142">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f9fc0-143">ในกล่องโต้ตอบ **เพิ่มโมดูล** เลือกโมดูล **การยินยอมใช้คุกกี้**, **ส่วนหัว** และ **แบนเนอร์โปรโมชัน** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-143">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="f9fc0-144">ในบานหน้าต่างคุณสมบัติของโมดูล **แบนเนอร์โปรโมชัน** ให้เลือก **เพิ่มข้อความ** แล้วเลือก **ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-144">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="f9fc0-145">ในกล่องโต้ตอบ **ข้อความ** เพิ่มข้อความและลิงก์สำหรับเนื้อหาโปรโมชัน แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-145">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="f9fc0-146">ในบานหน้าต่างคุณสมบัติของโมดูล **การยินยอมใช้คุกกี้** ให้เพิ่มและตั้งค่าคอนฟิกข้อความและลิงก์ไปยังหน้าความเป็นส่วนตัวของไซต์</span><span class="sxs-lookup"><span data-stu-id="f9fc0-146">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="f9fc0-147">ในช่อง **เมนูการนำทาง** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-147">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f9fc0-148">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **เมนูการนำทาง** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-148">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f9fc0-149">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูนำทางภายใต้ **ที่มาของเมนูนำทาง** ให้เลือก **Retail Server**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-149">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="f9fc0-150">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูนำทางภายใต้ **รายการเมนูแบบคงที่** ให้เลือก **เพิ่มรายการเมนู** แล้วเลือก **รายการเมนู**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-150">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="f9fc0-151">ในกล่องโต้ตอบ **รายการเมนู** ภายใต้ **ข้อความรายการเมนู** ป้อน "การติดต่อ"</span><span class="sxs-lookup"><span data-stu-id="f9fc0-151">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="f9fc0-152">ในกล่องโต้ตอบ **รายการเมนู** ภายใต้ **เป้าหมายลิงก์รายการเมนู** ให้เลือก **เพิ่มลิงก์**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-152">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="f9fc0-153">ในกล่องโต้ตอบ **เพิ่มลิงก์** ให้เลือก URL สำหรับหน้า "การติดต่อ" ของไซต์ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-153">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="f9fc0-154">ในกล่องโต้ตอบ **รายการเมนู** ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-154">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="f9fc0-155">ในช่อง **ค้นหา** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-155">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f9fc0-156">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ค้นหา** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-156">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f9fc0-157">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลค้นหา ให้ตั้งค่าคอนฟิกคุณสมบัติตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-157">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="f9fc0-158">ในช่อง **ไอคอนรถเข็น** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-158">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f9fc0-159">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ไอคอนรถเข็น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-159">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f9fc0-160">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูไอคอนรถเข็น ให้ตั้งค่าคอนฟิกคุณสมบัติตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-160">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="f9fc0-161">ถ้าคุณต้องการให้ไอคอนรถเข็นแสดงสรุปรถเข็น (หรือที่เรียกอีกอย่างหนึ่งว่ารถเข็นมินิ) เมื่อผู้ใช้เลื่อนเมาส์ไปวางไว้ เลือก **แสดงมินิรถเข็น**</span><span class="sxs-lookup"><span data-stu-id="f9fc0-161">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="f9fc0-162">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f9fc0-162">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f9fc0-163">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกหน้า ให้ทำตามขั้นตอนต่อไปนี้บนทุกเท็มเพลตหน้าที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="f9fc0-163">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f9fc0-164">ในช่อง **ส่วนหัว** ของโมดูล **หน้าเริ่มต้น** ให้เพิ่มส่วนย่อยที่เป็นส่วนท้ายที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f9fc0-164">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="f9fc0-165">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f9fc0-165">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9fc0-166">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f9fc0-166">Additional resources</span></span>

[<span data-ttu-id="f9fc0-167">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="f9fc0-167">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f9fc0-168">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="f9fc0-168">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f9fc0-169">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="f9fc0-169">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f9fc0-170">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="f9fc0-170">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f9fc0-171">โมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="f9fc0-171">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="f9fc0-172">การยอมรับคุกกี้</span><span class="sxs-lookup"><span data-stu-id="f9fc0-172">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="f9fc0-173">โมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="f9fc0-173">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="f9fc0-174">โมดูลตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="f9fc0-174">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="f9fc0-175">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-175">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]