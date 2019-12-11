---
title: โมดูลของส่วนท้าย
description: หัวข้อนี้ครอบคลุมถึงโมดูลของส่วนท้ายและวิธีการสร้าง Dynamics 365 Commerce
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697324"
---
# <a name="footer-module"></a><span data-ttu-id="26012-103">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="26012-103">Footer module</span></span>  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="26012-104">หัวข้อนี้ครอบคลุมถึงโมดูลของส่วนท้ายและอธิบายวิธีการสร้างใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="26012-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="26012-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="26012-105">Overview</span></span>

<span data-ttu-id="26012-106">โมดูลของส่วนท้ายเป็นคอนเทนเนอร์พิเศษที่ใช้เพื่อโฮสต์โมดูลที่ปรากฏในส่วนท้ายของเพจ</span><span class="sxs-lookup"><span data-stu-id="26012-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="26012-107">ตัวอย่างเช่น สามารถรวมลิงค์ไปยังเพจต่างๆ ทั่วทั้งไซต์ เช่น **ติดต่อเรา** และเพจ **นโยบายร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="26012-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="26012-108">คุณสมบัติของโมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="26012-108">Footer module properties</span></span> 

<span data-ttu-id="26012-109">เช่นเดียวกับคอนเทนเนอร์ส่วนใหญ่ โมดูลของส่วนท้ายสนับสนุนคุณสมบัติสำหรับหัวข้อและความกว้าง</span><span class="sxs-lookup"><span data-stu-id="26012-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="26012-110">นอกจากนี้ยังสนับสนุนการเพิ่มโมดูลประเภทของหลายส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="26012-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="26012-111">แต่ละโมดูลประเภทของส่วนท้ายที่มีการเพิ่มจะถูกแสดงเป็นคอลัมน์ในโมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="26012-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="26012-112">โมดูลที่มีอยู่ในโมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="26012-112">Modules available in a footer module</span></span>

<span data-ttu-id="26012-113">**สินค้าส่วนท้าย** โมดูลสินค้าส่วนท้ายอาจประกอบด้วยหัวข้อ รูปภาพ และลิงค์</span><span class="sxs-lookup"><span data-stu-id="26012-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="26012-114">คุณสามารถใช้หัวข้ออย่างเดียวห รือรวมกันกับรูปภาพและลิงค์</span><span class="sxs-lookup"><span data-stu-id="26012-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="26012-115">คุณสามารถตั้งค่าคอนฟิกทุกลิงค์ในส่วนท้าย เพื่อให้มีข้อความเพียงอย่างเดียว (ตัวอย่างเช่น "ติดต่อเรา" และลิงค์ "ความเป็นส่วนตัว") หรือเพื่อให้มีทั้งข้อความและรูปภาพ (ตัวอย่างเช่น ลิงค์โซเชียลมีเดีย)</span><span class="sxs-lookup"><span data-stu-id="26012-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="26012-116">**กลับไปที่ด้านบนสุด** - การกลับไปที่โมดูลอันดับต้นๆ ให้ลิงค์สำหรับการนำทางด่วนไปที่ด้านบนของเพจ</span><span class="sxs-lookup"><span data-stu-id="26012-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="26012-117">ต้องใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="26012-117">A destination is required.</span></span> <span data-ttu-id="26012-118">ค่าปลายทางเริ่มต้นคือ # ซึ่งพาผู้ใช้ไปยังด้านบนของเพจ</span><span class="sxs-lookup"><span data-stu-id="26012-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="26012-119">สร้างโมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="26012-119">Author a footer module</span></span>

1. <span data-ttu-id="26012-120">ในบานหน้าต่างนำทาง ให้เลือก **ส่วน** แล้วเลือก **ส่วนของเพจใหม่**</span><span class="sxs-lookup"><span data-stu-id="26012-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="26012-121">ในกล่องโต้ตอบ **ส่วนของเพจใหม่** ให้เลือกโมดูลส่วนท้าย ป้อนชื่อสำหรับส่วนของเพจ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="26012-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="26012-122">ในแผนภูมิเค้าร่างทางด้านซ้าย เลือกปุ่มจุดไข่ปลา (**...**) สำหรับโมดูลส่วนท้าย จากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="26012-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="26012-123">ในกล่องโต้ตอบ  **เพิ่มโมดูล** ให้เลือกโมดูลประเภทของส่วนท้าย แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="26012-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="26012-124">ในแผนภูมิเค้าร่าง เลือกปุ่มจุดไข่ปลาสำหรับโมดูลประเภทของส่วนท้าย จากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="26012-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="26012-125">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูลสินค้าของส่วนท้าย แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="26012-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="26012-126">ในแผนภูมิเค้าร่าง ให้เลือกโมดูลสินค้าของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="26012-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="26012-127">จากนั้น ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคอนฟิกหัวข้อ ลิงค์ และลิงค์ข้อความ และรูปภาพตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="26012-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="26012-128">หากต้องการเพิ่มสินค้าของส่วนท้าย ทำซ้ำขั้นตอนที่ 5 ถึง 7</span><span class="sxs-lookup"><span data-stu-id="26012-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="26012-129">หากต้องการเพิ่มลิงค์ "กลับไปที่ด้านบน" ไปที่ส่วนท้าย เลือกปุ่มจุดไข่ปลาสำหรับโมดูลประเภทของส่วนท้าย จากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="26012-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="26012-130">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูลกลับไปที่ด้านบน แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="26012-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="26012-131">ในแผนภูมิเค้าร่าง ให้เลือกโมดูลกลับไปที่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="26012-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="26012-132">จากนั้น ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคอนฟิกโมดูลกลับไปที่ด้านบนตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="26012-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="26012-133">บันทึกส่วนที่เป็นเพจ เช็คอิน และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="26012-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="26012-134">บนทุกๆ แม่แบบเพจที่สร้างขึ้นสำหรับไซต์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="26012-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="26012-135">ในช่อง **หลัก** ของเพจเริ่มต้น ในโมดูลส่วนท้าย ให้เพิ่มส่วนที่เป็นส่วนท้ายที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="26012-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="26012-136">บันทึกเท็มเพลต เช็คอิน และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="26012-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="26012-137">โดยการเพิ่มส่วนของเพจลงในแม่แบบเพจ คุณช่วยรับประกันว่าส่วนท้ายจะแสดงบนทุกเพจ</span><span class="sxs-lookup"><span data-stu-id="26012-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26012-138">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="26012-138">Additional resources</span></span>

[<span data-ttu-id="26012-139">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="26012-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="26012-140">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="26012-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="26012-141">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="26012-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="26012-142">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="26012-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="26012-143">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="26012-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="26012-144">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="26012-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="26012-145">โมดูลหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="26012-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="26012-146">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="26012-146">Footer module</span></span>](author-footer-module.md)
