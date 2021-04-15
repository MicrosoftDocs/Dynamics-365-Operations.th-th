---
title: โมดูลของส่วนท้าย
description: หัวข้อนี้ครอบคลุมถึงโมดูลของส่วนท้ายและวิธีการสร้าง Dynamics 365 Commerce
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d6e7b0ad4fe0723575a0ec55a9b02d110568db58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797244"
---
# <a name="footer-module"></a><span data-ttu-id="b3aef-103">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="b3aef-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3aef-104">หัวข้อนี้ครอบคลุมถึงโมดูลของส่วนท้ายและอธิบายวิธีการสร้างใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b3aef-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b3aef-105">โมดูลของส่วนท้ายเป็นคอนเทนเนอร์พิเศษที่ใช้เพื่อโฮสต์โมดูลที่ปรากฏในส่วนท้ายของเพจ</span><span class="sxs-lookup"><span data-stu-id="b3aef-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="b3aef-106">ตัวอย่างเช่น สามารถรวมลิงค์ไปยังเพจต่างๆ ทั่วทั้งไซต์ เช่น **ติดต่อเรา** และเพจ **นโยบายร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="b3aef-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="b3aef-107">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลส่วนท้ายบนหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="b3aef-107">The following image shows an example of a footer module on a site page.</span></span>

![ตัวอย่างของโมดูลส่วนท้าย](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties&quot;></a><span data-ttu-id=&quot;b3aef-109&quot;>คุณสมบัติของโมดูลของส่วนท้าย</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b3aef-109&quot;>Footer module properties</span></span> 

<span data-ttu-id=&quot;b3aef-110&quot;>เช่นเดียวกับคอนเทนเนอร์ส่วนใหญ่ โมดูลของส่วนท้ายสนับสนุนคุณสมบัติสำหรับส่วนหัวและความกว้าง</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b3aef-110&quot;>Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id=&quot;b3aef-111&quot;>นอกจากนี้ยังสนับสนุนการเพิ่มโมดูลประเภทของหลายส่วนท้าย</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b3aef-111&quot;>It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id=&quot;b3aef-112&quot;>แต่ละโมดูลประเภทของส่วนท้ายที่มีการเพิ่มจะถูกแสดงเป็นคอลัมน์ในโมดูลส่วนท้าย</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b3aef-112&quot;>Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name=&quot;modules-available-in-a-footer-module&quot;></a><span data-ttu-id=&quot;b3aef-113&quot;>โมดูลที่มีอยู่ในโมดูลส่วนท้าย</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b3aef-113&quot;>Modules available in a footer module</span></span>

<span data-ttu-id=&quot;b3aef-114&quot;>**สินค้าส่วนท้าย** โมดูลสินค้าส่วนท้ายอาจประกอบด้วยหัวข้อ รูปภาพ และลิงค์</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b3aef-114&quot;>**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id=&quot;b3aef-115&quot;>คุณสามารถใช้หัวข้ออย่างเดียวห รือรวมกันกับรูปภาพและลิงค์</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b3aef-115&quot;>The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id=&quot;b3aef-116&quot;>คุณสามารถตั้งค่าคอนฟิกทุกลิงค์ในส่วนท้าย เพื่อให้มีข้อความเพียงอย่างเดียว (ตัวอย่างเช่น &quot;ติดต่อเรา&quot; และลิงค์ &quot;ความเป็นส่วนตัว") หรือเพื่อให้มีทั้งข้อความและรูปภาพ (ตัวอย่างเช่น ลิงค์โซเชียลมีเดีย)</span><span class="sxs-lookup"><span data-stu-id="b3aef-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="b3aef-117">**กลับไปที่ด้านบนสุด** - การกลับไปที่โมดูลอันดับต้นๆ ให้ลิงค์สำหรับการนำทางด่วนไปที่ด้านบนของเพจ</span><span class="sxs-lookup"><span data-stu-id="b3aef-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="b3aef-118">ต้องใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="b3aef-118">A destination is required.</span></span> <span data-ttu-id="b3aef-119">ค่าปลายทางเริ่มต้นคือ \# ซึ่งพาผู้ใช้ไปยังด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="b3aef-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="b3aef-120">สร้างโมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="b3aef-120">Create a footer module</span></span>

1. <span data-ttu-id="b3aef-121">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="b3aef-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b3aef-122">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **คอนเทนเนอร์** ป้อนชื่อสำหรับส่วนย่อย แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b3aef-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b3aef-123">ในช่อง **คอนเทนเนอร์เริ่มต้น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="b3aef-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b3aef-124">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ประเภทของส่วนท้าย** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b3aef-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b3aef-125">ในช่อง **ประเภทส่วนท้าย** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="b3aef-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b3aef-126">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายการส่วนท้าย** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b3aef-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b3aef-127">เลือกช่อง **รายการส่วนท้าย** จากนั้นในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคอนฟิกส่วนหัว ลิงก์และข้อความลิงก์ และรูปภาพตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="b3aef-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="b3aef-128">หากต้องการเพิ่มรายการส่วนท้าย ทำซ้ำแต่ละขั้นตอนที่ 5 ถึง 7</span><span class="sxs-lookup"><span data-stu-id="b3aef-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="b3aef-129">หากต้องการเพิ่มลิงค์ "กลับไปที่ด้านบน" ไปที่ส่วนท้าย เลือกปุ่มจุดไข่ปลา (**...**) ในช่อง **ประเภทของส่วนท้าย** จากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="b3aef-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b3aef-130">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **กลับไปที่ด้านบน** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b3aef-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b3aef-131">เลือกช่อง **กลับไปที่ด้านบน** จากนั้นในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าคอนฟิกข้อความและคุณสมบัติโมดูลอื่นๆ ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b3aef-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="b3aef-132">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อเช็คอินส่วนย่อย และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="b3aef-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b3aef-133">เพื่อให้มั่นใจว่าส่วนหัวจะปรากฏบนทุกเพจ ให้ทำตามขั้นตอนต่อไปนี้บนทุกแม่แบบเพจที่สร้างขึ้นสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="b3aef-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="b3aef-134">ในช่อง **ส่วนท้าย** ของโมดูล **หน้าเริ่มต้น** ให้เพิ่มส่วนย่อยที่เป็นส่วนท้ายที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b3aef-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="b3aef-135">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="b3aef-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b3aef-136">โดยการเพิ่มส่วนย่อยลงในเท็มเพลตหน้า คุณช่วยรับประกันว่าส่วนท้ายจะแสดงบนทุกหน้า</span><span class="sxs-lookup"><span data-stu-id="b3aef-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3aef-137">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b3aef-137">Additional resources</span></span>

[<span data-ttu-id="b3aef-138">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="b3aef-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b3aef-139">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="b3aef-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b3aef-140">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3aef-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b3aef-141">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="b3aef-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b3aef-142">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="b3aef-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b3aef-143">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3aef-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b3aef-144">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="b3aef-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b3aef-145">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="b3aef-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]