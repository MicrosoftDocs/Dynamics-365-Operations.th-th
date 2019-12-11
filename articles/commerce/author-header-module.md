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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697286"
---
# <a name="header-module"></a><span data-ttu-id="22757-103">โมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="22757-103">Header module</span></span>

<span data-ttu-id="22757-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="22757-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="22757-105">หัวข้อนี้ครอบคลุมถึงโมดูลหัวข้อและอธิบายวิธีการสร้างใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="22757-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="22757-106">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="22757-106">Overview</span></span>

<span data-ttu-id="22757-107">โมดูลส่วนหัวคือคอนเทนเนอร์พิเศษที่ใช้เพื่อโฮสต์โมดูลทั้งหมดที่จะแสดงในส่วนหัวของเพจ</span><span class="sxs-lookup"><span data-stu-id="22757-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="22757-108">ตัวอย่างเช่น คุณสามารถรวมโลโก้ไซต์ของคุณ ลิงค์ไปยังลำดับชั้นการนำทาง ลิงค์ไปยังเพจอื่นๆ บนไซต์และแถบค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="22757-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="22757-109">โมดูลส่วนหัวจะถูกปรับให้เหมาะสมโดยอัตโนมัติสำหรับอุปกรณ์ที่ไซต์กำลังดู (นั่นคือ อุปกรณ์เดสก์ทอป หรืออุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="22757-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="22757-110">ตัวอย่างเช่น บนอุปกรณ์เคลื่อนที่ แถบนำทางจะถูกยุบลงในปุ่ม **เมนู** (ซึ่งบางครั้งเรียกว่า *เมนู hamburger*)</span><span class="sxs-lookup"><span data-stu-id="22757-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="22757-111">คุณสมบัติของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="22757-111">Properties of a header</span></span>

<span data-ttu-id="22757-112">เช่นเดียวกับคอนเทนเนอร์ทั่วไป โมดูลส่วนหัวสนับสนุนคุณสมบัติ **ส่วนหัว** และ **ความกว้าง**</span><span class="sxs-lookup"><span data-stu-id="22757-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="22757-113">โมดูลหัวข้อมีหลายช่อง</span><span class="sxs-lookup"><span data-stu-id="22757-113">A header module has multiple slots.</span></span> <span data-ttu-id="22757-114">ตัวอย่างเช่น มีช่องสำหรับข้อความที่ให้ข้อมูล เมนูนำทาง โลโก้ แถบค้นหา ไอคอนรถเข็น ไอคอนรายการสิ่งที่ต้องการ และข้อมูลบัญชี</span><span class="sxs-lookup"><span data-stu-id="22757-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="22757-115">แต่ละช่องสนับสนุนชุดของโมดูลเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="22757-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="22757-116">โมดูลที่มีอยู่ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="22757-116">Modules that are available in a header module</span></span>

<span data-ttu-id="22757-117">โมดูลต่อไปนี้สามารถใช้ได้ในโมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="22757-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="22757-118">**เมนูนำทาง** – เมนูนำทางแสดงถึงลำดับชั้นการนำทางช่องทาง และลิงค์การนำทางแบบคงที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="22757-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="22757-119">ลำดับชั้นการนำทางของช่องทางสามารถตั้งค่าคอนฟิกใน Dynamics 365 Retail ได้</span><span class="sxs-lookup"><span data-stu-id="22757-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="22757-120">สินค้าที่จัดโครงแบบจะปรากฏเป็นการนำทางส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="22757-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="22757-121">นอกจากนี้ คุณยังสามารถตั้งค่าคอนฟิกลิงค์การนำทางแบบคงที่ และลิงค์ที่สัมพันธ์กับเพจอื่นๆ บนไซต์อีคอมเมิร์ซสามารถระบุได้</span><span class="sxs-lookup"><span data-stu-id="22757-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="22757-122">ส่วนหัวอาจสอดคล้องกับด้านซ้าย ขวา หรือกึ่งกลาง</span><span class="sxs-lookup"><span data-stu-id="22757-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="22757-123">**ไอคอนรถเข็น** – ไอคอนรถเข็นเป็นไอคอนพิเศษที่แสดงถึงรถเข็น</span><span class="sxs-lookup"><span data-stu-id="22757-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="22757-124">แสดงอยู่ในส่วนหัว และระบุจำนวนของสินค้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="22757-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="22757-125">ลิงค์ไปยังเพจรถเข็นควรมีไอคอนรถเข็น เพื่อให้ลูกค้าสามารถเปลี่ยนเส้นทางไปยังเพจรถเข็นเมื่อมีการโต้ตอบกับไอคอน</span><span class="sxs-lookup"><span data-stu-id="22757-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="22757-126">**ไอคอนรายการสิ่งที่ต้องการ** – ไอคอนรายการสิ่งที่ต้องการจะแสดงอยู่ในส่วนหัว และระบุจำนวนของสินค้าที่มีการเพิ่มลงในรายการสิ่งที่ต้องการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="22757-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="22757-127">ลิงค์ไปยังเพจรายการสิ่งที่ต้องการควรมีไอคอนนี้ เพื่อให้ลูกค้าสามารถเปลี่ยนเส้นทางไปยังเพจรายการสิ่งที่ต้องการเมื่อมีการโต้ตอบกับไอคอน</span><span class="sxs-lookup"><span data-stu-id="22757-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="22757-128">**โมดูลการลงชื่อเข้าใช้** – ระบบจะแสดงโมดูลการลงชื่อเข้าใช้ในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="22757-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="22757-129">ให้ลูกค้าลงชื่อเข้าใช้บัญชีของตน หรือลงทะเบียนสำหรับบัญชี</span><span class="sxs-lookup"><span data-stu-id="22757-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="22757-130">ถ้าลูกค้าลงชื่อเข้าใช้แล้ว คุณสามารถตั้งค่าคอนฟิกโมดูลเพื่อแสดงลิงค์ไปยังเพจบัญชี เพจประวัติการสั่งซื้อ หรือเพจอื่น</span><span class="sxs-lookup"><span data-stu-id="22757-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="22757-131">**โมดูลโลโก้** – โมดูลนี้แสดงโลโก้ซึ่งแสดงถึงผู้ค้าปลีกและแบรนด์</span><span class="sxs-lookup"><span data-stu-id="22757-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="22757-132">เป็นรูปภาพที่มีลิงค์</span><span class="sxs-lookup"><span data-stu-id="22757-132">It's an image that has a link.</span></span> <span data-ttu-id="22757-133">โดยทั่วไปลิงค์จะได้รับการตั้งค่าคอนฟิก เพื่อให้มีการเปลี่ยนเส้นทางไปยังโฮมเพจ ดังนั้นลูกค้าสามารถกลับไปยังโฮมเพจจากเพจใดก็ได้บนไซต์อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="22757-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="22757-134">**การแจ้งเตือน** – ข้อความแจ้งเตือนจะปรากฏขึ้นในส่วนหัว และใช้เพื่อแสดงข้อความแบบอินไลน์ที่ใช้กับทุกเพจบนไซต์</span><span class="sxs-lookup"><span data-stu-id="22757-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="22757-135">ตัวอย่างเช่น ข้อความแจ้งเตือนอาจแสดงข้อความ เช่น "ยอดขายประจำปีสิ้นสุดใน 2วัน"</span><span class="sxs-lookup"><span data-stu-id="22757-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="22757-136">**แถบการค้นหา** - แถบการค้นหาจะช่วยให้ผู้ใช้ป้อนคำที่ใช้ค้นหา เพื่อให้ผู้ใช้สามารถค้นหาผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="22757-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="22757-137">ต้องมีการตั้งค่าคอนฟิกโมดูลกับ URL ของเพจผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="22757-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="22757-138">คุณสามารถตั้งค่าคอนฟิกพารามิเตอร์สตริงการสอบถามได้ (ค่าเริ่มต้นคือ **"q"**)</span><span class="sxs-lookup"><span data-stu-id="22757-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="22757-139">แถบการค้นหามีช่อง autosuggest ซึ่งควรมีการเพิ่มโมดูล autosuggest</span><span class="sxs-lookup"><span data-stu-id="22757-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="22757-140">**Autosuggest** –โมดูล Autosuggest แสดงผลลัพธ์ที่แนะนำโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="22757-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="22757-141">ผลลัพธ์เหล่านี้อาจเป็นคำสำคัญ ผลิตภัณฑ์ หรือประเภทที่พบคำที่ใช้ค้นหา</span><span class="sxs-lookup"><span data-stu-id="22757-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="22757-142">สร้างโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="22757-142">Create a header module</span></span>

<span data-ttu-id="22757-143">เมื่อต้องการสร้างโมดูลส่วนหัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="22757-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="22757-144">สร้างส่วนของเพจซึ่งรวมถึงโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="22757-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="22757-145">เพิ่มโมดูลในช่องในโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="22757-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="22757-146">อัพเดตการตั้งค่าสำหรับแต่ละโมดูล</span><span class="sxs-lookup"><span data-stu-id="22757-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="22757-147">บันทึกส่วนของเพจ</span><span class="sxs-lookup"><span data-stu-id="22757-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="22757-148">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="22757-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="22757-149">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกเพจ ให้ทำตามขั้นตอนต่อไปนี้บนทุกแม่แบบเพจที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="22757-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="22757-150">บนเพจเริ่มต้น ให้เพิ่มส่วนของเพจที่มีโมดูลส่วนหัวไปยังส่วนหัวในช่องหลัก</span><span class="sxs-lookup"><span data-stu-id="22757-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="22757-151">บันทึกแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="22757-151">Save the template.</span></span> 
1. <span data-ttu-id="22757-152">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="22757-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22757-153">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="22757-153">Additional resources</span></span>

[<span data-ttu-id="22757-154">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="22757-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="22757-155">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="22757-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="22757-156">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="22757-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="22757-157">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="22757-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="22757-158">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="22757-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="22757-159">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="22757-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="22757-160">โมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="22757-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="22757-161">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="22757-161">Footer module</span></span>](author-footer-module.md)
