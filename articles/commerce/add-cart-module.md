---
title: โมดูลรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696772"
---
# <a name="cart-module"></a><span data-ttu-id="648b7-103">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="648b7-104">หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="648b7-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="648b7-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="648b7-105">Overview</span></span>

<span data-ttu-id="648b7-106">โมดูลรถเข็นเป็นคอนเทนเนอร์ที่ใช้สำหรับโฮสต์โมดูลทั้งหมดที่จำเป็นต้องใช้ในการแสดงรายการที่อยู่ในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-106">A cart module is container that is used to host all the modules that are required to showcase items that are in the cart.</span></span> <span data-ttu-id="648b7-107">ตัวอย่างเช่น จะรวมสินค้าทั้งหมดที่มีการเพิ่มลงในรถเข็น สรุปใบสั่ง และรหัสโปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="648b7-107">For example, it includes all the items that have been added to the cart, the order summary, and promotional codes.</span></span>

<span data-ttu-id="648b7-108">โมดูลรถเข็นแสดงข้อมูลตามรหัสรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-108">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="648b7-109">รหัสรถเข็นเป็นคุกกี้ของเบราว์เซอร์ที่มีให้ใช้งานทั่วทั้งไซต์</span><span class="sxs-lookup"><span data-stu-id="648b7-109">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="648b7-110">คุณสมบัติของโมดูลรถเข็นและช่อง</span><span class="sxs-lookup"><span data-stu-id="648b7-110">Cart module properties and slots</span></span>

<span data-ttu-id="648b7-111">ในฐานะที่เป็นคอนเทนเนอร์ โมดูลรถเข็นจะควคุณสมบัติพื้นฐานบางอย่าง เช่น หัวข้อง และ ความกว้าง</span><span class="sxs-lookup"><span data-stu-id="648b7-111">As a container, a cart module controls some basic properties, such as the heading and the width.</span></span> <span data-ttu-id="648b7-112">โดยทั่วไปหัวข้อจะเป็นข้อความ เช่น **ถุงช้อปปิ้ง** **รถเข็นของคุณ** หรือ **สินค้าในรถเข็นของคุณ**</span><span class="sxs-lookup"><span data-stu-id="648b7-112">The heading is typically text such as **Shopping bag**, **Your cart**, or **Items in your cart**.</span></span> <span data-ttu-id="648b7-113">การตั้งค่าความกว้างจะกำหนดว่าโมดูลภายในคอนเทนเนอร์ต้องพอดีกับคอนเทนเนอร์ หรือเต็มหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="648b7-113">The width setting determines whether the modules inside the container must fit within that container, or whether they can fill the screen.</span></span>

<span data-ttu-id="648b7-114">หน้ารถเข็นสินค้าจะถูกแบ่งออกเป็นหลายภาค: สินค้าในรายการรถเข็น สรุปใบสั่ง และการชำระเงิน และฟังก์ชัน "ค้นหาในร้านค้า" </span><span class="sxs-lookup"><span data-stu-id="648b7-114">The cart page is divided into multiple regions: cart line items, order summary and checkout, and "find in store" functionality.</span></span> <span data-ttu-id="648b7-115">แต่ละภาคจะถูกแม็ปกับช่องในโมดูลรถเข็น และช่องทุกช่องยอมรับชุดของโมดูลที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="648b7-115">Each region is mapped to a slot in the cart module, and every slot accepts a predefined set of modules.</span></span>

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="648b7-116">โมดูลที่สามารถใช้ในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="648b7-117">**สินค้าในรถเข็น** –โมดูลนี้แสดงสรุปสินค้าทุกรายการที่มีการเพิ่มลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-117">**Cart line items** – This module shows a summary of every item that has been added to the cart.</span></span> <span data-ttu-id="648b7-118">ข้อมูลรวมถึงชื่อผลิตภัณฑ์ มิติที่เลือก ราคา ปริมาณ และส่วนลด</span><span class="sxs-lookup"><span data-stu-id="648b7-118">The information includes the product title, selected dimensions, price, quantity, and discounts.</span></span> <span data-ttu-id="648b7-119">นอกจากนี้โมดูลยังสนับสนุนการดำเนินการ เช่น "ลบออกจากรถเข็น" และ "เพิ่มไปยังรายการที่ต้องการ"</span><span class="sxs-lookup"><span data-stu-id="648b7-119">This module also supports actions such as "remove from cart" and "add to wish list."</span></span> <span data-ttu-id="648b7-120">สำหรับสินค้าแต่ละรายการ จะมีตัวเลือกในการจัดส่งสินค้า หรือรับสินค้าจากร้านค้า</span><span class="sxs-lookup"><span data-stu-id="648b7-120">For each line item, there is an option to ship the item or pick it up from the store.</span></span> <span data-ttu-id="648b7-121">คุณต้องตั้งค่าคอนฟิกตัวเลือกนี้แยกต่างหาก ในโมดูลการรับสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="648b7-121">This option must be configured separately in the pick up in store module.</span></span>
- <span data-ttu-id="648b7-122">**สรุปใบสั่ง** –โมดูลนี้แสดงสรุปใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="648b7-122">**Order summary** – This module shows an order summary.</span></span> <span data-ttu-id="648b7-123">ข้อมูลรวมถึง ยอดรวม การจัดส่ง ภาษี และการประหยัด</span><span class="sxs-lookup"><span data-stu-id="648b7-123">The information includes the subtotal, shipping, taxes, and savings.</span></span> <span data-ttu-id="648b7-124">สามารถตั้งค่าคอนฟิกหัวข้อสำหรับโมดูลนี้</span><span class="sxs-lookup"><span data-stu-id="648b7-124">A heading can be configured for this module.</span></span>
- <span data-ttu-id="648b7-125">**รหัสโปรโมชัน** –โมดูลนี้จะช่วยให้ลูกค้าสามารถแลกรหัสโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="648b7-125">**Promo code** – This module lets the customer redeem promotional codes.</span></span> <span data-ttu-id="648b7-126">คุณสามารถใช้หรือลบรหัสโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="648b7-126">A promotional code can be applied or removed.</span></span>
- <span data-ttu-id="648b7-127">**การชำระเงิน** –โมดูลนี้จะเริ่มต้นการดำเนินการชำระเงิน และเปลี่ยนเส้นทางผู้ใช้ไปที่หน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="648b7-127">**Checkout** – This module initiates the checkout action and redirects the user to the checkout page.</span></span> <span data-ttu-id="648b7-128">ต้องตั้งค่าคอนฟิกลิงค์สามลิงค์สำหรับโมดูลนี้:</span><span class="sxs-lookup"><span data-stu-id="648b7-128">Three links must be configured for this module:</span></span>

    - <span data-ttu-id="648b7-129">**การเงินชำระเงิน** –ลิงก์นี้บังคับให้ลูกค้าล็อกอินถ้ายังไม่ได้ล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="648b7-129">**Checkout** – This link forces customers to sign in if they aren't already signed in.</span></span>
    - <span data-ttu-id="648b7-130">**การเช็คเอาท์สำหรับแขก** –ลิงค์นี้ช่วยให้ลูกค้าที่ไม่ระบุชื่อสั่งซื้อได้</span><span class="sxs-lookup"><span data-stu-id="648b7-130">**Guest checkout** – This link lets anonymous customers place orders.</span></span> <span data-ttu-id="648b7-131">แสดงเฉพาะเมื่อลูกค้าไม่ได้ล็อกอินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="648b7-131">It's shown only when customers aren't signed in.</span></span>
    - <span data-ttu-id="648b7-132">**กลับไปที่การช้อปปิ้ง** –ลิงค์นี้ให้ลูกค้าไปที่โฮมเพจหรือหน้าอื่นๆ เพื่อให้สามารถดำเนินการเลือกซื้อต่อไป</span><span class="sxs-lookup"><span data-stu-id="648b7-132">**Back to shopping** – This link lets customers go to the home page or any other page, so that they can continue to shop.</span></span>

- <span data-ttu-id="648b7-133">**บล็อคเนื้อหา** –โมดูลนี้สนับสนุนการส่งข้อความแบบกำหนดเองในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-133">**Content rich block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="648b7-134">ข้อความจะถูกขับเคลื่อนโดยระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="648b7-134">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="648b7-135">คุณสามารถเพิ่มข้อความใดก็ได้ เช่น "สำหรับปัญหาในการสั่งซื้อ โปรดติดต่อ 1-800-Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="648b7-135">Any message can be added, such as "For issues with the order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="648b7-136">**เบิกสินค้าในร้านค้า** –โมดูลนี้แสดงรายการของร้านค้าใกล้เคียง ที่มีสินค้าพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="648b7-136">**Pick up in store** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="648b7-137">โดยค่าเริ่มต้น โมดูลนี้จะแสดงร้านค้าที่อยู่ภายในรัศมี 50 ไมล์จากสถานที่ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="648b7-137">By default, this module shows stores that are within a 50-mile radius of the customer's location.</span></span> <span data-ttu-id="648b7-138">อย่างไรก็ตาม คุณสามารถกำหนดรัศมีในการค้นหาได้ในโมดูล</span><span class="sxs-lookup"><span data-stu-id="648b7-138">However, the search radius can be customized in the module.</span></span> <span data-ttu-id="648b7-139">สำหรับร้านค้าแต่ละร้าน ทำการตรวจสอบสินค้าคงคลัง ถ้ามีการเปิดใช้งานฟังก์ชันการตรวจสอบสินค้าคงคลัง และมีการแสดงข้อความ มีสินค้าในสต๊อก หรือ ไม่มีสินค้าในสต๊อก ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="648b7-139">For each store, an inventory check is done, if the inventory check functionality is turned on, and an appropriate in-stock or out-of-stock message is shown.</span></span>
- <span data-ttu-id="648b7-140">**ค้นหาร้านค้า โดย Bing Maps** - โมดูลนี้สามารถใช้ในโมดูลเบิกสินค้าจากร้านค้า</span><span class="sxs-lookup"><span data-stu-id="648b7-140">**Store search by Bing Maps** – This module can be used inside the pick up in store module.</span></span> <span data-ttu-id="648b7-141">ช่วยให้ลูกค้าค้นหาร้านค้าด้วยการป้อนตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="648b7-141">It lets customers search for stores by entering a location.</span></span> <span data-ttu-id="648b7-142">อินเทอร์เฟสเขียนโปรแกรมกำหนดพิกัดทางภูมิศาสตร์ของ Bing Maps (API) ถูกใช้เพื่อแปลงสถานที่ที่ลูกค้าป้อนให้เป็นละติจูดและลองจิจูด</span><span class="sxs-lookup"><span data-stu-id="648b7-142">The Bing Maps geocoding application programming interface (API) is used to convert the location that the customer entered to a latitude and a longitude.</span></span> <span data-ttu-id="648b7-143">ถ้าไม่มีการใช้โมดูลนี้ เฉพาะร้านค้าที่อยู่ใกล้กับสถานที่ปัจจุบันของลูกค้าจะถูกแสดงขึ้น และลูกค้าไม่สามารถค้นหาสถานที่อื่นได้</span><span class="sxs-lookup"><span data-stu-id="648b7-143">If this module isn't used, only stores that are near the customer's current location are shown, and the customer can't search for a different location.</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="648b7-144">การตั้งค่าโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-144">Cart module settings</span></span>

<span data-ttu-id="648b7-145">โมดูลรถเข็นมีสามการตั้งค่า ที่สามารถตั้งค่าคอนฟิกได้:</span><span class="sxs-lookup"><span data-stu-id="648b7-145">Cart modules have three settings that can be configured:</span></span>

- <span data-ttu-id="648b7-146">**ปริมาณสูงสุด** - จำนวนสูงสุดของสินค้าแต่ละรายการที่สามารถเพิ่มเข้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-146">**Maximum quantity** – The maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="648b7-147">ตัวอย่างเช่น ผู้ค้าปลีกอาจตั้งให้สามารถขายผลิตภัณฑ์แต่ละอย่างได้เพียง 10 ชุด ในหนึ่งธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="648b7-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="648b7-148">**การตรวจสอบสินค้าคงคลัง** – เมื่อมีการกำหนดค่า เป็น **จริง** สินค้าจะถูกเพืเมลงในรถเข็น เฉพาะหลังจากที่โมดูลกล่องการซื้อได้ตรวจสอบให้แน่ใจว่ามีสินค้าอยู่ในสต๊อก</span><span class="sxs-lookup"><span data-stu-id="648b7-148">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="648b7-149">การตรวจสอบสินค้าคงคลังนี้ดำเนินการทั้งสองอย่างสำหรับสถานการณ์ที่สินค้าจะถูกจัดส่ง และสำหรับสถานการณ์ที่จะมีการเบิกสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="648b7-149">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="648b7-150">ถ้าค่าถูกกำหนดเป็น **เท็จ** จะไม่มีการตรวจสอบสินค้าคงคลัง ก่อนที่จะมีการเพิ่มสินค้าลงในรถเข็นและใบสั่งถูกสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="648b7-150">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="648b7-151">**บัฟเฟอร์สินค้าคงคลัง** –สินค้าคงคลังจะมีการเก็บรักษาในเวลาจริง และเมื่อลูกค้าหลายรายที่สั่งซื้อ อาจเป็นเรื่องยากที่จะรักษาการตรวจนับสินค้าคงคลังที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="648b7-151">**Inventory buffer** – Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="648b7-152">ดังนั้น จึงสามารถกำหนดบัฟเฟอร์ให้กับสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="648b7-152">Therefore, a buffer can be defined for inventory.</span></span> <span data-ttu-id="648b7-153">เมื่อมีการตรวจสอบสินค้าคงคลังแล้ว ถ้าสินค้าคงคลังน้อยกว่าจำนวนบัฟเฟอร์ ผลิตภัณฑ์จะถือว่าไม่มีในสต็อก</span><span class="sxs-lookup"><span data-stu-id="648b7-153">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="648b7-154">ดังนั้น เมื่อการขายเกิดขึ้นอย่างรวดเร็วผ่านหลายช่องทาง เพื่อให้การตรวจนับสินค้าคงคลังไม่ได้รับการซิงค์อย่างครบถ้วน มีความเสี่ยงน้อยกว่าที่สินค้าที่ไม่มีในสต๊อกจะถูกขาย</span><span class="sxs-lookup"><span data-stu-id="648b7-154">Therefore, when sales occur quickly through several channels, so that the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="retail-server-interaction"></a><span data-ttu-id="648b7-155">การโต้ตอบเซิร์ฟเวอร์การขายปลีก</span><span class="sxs-lookup"><span data-stu-id="648b7-155">Retail Server interaction</span></span>

<span data-ttu-id="648b7-156">โมดูลรถเข็นจะดึงข้อมูลผลิตภัณฑ์โดยใช้ Retail Server APIs</span><span class="sxs-lookup"><span data-stu-id="648b7-156">The cart module retrieves product information by using Retail Server APIs.</span></span> <span data-ttu-id="648b7-157">รหัสรถเข็นจากคุกกี้ของเบราว์เซอร์ใช้เพื่อดึงข้อมูลผลิตภัณฑ์ทั้งหมดจาก Retail Server</span><span class="sxs-lookup"><span data-stu-id="648b7-157">The cart ID from the browser cookie is used to retrieve all the product information from Retail Server.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="648b7-158">เพิ่มโมดูลรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="648b7-158">Add a cart module to a page</span></span>

<span data-ttu-id="648b7-159">การเพิ่มโมดูลรถเข็นไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="648b7-159">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="648b7-160">สร้างส่วนย่อยที่มีชื่อว่า **ส่วนย่อยของรถเข็น** และเพิ่มโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-160">Create a fragment that is named **cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="648b7-161">ในช่อง **สินค้าของรายการรถเข็น** ของโมดูลรถเข็นให้เพิ่มโมดูลสินค้าของรายการรถเข็น</span><span class="sxs-lookup"><span data-stu-id="648b7-161">In the **Cart line items** slot of the cart module, add a cart line items module.</span></span>
1. <span data-ttu-id="648b7-162">ในช่อง **สรุปใบสั่งซื้อ** ให้เพิ่มโมดูลสรุปใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="648b7-162">In the **Order summary** slot, add an order summary module.</span></span>
1. <span data-ttu-id="648b7-163">ในช่อง **รหัสโปรโมชัน** เพิ่มโมดูลรหัสโปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="648b7-163">In the **Promo code** slot, add a promo code module.</span></span>
1. <span data-ttu-id="648b7-164">ในช่อง **การชำระเงิน** ให้เพิ่มโมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="648b7-164">In the **Checkout** slot, add a checkout module.</span></span>
1. <span data-ttu-id="648b7-165">ในช่อง **ค้นหาในร้าค้า** ให้เพิ่มโมดูลการเบิกสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="648b7-165">In the **Find in Store** slot, add a pick up in store module.</span></span>
1. <span data-ttu-id="648b7-166">ในโมดูิเบิกสินค้าในร้าน เลือกช่อง **การค้นหาร้านค้า** และเพิ่มการค้นหาร้านค้าโดยใช้โมดูล Bing Maps</span><span class="sxs-lookup"><span data-stu-id="648b7-166">In the pick up in store module, select the **Store search** slot, and add a store search by Bing Maps module.</span></span>
1. <span data-ttu-id="648b7-167">เช็คอินส่วน และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="648b7-167">Check in the fragment, and publish it.</span></span>
1. <span data-ttu-id="648b7-168">สร้างเท็มเพลตที่มีชื่อ **เท็มเพลตรถเข็น** และเพิ่มส่วนของรถเข็นที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="648b7-168">Create a template that is named **cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="648b7-169">บันทึกเท็มเพลต เช็คอิน และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="648b7-169">Save the template, check it in, and publish it.</span></span>
1. <span data-ttu-id="648b7-170">สร้างหน้าที่ใช้เท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="648b7-170">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="648b7-171">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="648b7-171">Save and preview the page.</span></span>
1. <span data-ttu-id="648b7-172">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="648b7-172">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="648b7-173">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="648b7-173">Additional resources</span></span>

[<span data-ttu-id="648b7-174">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="648b7-174">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="648b7-175">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="648b7-175">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="648b7-176">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="648b7-176">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="648b7-177">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="648b7-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="648b7-178">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="648b7-178">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="648b7-179">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="648b7-179">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="648b7-180">โมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="648b7-180">Footer module</span></span>](author-footer-module.md)
