---
title: โมดูลรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025447"
---
# <a name="cart-module"></a><span data-ttu-id="56506-103">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="56506-104">หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="56506-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="56506-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="56506-105">Overview</span></span>

<span data-ttu-id="56506-106">โมดูลรถเข็นใช้เพื่อแสดงสินค้าที่มีการเพิ่มลงในรถเข็น ก่อนที่จะดำเนินการชำระเงินให้แก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="56506-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="56506-107">ตัวอย่างเช่น จะรวมสินค้าทั้งหมดที่มีการเพิ่มลงในรถเข็น และสรุปใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="56506-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="56506-108">นอกจากนี้ยังช่วยให้ลูกค้าสามารถใช้หรือลบรหัสโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="56506-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="56506-109">โมดูลรถเข็นสนับสนุนการชำระเงินของผู้ที่ลงชื่อเข้าใช้ และการชำระเงินของผู้เยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="56506-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="56506-110">นอกจากนี้ยังสนับสนุนลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="56506-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="56506-111">คุณสามารถตั้งค่าคอนฟิกเส้นทางสำหรับลิงก์นี้ได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย \> เส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="56506-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="56506-112">โมดูลรถเข็นแสดงข้อมูลตามรหัสรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="56506-113">รหัสรถเข็นเป็นคุกกี้ของเบราว์เซอร์ที่มีให้ใช้งานทั่วทั้งไซต์</span><span class="sxs-lookup"><span data-stu-id="56506-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="56506-114">คุณสมบัติของโมดูลรถเข็นและช่อง</span><span class="sxs-lookup"><span data-stu-id="56506-114">Cart module properties and slots</span></span>

<span data-ttu-id="56506-115">โมดูลรถเข็นมีคุณสมบัติ **หัวข้อ** ซึ่งสามารถตั้งค่าเป็นค่าต่าง ๆ เช่น **ถุงช้อปปิ้ง** และ **สินค้าในรถเข็นของคุณ**</span><span class="sxs-lookup"><span data-stu-id="56506-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="56506-116">โมดูลที่สามารถใช้ในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="56506-117">**บล็อคข้อความ** –โมดูลนี้สนับสนุนการส่งข้อความแบบกำหนดเองในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="56506-118">ข้อความจะถูกขับเคลื่อนโดยระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="56506-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="56506-119">คุณสามารถเพิ่มข้อความใดก็ได้ เช่น "สำหรับปัญหาในการสั่งซื้อของคุณ โปรดติดต่อ 1-800-Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="56506-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="56506-120">**ตัวเลือกร้านค้า** –โมดูลนี้แสดงรายการของร้านค้าใกล้เคียง ที่มีสินค้าพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="56506-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="56506-121">ซึ่งช่วยให้ผู้ใช้ป้อนสถานที่ เพื่อค้นหาร้านค้าที่อยู่ใกล้เคียง</span><span class="sxs-lookup"><span data-stu-id="56506-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="56506-122">โมดูลตัวเลือกร้านค้าทำงานร่วมกับ Application Programming Interface กำหนดพิกัดทางภูมิศาสตร์ของ Bing Maps (API) เพื่อแปลงสถานที่ที่ลูกค้าป้อนให้เป็นละติจูดและลองจิจูด</span><span class="sxs-lookup"><span data-stu-id="56506-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="56506-123">ต้องใช้คีย์ API ของ Bing Maps และต้องเพิ่มลงในหน้าพารามิเตอร์ที่ใช้ร่วมกันของการขายปลีกใน Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="56506-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="56506-124">โมดูลนี้สนับสนุนสองคุณสมบัติ **รัศมีการค้นหา** และ **ลิงก์เงื่อนไขของการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="56506-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="56506-125">คุณสมบัติ **รัศมีการค้นหา** จะกำหนดรัศมีการค้นหาสำหรับร้านค้าในหน่วยไมล์</span><span class="sxs-lookup"><span data-stu-id="56506-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="56506-126">ถ้าไม่มีการระบุค่า จะมีการใช้รัศมีการค้นหาเริ่มต้น 50 ไมล์</span><span class="sxs-lookup"><span data-stu-id="56506-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="56506-127">ถ้ามีการใช้ Bings Maps หรือบริการภายนอกใด ๆ คุณสมบัติ **ลิงก์เงื่อนไขของการให้บริการ** สามารถใช้เพื่อระบุลิงก์ไปยังเงื่อนไขของการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="56506-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="56506-128">ลิงก์เงื่อนไขของการให้บริการจำเป็นสำหรับบริการ Bing Maps</span><span class="sxs-lookup"><span data-stu-id="56506-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="56506-129">การตั้งค่าโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-129">Cart module settings</span></span>

<span data-ttu-id="56506-130">โมดูลรถเข็นมีการตั้งค่าดังนี้ ที่สามารถตั้งค่าคอนฟิกได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="56506-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="56506-131">**ปริมาณสูงสุด** - คุณสมบัตินี้ใช้เพื่อระบุจำนวนสูงสุดของสินค้าแต่ละรายการที่สามารถเพิ่มเข้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="56506-132">ตัวอย่างเช่น ผู้ค้าปลีกอาจตั้งให้สามารถขายผลิตภัณฑ์แต่ละอย่างได้เพียง 10 ชุด ในหนึ่งธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="56506-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="56506-133">**การตรวจสอบสินค้าคงคลัง** – เมื่อมีการกำหนดค่า เป็น **จริง** สินค้าจะถูกเพืเมลงในรถเข็น เฉพาะหลังจากที่โมดูลกล่องการซื้อได้ตรวจสอบให้แน่ใจว่ามีสินค้าอยู่ในสต๊อก</span><span class="sxs-lookup"><span data-stu-id="56506-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="56506-134">การตรวจสอบสินค้าคงคลังนี้ดำเนินการทั้งสองอย่างสำหรับสถานการณ์ที่สินค้าจะถูกจัดส่ง และสำหรับสถานการณ์ที่จะมีการเบิกสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="56506-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="56506-135">ถ้าค่าถูกกำหนดเป็น **เท็จ** จะไม่มีการตรวจสอบสินค้าคงคลัง ก่อนที่จะมีการเพิ่มสินค้าลงในรถเข็นและใบสั่งถูกสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="56506-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="56506-136">**บัฟเฟอร์สินค้าคงคลัง** – ใช้คุณสมบัตินี้เพื่อระบุหมายเลขบัฟเฟอร์สำหรับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="56506-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="56506-137">สินค้าคงคลังจะมีการเก็บรักษาในเวลาจริง และเมื่อลูกค้าหลายรายที่สั่งซื้อ อาจเป็นเรื่องยากที่จะรักษาการตรวจนับสินค้าคงคลังที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="56506-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="56506-138">เมื่อมีการตรวจสอบสินค้าคงคลังแล้ว ถ้าสินค้าคงคลังน้อยกว่าจำนวนบัฟเฟอร์ ผลิตภัณฑ์จะถือว่าไม่มีในสต็อก</span><span class="sxs-lookup"><span data-stu-id="56506-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="56506-139">ดังนั้น เมื่อการขายเกิดขึ้นอย่างรวดเร็วผ่านหลายช่องทาง และการตรวจนับสินค้าคงคลังไม่ได้รับการซิงค์อย่างครบถ้วน มีความเสี่ยงน้อยกว่าที่สินค้าที่ไม่มีในสต๊อกจะถูกขาย</span><span class="sxs-lookup"><span data-stu-id="56506-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="56506-140">**กลับไปยังการช้อปปิ้ง** – คุณสมบัตินี้ใช้เพื่อระบุเส้นทางสำหรับลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="56506-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="56506-141">คุณสามารถตั้งค่าคอนฟิกเส้นทางนี้ได้ที่ระดับไซต์</span><span class="sxs-lookup"><span data-stu-id="56506-141">This route can be configured at the site level.</span></span> <span data-ttu-id="56506-142">การตั้งค่าคอนฟิกนี้ช่วยให้ร้านค้าปลีกพาลูกค้ากลับไปยังโฮมเพจ หรือหน้าอื่นๆบนไซต์</span><span class="sxs-lookup"><span data-stu-id="56506-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="56506-143">การโต้ตอบ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="56506-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="56506-144">โมดูลของรถเข็นจะดึงข้อมูลผลิตภัณฑ์โดยใช้ Commerce Scale Unit APIs</span><span class="sxs-lookup"><span data-stu-id="56506-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="56506-145">รหัสรถเข็นจากคุกกี้ของเบราว์เซอร์ใช้เพื่อดึงข้อมูลผลิตภัณฑ์ทั้งหมดจาก Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="56506-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="56506-146">เพิ่มโมดูลรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="56506-146">Add a cart module to a page</span></span>

<span data-ttu-id="56506-147">การเพิ่มโมดูลรถเข็นไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="56506-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="56506-148">สร้างส่วนย่อยที่มีชื่อว่า **ส่วนย่อยของรถเข็น** และเพิ่มโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="56506-149">เพิ่มหัวเรื่องไปยังโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="56506-150">เพิ่มโมดูลตัวเลือกร้านค้าไปยังโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="56506-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="56506-151">บันทึกส่วน แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="56506-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="56506-152">สร้างเท็มเพลตที่มีชื่อ **แม่แบบรถเข็น** และเพิ่มส่วนของรถเข็นที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="56506-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="56506-153">บันทึกแม่แบบ แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="56506-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="56506-154">สร้างหน้าที่ใช้เท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="56506-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="56506-155">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="56506-155">Save and preview the page.</span></span>
1. <span data-ttu-id="56506-156">แก้ไขหน้าให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="56506-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56506-157">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="56506-157">Additional resources</span></span>

[<span data-ttu-id="56506-158">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="56506-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="56506-159">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="56506-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="56506-160">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="56506-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="56506-161">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="56506-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="56506-162">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="56506-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="56506-163">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="56506-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="56506-164">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="56506-164">Footer module</span></span>](author-footer-module.md)
