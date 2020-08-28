---
title: โมดูลหัวข้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686633"
---
# <a name="header-module"></a><span data-ttu-id="06e3f-103">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="06e3f-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06e3f-104">หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างส่วนหัวของหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="06e3f-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="06e3f-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="06e3f-105">Overview</span></span>

<span data-ttu-id="06e3f-106">ใน Dynamics 365 Commerce ส่วนหัวของหน้าประกอบด้วยหลายโมดูล เช่น ส่วนหัว เมนูนำทาง การค้นหา แบนเนอร์โปรโมชัน และโมดูลการยินยอมเก็บคุกกี้</span><span class="sxs-lookup"><span data-stu-id="06e3f-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="06e3f-107">โมดูลของส่วนหัวรวมถึงโลโก้ของไซต์ ลิงก์ไปยังลำดับชั้นการนำทาง ลิงก์ไปยังหน้าอื่น ๆ บนไซต์ สัญลักษณ์รถเข็น สัญลักษณ์สิ่งที่ต้องการ ตัวเลือกการลงชื่อเข้าใช้ และแถบค้นหา</span><span class="sxs-lookup"><span data-stu-id="06e3f-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="06e3f-108">โมดูลส่วนหัวจะถูกปรับให้เหมาะสมโดยอัตโนมัติสำหรับอุปกรณ์ที่ไซต์กำลังดู (อธิบายอีกอย่างคือ อุปกรณ์เดสก์ทอป หรืออุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="06e3f-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="06e3f-109">ตัวอย่างเช่น บนอุปกรณ์เคลื่อนที่ แถบนำทางจะถูกยุบลงในปุ่ม **เมนู** (ซึ่งบางครั้งเรียกว่า *เมนู hamburger*)</span><span class="sxs-lookup"><span data-stu-id="06e3f-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="06e3f-110">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลส่วนหัวบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="06e3f-110">The following image shows an example of a header module on a home page.</span></span>

![ตัวอย่างของโมดูลส่วนหัว](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="06e3f-112">คุณสมบัติของโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="06e3f-112">Properties of a header module</span></span>

<span data-ttu-id="06e3f-113">โมดูลส่วนหัวสนับสนุนคุณสมบัติ **รูปโลโก้** **ลิงก์ของโลโก้** และ **ลิงก์บัญชีของฉัน**</span><span class="sxs-lookup"><span data-stu-id="06e3f-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="06e3f-114">คุณสมบัติ **รูปโลโก้** และ **ลิงค์โลโก้** ใช้เพื่อกำหนดโลโก้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="06e3f-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="06e3f-115">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เพิ่มโลโก้](add-logo.md)</span><span class="sxs-lookup"><span data-stu-id="06e3f-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="06e3f-116">คุณสมบัติ **ลิงก์บัญชีของฉัน** สามารถใช้ในการกำหนดหน้าบัญชีที่เจ้าของไซต์ต้องการแสดงลิงก์ด่วนในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="06e3f-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="06e3f-117">โมดูลที่มีอยู่ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="06e3f-117">Modules that are available in a header module</span></span>

<span data-ttu-id="06e3f-118">โมดูลต่อไปนี้สามารถใช้ได้ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="06e3f-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="06e3f-119">**เมนูนำทาง** – เมนูนำทางแสดงถึงลำดับชั้นการนำทางช่องทาง และลิงค์การนำทางแบบคงที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="06e3f-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="06e3f-120">ลำดับชั้นการนำทางของช่องทางสามารถตั้งค่าคอนฟิกใน Dynamics 365 Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="06e3f-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="06e3f-121">เมนูนำทางมีคุณสมบัติ **ต้นทางการนำทาง** ที่ใช้เพื่อระบุรายการเมนูการนำทางของ Retail Server และรายการเมนูแบบคงที่เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="06e3f-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="06e3f-122">ถ้ามีการระบุรายการเมนูแบบคงที่เป็นแหล่งที่มา จะสามารถระบุลิงก์ที่สัมพันธ์กับหน้าอื่น ๆ บนไซต์ได้</span><span class="sxs-lookup"><span data-stu-id="06e3f-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="06e3f-123">สินค้าที่จัดโครงแบบจะปรากฏเป็นการนำทางส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="06e3f-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="06e3f-124">**การค้นหา** - โมดูลการค้นหาจะช่วยให้ผู้ใช้ป้อนคำที่ใช้ค้นหา เพื่อค้นหาผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="06e3f-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="06e3f-125">URL เริ่มต้นของหน้าการค้นหา และต้องระบุพารามิเตอร์การสอบถามที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="06e3f-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="06e3f-126">โมดูลการค้นหาจะมีคุณสมบัติซึ่งช่วยให้คุณสามารถระงับปุ่มค้นหา หรือป้ายชื่อตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="06e3f-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="06e3f-127">โมดูลที่ใช้ในการค้นหายังสนับสนุนตัวเลือกการแนะนำอัตโนมัติ เช่น ผลิตภัณฑ์ คำสำคัญ และผลการค้นหาของประเภท</span><span class="sxs-lookup"><span data-stu-id="06e3f-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="06e3f-128">**ไอคอนรถเข็น** - โมดูลไอคอนรถเข็นแสดงถึงไอคอนรถเข็นซึ่งแสดงจำนวนของสินค้าในรถเข็นในเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="06e3f-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="06e3f-129">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลไอคอนรถเข็น](cart-icon-module.md)</span><span class="sxs-lookup"><span data-stu-id="06e3f-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="06e3f-130">สร้างโมดูลส่วนหัวของหน้า</span><span class="sxs-lookup"><span data-stu-id="06e3f-130">Create a header module for a page</span></span>

<span data-ttu-id="06e3f-131">เมื่อต้องการสร้างโมดูลส่วนหัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="06e3f-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="06e3f-132">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="06e3f-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="06e3f-133">ในกล่องโต้ตอบ **ส่วนย่อยของหน้าใหม่** ให้เลือกโมดูล **คอนเทนเนอร์** ป้อนชื่อสำหรับส่วนย่อยของหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="06e3f-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="06e3f-134">เลือก **คอนเทนเนอร์เริ่มต้น** จากนั้นในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคุณสมบัติของ **ความกว้าง** เป็น **เติมคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="06e3f-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="06e3f-135">ในช่อง **คอนเทนเนอร์เริ่มต้น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="06e3f-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06e3f-136">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **แบนเนอร์โปรโมชั่น** และ **การยินยอมใช้คุกกี้** จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="06e3f-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="06e3f-137">ในช่อง **คอนเทนเนอร์เริ่มต้น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="06e3f-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06e3f-138">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="06e3f-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="06e3f-139">เลือกช่อง **คอนเทนเนอร์** จากนั้นในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคุณสมบัติของ **ความกว้าง** เป็น **เติมคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="06e3f-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="06e3f-140">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="06e3f-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06e3f-141">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ส่วนหัว** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="06e3f-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="06e3f-142">ในช่อง **เมนูการนำทาง** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="06e3f-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06e3f-143">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **เมนูการนำทาง** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="06e3f-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="06e3f-144">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูการนำทาง ให้ตั้งค่าคอนฟิกคุณสมบัติตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="06e3f-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="06e3f-145">ในช่อง **ค้นหา** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="06e3f-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06e3f-146">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ค้นหา** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="06e3f-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="06e3f-147">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลค้นหา ให้ตั้งค่าคอนฟิกคุณสมบัติตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="06e3f-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="06e3f-148">ในช่อง **ไอคอนรถเข็น** ของโมดูลส่วนหัว ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="06e3f-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="06e3f-149">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ไอคอนรถเข็น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="06e3f-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="06e3f-150">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลเมนูไอคอนรถเข็น ให้ตั้งค่าคอนฟิกคุณสมบัติตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="06e3f-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="06e3f-151">ถ้าคุณต้องการให้ไอคอนรถเข็นแสดงสรุปรถเข็น (หรือที่เรียกอีกอย่างหนึ่งว่ารถเข็นมินิ) เมื่อผู้ใช้เลื่อนเมาส์ไปวางไว้ เลือก **แสดงมินิรถเข็น**</span><span class="sxs-lookup"><span data-stu-id="06e3f-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="06e3f-152">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="06e3f-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="06e3f-153">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกเพจ ให้ทำตามขั้นตอนต่อไปนี้บนทุกแม่แบบเพจที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="06e3f-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="06e3f-154">ในช่อง **ส่วนหัว** ของโมดูล **หน้าเริ่มต้น** ให้เพิ่มส่วนย่อยที่เป็นส่วนท้ายที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="06e3f-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="06e3f-155">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="06e3f-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06e3f-156">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="06e3f-156">Additional resources</span></span>

[<span data-ttu-id="06e3f-157">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06e3f-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="06e3f-158">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="06e3f-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="06e3f-159">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="06e3f-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="06e3f-160">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="06e3f-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="06e3f-161">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="06e3f-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="06e3f-162">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="06e3f-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="06e3f-163">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="06e3f-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="06e3f-164">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="06e3f-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="06e3f-165">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="06e3f-165">Footer module</span></span>](author-footer-module.md)
