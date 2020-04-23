---
title: โมดูลรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261432"
---
# <a name="cart-module"></a><span data-ttu-id="eadea-103">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="eadea-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eadea-104">หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="eadea-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="eadea-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="eadea-105">Overview</span></span>

<span data-ttu-id="eadea-106">โมดูลรถเข็นแสดงสินค้าที่มีการเพิ่มลงในรถเข็น ก่อนที่ลูกค้าจะดำเนินการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="eadea-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="eadea-107">นอกจากนี้ โมดูลยังแสดงสรุปใบสั่งและอนุญาตให้ลูกค้าสามารถใช้หรือลบรหัสโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="eadea-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="eadea-108">โมดูลรถเข็นสนับสนุนการชำระเงินของผู้ที่ลงชื่อเข้าใช้ และการชำระเงินของผู้เยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="eadea-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="eadea-109">นอกจากนี้ยังสนับสนุนลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="eadea-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="eadea-110">คุณสามารถตั้งค่าคอนฟิกเส้นทางสำหรับลิงก์นี้ได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย \> เส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="eadea-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="eadea-111">โมดูลรถเข็นแสดงข้อมูลตามรหัสรถเข็น ซึ่งเป็นคุ้กกี้ของเบราว์เซอร์ที่มีอยู่ทั่วทั้งไซต์</span><span class="sxs-lookup"><span data-stu-id="eadea-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="eadea-112">คุณสมบัติของโมดูลรถเข็นและช่อง</span><span class="sxs-lookup"><span data-stu-id="eadea-112">Cart module properties and slots</span></span>

<span data-ttu-id="eadea-113">โมดูลรถเข็นมีคุณสมบัติ **หัวข้อ** ซึ่งสามารถตั้งค่าเป็นค่าต่าง ๆ เช่น **ถุงช้อปปิ้ง** และ **สินค้าในรถเข็นของคุณ**</span><span class="sxs-lookup"><span data-stu-id="eadea-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="eadea-114">โมดูลที่สามารถใช้ในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="eadea-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="eadea-115">**บล็อคข้อความ** –โมดูลนี้สนับสนุนการส่งข้อความแบบกำหนดเองในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="eadea-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="eadea-116">ข้อความจะถูกขับเคลื่อนโดยระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="eadea-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="eadea-117">คุณสามารถเพิ่มข้อความใดก็ได้ เช่น "สำหรับปัญหาในการสั่งซื้อของคุณ โปรดติดต่อ 1-800-Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="eadea-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="eadea-118">**ตัวเลือกร้านค้า** –โมดูลนี้แสดงรายการของร้านค้าใกล้เคียง ที่มีสินค้าพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="eadea-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="eadea-119">ซึ่งช่วยให้ผู้ใช้ป้อนสถานที่ เพื่อค้นหาร้านค้าที่อยู่ใกล้เคียง</span><span class="sxs-lookup"><span data-stu-id="eadea-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="eadea-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลตัวเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="eadea-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="eadea-121">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="eadea-121">Module properties</span></span>

<span data-ttu-id="eadea-122">โมดูลรถเข็นมีการตั้งค่าดังนี้ ที่สามารถตั้งค่าคอนฟิกได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="eadea-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="eadea-123">**ปริมาณสูงสุด** - คุณสมบัตินี้ใช้เพื่อระบุจำนวนสูงสุดของสินค้าแต่ละรายการที่สามารถเพิ่มเข้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="eadea-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="eadea-124">ตัวอย่างเช่น ผู้ค้าปลีกอาจตั้งให้สามารถขายผลิตภัณฑ์แต่ละอย่างได้เพียง 10 ชุด ในหนึ่งธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="eadea-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="eadea-125">**การตรวจสอบสินค้าคงคลัง** – เมื่อมีการกำหนดค่า เป็น **จริง** สินค้าจะถูกเพืเมลงในรถเข็น เฉพาะหลังจากที่โมดูลกล่องการซื้อได้ตรวจสอบให้แน่ใจว่ามีสินค้าอยู่ในสต๊อก</span><span class="sxs-lookup"><span data-stu-id="eadea-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="eadea-126">มีการดำเนินการการตรวจสอบสินค้าคงคลังนี้สำหรับสถานการณ์ที่ซึ่งสินค้าจะถูกจัดส่ง และสำหรับสถานการณ์ที่ซึ่งจะมีการเบิกสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="eadea-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="eadea-127">ถ้าค่าถูกกำหนดเป็น **เท็จ** จะไม่มีการตรวจสอบสินค้าคงคลัง ก่อนที่จะมีการเพิ่มสินค้าลงในรถเข็นและใบสั่งถูกสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="eadea-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="eadea-128">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกการตั้งค่าสินค้าคงคลังในฝ่ายสนับสนุน โปรดดูที่ [คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก](calculated-inventory-retail-channels.md)</span><span class="sxs-lookup"><span data-stu-id="eadea-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="eadea-129">**บัฟเฟอร์สินค้าคงคลัง** – ใช้คุณสมบัตินี้เพื่อระบุหมายเลขบัฟเฟอร์สำหรับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="eadea-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="eadea-130">สินค้าคงคลังจะมีการเก็บรักษาในเวลาจริง และเมื่อลูกค้าหลายรายที่สั่งซื้อ อาจเป็นเรื่องยากที่จะรักษาการตรวจนับสินค้าคงคลังที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="eadea-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="eadea-131">เมื่อมีการตรวจสอบสินค้าคงคลังแล้ว ถ้าสินค้าคงคลังน้อยกว่าจำนวนบัฟเฟอร์ ผลิตภัณฑ์จะถือว่าไม่มีในสต็อก</span><span class="sxs-lookup"><span data-stu-id="eadea-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="eadea-132">ดังนั้น เมื่อการขายเกิดขึ้นอย่างรวดเร็วผ่านหลายช่องทาง และการตรวจนับสินค้าคงคลังไม่ได้รับการซิงค์อย่างครบถ้วน มีความเสี่ยงน้อยกว่าที่สินค้าที่ไม่มีในสต๊อกจะถูกขาย</span><span class="sxs-lookup"><span data-stu-id="eadea-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="eadea-133">**กลับไปยังการช้อปปิ้ง** – คุณสมบัตินี้ใช้เพื่อระบุเส้นทางสำหรับลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="eadea-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="eadea-134">คุณสามารถตั้งค่าคอนฟิกกระบวนการผลิตที่ระดับไซต์ ซึ่งช่วยให้ร้านค้าปลีกสามารถนำลูกค้ากลับไปยังโฮมเพจหรือหน้าอื่นๆ บนไซต์ได้</span><span class="sxs-lookup"><span data-stu-id="eadea-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="eadea-135">การโต้ตอบ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="eadea-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="eadea-136">โมดูลของรถเข็นจะดึงข้อมูลผลิตภัณฑ์โดยใช้ Commerce Scale Unit APIs</span><span class="sxs-lookup"><span data-stu-id="eadea-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="eadea-137">รหัสรถเข็นจากคุกกี้ของเบราว์เซอร์ใช้เพื่อดึงข้อมูลผลิตภัณฑ์ทั้งหมดจาก Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="eadea-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="eadea-138">เพิ่มโมดูลรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="eadea-138">Add a cart module to a page</span></span>

<span data-ttu-id="eadea-139">การเพิ่มโมดูลรถเข็นไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="eadea-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="eadea-140">สร้างส่วนที่มีชื่อว่า **ส่วนของรถเข็น** และเพิ่มโมดูลรถเข็นไปยังส่วนใหม่</span><span class="sxs-lookup"><span data-stu-id="eadea-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="eadea-141">เพิ่มหัวเรื่องไปยังโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="eadea-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="eadea-142">เพิ่มโมดูลตัวเลือกร้านค้าไปยังโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="eadea-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="eadea-143">บันทึกส่วน แก้ไขให้เสร็จสิ้น และจากนั้น เผยแพร่ส่วน</span><span class="sxs-lookup"><span data-stu-id="eadea-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="eadea-144">สร้างเท็มเพลตที่มีชื่อว่า **เท็มเพลตรถเข็น** และเพิ่มส่วนของรถเข็นที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="eadea-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="eadea-145">บันทึกเท็มเพลต แก้ไขให้เสร็จสิ้น และจากนั้น เผยแพร่เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="eadea-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="eadea-146">สร้างหน้าที่ใช้เท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="eadea-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="eadea-147">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="eadea-147">Save and preview the page.</span></span>
1. <span data-ttu-id="eadea-148">แก้ไขหน้าให้เสร็จสิ้น และจากนั้น เผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="eadea-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eadea-149">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="eadea-149">Additional resources</span></span>

[<span data-ttu-id="eadea-150">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="eadea-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="eadea-151">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="eadea-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="eadea-152">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="eadea-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="eadea-153">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="eadea-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="eadea-154">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="eadea-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="eadea-155">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="eadea-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="eadea-156">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="eadea-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="eadea-157">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="eadea-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="eadea-158">โมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="eadea-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="eadea-159">คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="eadea-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
