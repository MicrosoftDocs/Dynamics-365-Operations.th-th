---
title: โมดูลของส่วนท้าย
description: หัวข้อนี้ครอบคลุมถึงโมดูลของส่วนท้ายและวิธีการสร้าง Dynamics 365 Commerce
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e81617979a945274500c9f4ceaa8078d8dfd79e8
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686729"
---
# <a name="footer-module"></a><span data-ttu-id="be943-103">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="be943-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="be943-104">หัวข้อนี้ครอบคลุมถึงโมดูลของส่วนท้ายและอธิบายวิธีการสร้างใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="be943-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="be943-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="be943-105">Overview</span></span>

<span data-ttu-id="be943-106">โมดูลของส่วนท้ายเป็นคอนเทนเนอร์พิเศษที่ใช้เพื่อโฮสต์โมดูลที่ปรากฏในส่วนท้ายของเพจ</span><span class="sxs-lookup"><span data-stu-id="be943-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="be943-107">ตัวอย่างเช่น สามารถรวมลิงค์ไปยังเพจต่างๆ ทั่วทั้งไซต์ เช่น **ติดต่อเรา** และเพจ **นโยบายร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="be943-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="be943-108">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลส่วนท้ายบนหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="be943-108">The following image shows an example of a footer module on a site page.</span></span>

![ตัวอย่างของโมดูลส่วนท้าย](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="be943-110">คุณสมบัติของโมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="be943-110">Footer module properties</span></span> 

<span data-ttu-id="be943-111">เช่นเดียวกับคอนเทนเนอร์ส่วนใหญ่ โมดูลของส่วนท้ายสนับสนุนคุณสมบัติสำหรับส่วนหัวและความกว้าง</span><span class="sxs-lookup"><span data-stu-id="be943-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="be943-112">นอกจากนี้ยังสนับสนุนการเพิ่มโมดูลประเภทของหลายส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="be943-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="be943-113">แต่ละโมดูลประเภทของส่วนท้ายที่มีการเพิ่มจะถูกแสดงเป็นคอลัมน์ในโมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="be943-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="be943-114">โมดูลที่มีอยู่ในโมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="be943-114">Modules available in a footer module</span></span>

<span data-ttu-id="be943-115">**สินค้าส่วนท้าย** โมดูลสินค้าส่วนท้ายอาจประกอบด้วยหัวข้อ รูปภาพ และลิงค์</span><span class="sxs-lookup"><span data-stu-id="be943-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="be943-116">คุณสามารถใช้หัวข้ออย่างเดียวห รือรวมกันกับรูปภาพและลิงค์</span><span class="sxs-lookup"><span data-stu-id="be943-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="be943-117">คุณสามารถตั้งค่าคอนฟิกทุกลิงค์ในส่วนท้าย เพื่อให้มีข้อความเพียงอย่างเดียว (ตัวอย่างเช่น "ติดต่อเรา" และลิงค์ "ความเป็นส่วนตัว") หรือเพื่อให้มีทั้งข้อความและรูปภาพ (ตัวอย่างเช่น ลิงค์โซเชียลมีเดีย)</span><span class="sxs-lookup"><span data-stu-id="be943-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="be943-118">**กลับไปที่ด้านบนสุด** - การกลับไปที่โมดูลอันดับต้นๆ ให้ลิงค์สำหรับการนำทางด่วนไปที่ด้านบนของเพจ</span><span class="sxs-lookup"><span data-stu-id="be943-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="be943-119">ต้องใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="be943-119">A destination is required.</span></span> <span data-ttu-id="be943-120">ค่าปลายทางเริ่มต้นคือ \# ซึ่งพาผู้ใช้ไปยังด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="be943-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="be943-121">สร้างโมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="be943-121">Create a footer module</span></span>

1. <span data-ttu-id="be943-122">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="be943-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="be943-123">ในกล่องโต้ตอบ **ส่วนย่อยของหน้าใหม่** ให้เลือกโมดูล **คอนเทนเนอร์** ป้อนชื่อสำหรับส่วนย่อยของหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="be943-123">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="be943-124">ในช่อง **คอนเทนเนอร์เริ่มต้น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="be943-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="be943-125">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ประเภทของส่วนท้าย** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="be943-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="be943-126">ในช่อง **ประเภทส่วนท้าย** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="be943-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="be943-127">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายการส่วนท้าย** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="be943-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="be943-128">เลือกช่อง **รายการส่วนท้าย** จากนั้นในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคอนฟิกส่วนหัว ลิงก์และข้อความลิงก์ และรูปภาพตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="be943-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="be943-129">หากต้องการเพิ่มรายการส่วนท้าย ทำซ้ำแต่ละขั้นตอนที่ 5 ถึง 7</span><span class="sxs-lookup"><span data-stu-id="be943-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="be943-130">หากต้องการเพิ่มลิงค์ "กลับไปที่ด้านบน" ไปที่ส่วนท้าย เลือกปุ่มจุดไข่ปลา (**...**) ในช่อง **ประเภทของส่วนท้าย** จากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="be943-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="be943-131">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **กลับไปที่ด้านบน** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="be943-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="be943-132">เลือกช่อง **กลับไปที่ด้านบน** จากนั้นในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคอนฟิกข้อความและคุณสมบัติโมดูลอื่นๆ ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be943-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="be943-133">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อเช็คอินส่วนย่อย และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="be943-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="be943-134">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกเพจ ให้ทำตามขั้นตอนต่อไปนี้บนทุกแม่แบบเพจที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="be943-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="be943-135">ในช่อง **ส่วนท้าย** ของโมดูล **หน้าเริ่มต้น** ให้เพิ่มส่วนย่อยที่เป็นส่วนท้ายที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="be943-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="be943-136">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="be943-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="be943-137">โดยการเพิ่มส่วนของเพจลงในแม่แบบเพจ คุณช่วยรับประกันว่าส่วนท้ายจะแสดงบนทุกเพจ</span><span class="sxs-lookup"><span data-stu-id="be943-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be943-138">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="be943-138">Additional resources</span></span>

[<span data-ttu-id="be943-139">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="be943-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="be943-140">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="be943-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="be943-141">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="be943-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="be943-142">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="be943-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="be943-143">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="be943-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="be943-144">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="be943-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="be943-145">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="be943-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="be943-146">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="be943-146">Footer module</span></span>](author-footer-module.md)
