---
title: โมดูลหัวข้อ
description: หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างใน Microsoft Dynamics 365 Commerce
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885489"
---
# <a name="header-module"></a><span data-ttu-id="69c6e-103">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="69c6e-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="69c6e-104">หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="69c6e-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="69c6e-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="69c6e-105">Overview</span></span>

<span data-ttu-id="69c6e-106">โมดูลส่วนหัวคือคอนเทนเนอร์พิเศษที่ใช้เพื่อโฮสต์โมดูลทั้งหมดที่จะแสดงในส่วนหัวของเพจ</span><span class="sxs-lookup"><span data-stu-id="69c6e-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="69c6e-107">ตัวอย่างเช่น คุณสามารถรวมโลโก้ไซต์ของคุณ ลิงค์ไปยังลำดับชั้นการนำทาง ลิงค์ไปยังเพจอื่นๆ บนไซต์และแถบค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="69c6e-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="69c6e-108">โมดูลส่วนหัวจะถูกปรับให้เหมาะสมโดยอัตโนมัติสำหรับอุปกรณ์ที่ไซต์กำลังดู (นั่นคือ อุปกรณ์เดสก์ทอป หรืออุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="69c6e-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="69c6e-109">ตัวอย่างเช่น บนอุปกรณ์เคลื่อนที่ แถบนำทางจะถูกยุบลงในปุ่ม **เมนู** (ซึ่งบางครั้งเรียกว่า *เมนู hamburger*)</span><span class="sxs-lookup"><span data-stu-id="69c6e-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="69c6e-110">คุณสมบัติของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="69c6e-110">Properties of a header</span></span>

<span data-ttu-id="69c6e-111">เช่นเดียวกับคอนเทนเนอร์ทั่วไป โมดูลส่วนหัวสนับสนุนคุณสมบัติ **ส่วนหัว** และ **ความกว้าง**</span><span class="sxs-lookup"><span data-stu-id="69c6e-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="69c6e-112">โมดูลหัวข้อมีหลายช่อง</span><span class="sxs-lookup"><span data-stu-id="69c6e-112">A header module has multiple slots.</span></span> <span data-ttu-id="69c6e-113">ตัวอย่างเช่น มีช่องสำหรับข้อความที่ให้ข้อมูล เมนูนำทาง โลโก้ แถบค้นหา ไอคอนรถเข็น ไอคอนรายการสิ่งที่ต้องการ และข้อมูลบัญชี</span><span class="sxs-lookup"><span data-stu-id="69c6e-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="69c6e-114">แต่ละช่องสนับสนุนชุดของโมดูลเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="69c6e-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="69c6e-115">โมดูลที่มีอยู่ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="69c6e-115">Modules that are available in a header module</span></span>

<span data-ttu-id="69c6e-116">โมดูลต่อไปนี้สามารถใช้ได้ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="69c6e-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="69c6e-117">**เมนูนำทาง** – เมนูนำทางแสดงถึงลำดับชั้นการนำทางช่องทาง และลิงค์การนำทางแบบคงที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="69c6e-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="69c6e-118">ลำดับชั้นการนำทางของช่องทางสามารถตั้งค่าคอนฟิกใน Dynamics 365 Retail ได้</span><span class="sxs-lookup"><span data-stu-id="69c6e-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="69c6e-119">สินค้าที่จัดโครงแบบจะปรากฏเป็นการนำทางส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="69c6e-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="69c6e-120">นอกจากนี้ คุณยังสามารถตั้งค่าคอนฟิกลิงค์การนำทางแบบคงที่ และลิงค์ที่สัมพันธ์กับเพจอื่นๆ บนไซต์อีคอมเมิร์ซสามารถระบุได้</span><span class="sxs-lookup"><span data-stu-id="69c6e-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="69c6e-121">ส่วนหัวอาจสอดคล้องกับด้านซ้าย ขวา หรือกึ่งกลาง</span><span class="sxs-lookup"><span data-stu-id="69c6e-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="69c6e-122">**ไอคอนรถเข็น** – ไอคอนรถเข็นเป็นไอคอนพิเศษที่แสดงถึงรถเข็น</span><span class="sxs-lookup"><span data-stu-id="69c6e-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="69c6e-123">แสดงอยู่ในส่วนหัว และระบุจำนวนของสินค้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="69c6e-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="69c6e-124">ลิงค์ไปยังเพจรถเข็นควรมีไอคอนรถเข็น เพื่อให้ลูกค้าสามารถเปลี่ยนเส้นทางไปยังเพจรถเข็นเมื่อมีการโต้ตอบกับไอคอน</span><span class="sxs-lookup"><span data-stu-id="69c6e-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="69c6e-125">**ไอคอนรายการสิ่งที่ต้องการ** – ไอคอนรายการสิ่งที่ต้องการจะแสดงอยู่ในส่วนหัว และระบุจำนวนของสินค้าที่มีการเพิ่มลงในรายการสิ่งที่ต้องการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="69c6e-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="69c6e-126">ลิงค์ไปยังเพจรายการสิ่งที่ต้องการควรมีไอคอนนี้ เพื่อให้ลูกค้าสามารถเปลี่ยนเส้นทางไปยังเพจรายการสิ่งที่ต้องการเมื่อมีการโต้ตอบกับไอคอน</span><span class="sxs-lookup"><span data-stu-id="69c6e-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="69c6e-127">**โมดูลการลงชื่อเข้าใช้** – ระบบจะแสดงโมดูลการลงชื่อเข้าใช้ในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="69c6e-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="69c6e-128">ให้ลูกค้าลงชื่อเข้าใช้บัญชีของตน หรือลงทะเบียนสำหรับบัญชี</span><span class="sxs-lookup"><span data-stu-id="69c6e-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="69c6e-129">ถ้าลูกค้าลงชื่อเข้าใช้แล้ว คุณสามารถตั้งค่าคอนฟิกโมดูลเพื่อแสดงลิงค์ไปยังเพจบัญชี เพจประวัติการสั่งซื้อ หรือเพจอื่น</span><span class="sxs-lookup"><span data-stu-id="69c6e-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="69c6e-130">**โมดูลโลโก้** – โมดูลนี้แสดงโลโก้ซึ่งแสดงถึงผู้ค้าปลีกและแบรนด์</span><span class="sxs-lookup"><span data-stu-id="69c6e-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="69c6e-131">เป็นรูปภาพที่มีลิงค์</span><span class="sxs-lookup"><span data-stu-id="69c6e-131">It's an image that has a link.</span></span> <span data-ttu-id="69c6e-132">โดยทั่วไปลิงค์จะได้รับการตั้งค่าคอนฟิก เพื่อให้มีการเปลี่ยนเส้นทางไปยังโฮมเพจ ดังนั้นลูกค้าสามารถกลับไปยังโฮมเพจจากเพจใดก็ได้บนไซต์อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="69c6e-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="69c6e-133">**การแจ้งเตือน** – ข้อความแจ้งเตือนจะปรากฏขึ้นในส่วนหัว และใช้เพื่อแสดงข้อความแบบอินไลน์ที่ใช้กับทุกเพจบนไซต์</span><span class="sxs-lookup"><span data-stu-id="69c6e-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="69c6e-134">ตัวอย่างเช่น ข้อความแจ้งเตือนอาจแสดงข้อความ เช่น "ยอดขายประจำปีสิ้นสุดใน 2วัน"</span><span class="sxs-lookup"><span data-stu-id="69c6e-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="69c6e-135">**แถบการค้นหา** - แถบการค้นหาจะช่วยให้ผู้ใช้ป้อนคำที่ใช้ค้นหา เพื่อให้ผู้ใช้สามารถค้นหาผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="69c6e-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="69c6e-136">ต้องมีการตั้งค่าคอนฟิกโมดูลกับ URL ของเพจผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="69c6e-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="69c6e-137">คุณสามารถตั้งค่าคอนฟิกพารามิเตอร์สตริงการสอบถามได้ (ค่าเริ่มต้นคือ **"q"**)</span><span class="sxs-lookup"><span data-stu-id="69c6e-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="69c6e-138">แถบการค้นหามีช่อง autosuggest ซึ่งควรมีการเพิ่มโมดูล autosuggest</span><span class="sxs-lookup"><span data-stu-id="69c6e-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="69c6e-139">**Autosuggest** –โมดูล Autosuggest แสดงผลลัพธ์ที่แนะนำโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="69c6e-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="69c6e-140">ผลลัพธ์เหล่านี้อาจเป็นคำสำคัญ ผลิตภัณฑ์ หรือประเภทที่พบคำที่ใช้ค้นหา</span><span class="sxs-lookup"><span data-stu-id="69c6e-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="69c6e-141">สร้างโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="69c6e-141">Create a header module</span></span>

<span data-ttu-id="69c6e-142">เมื่อต้องการสร้างโมดูลส่วนหัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="69c6e-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="69c6e-143">สร้างส่วนของเพจซึ่งรวมถึงโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="69c6e-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="69c6e-144">เพิ่มโมดูลในช่องในโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="69c6e-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="69c6e-145">อัพเดตการตั้งค่าสำหรับแต่ละโมดูล</span><span class="sxs-lookup"><span data-stu-id="69c6e-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="69c6e-146">บันทึกส่วนของเพจ</span><span class="sxs-lookup"><span data-stu-id="69c6e-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="69c6e-147">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="69c6e-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="69c6e-148">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกเพจ ให้ทำตามขั้นตอนต่อไปนี้บนทุกแม่แบบเพจที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="69c6e-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="69c6e-149">บนเพจเริ่มต้น ให้เพิ่มส่วนของเพจที่มีโมดูลส่วนหัวไปยังส่วนหัวในช่องหลัก</span><span class="sxs-lookup"><span data-stu-id="69c6e-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="69c6e-150">บันทึกแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="69c6e-150">Save the template.</span></span> 
1. <span data-ttu-id="69c6e-151">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="69c6e-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69c6e-152">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="69c6e-152">Additional resources</span></span>

[<span data-ttu-id="69c6e-153">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69c6e-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="69c6e-154">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="69c6e-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="69c6e-155">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="69c6e-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="69c6e-156">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="69c6e-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="69c6e-157">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="69c6e-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="69c6e-158">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="69c6e-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="69c6e-159">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="69c6e-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="69c6e-160">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="69c6e-160">Footer module</span></span>](author-footer-module.md)
