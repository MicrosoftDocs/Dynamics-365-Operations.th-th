---
title: โมดูลกล่องการซื้อ
description: หัวข้อนี้ครอบคลุมโมดูลกล่องการฃื้อ และอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3417156cbf3cb20a5190e5e51b61b3423816895a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154074"
---
# <a name="buy-box-module"></a><span data-ttu-id="0429c-103">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-103">Buy box module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0429c-104">หัวข้อนี้ครอบคลุมโมดูลกล่องการฃื้อ และอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0429c-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0429c-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="0429c-105">Overview</span></span>

<span data-ttu-id="0429c-106">โดยทั่วไปแล้วข้อกำหนด *กล่องการซื้อ* อ้างถึงพื้นที่ของเพจรายละเอียดผลิตภัณฑ์ที่อยู่ "เหนือโฟลด์" และที่โฮสต์ข้อมูลที่สำคัญทั้งหมดที่จำเป็นต่อการทำการซื้อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0429c-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="0429c-107">(พื้นที่ที่อยู่ "เหนือโฟลด์" จะปรากฏขึ้นเมื่อมีการโหลดหน้าแรก ดังนั้นผู้ใช้จึงไม่ต้องเลื่อนลงเพื่อดูรายการนั้น)</span><span class="sxs-lookup"><span data-stu-id="0429c-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="0429c-108">โมดูลกล่องการซื้อคือตู้คอนเทนเนอร์พิเศษที่ใช้เพื่อโฮสต์โมดูลทั้งหมดที่แสดงอยู่ในพื้นที่กล่องการซื้อของหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0429c-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="0429c-109">URL ของหน้ารายละเอียดผลิตภัณฑ์รวมถึงรหัสผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0429c-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="0429c-110">ข้อมูลทั้งหมดที่จำเป็นต้องใช้ในการแสดงโมดูลกล่องการซื้อ จะได้รับมาจากรหัสผลิตภัณฑ์นี้</span><span class="sxs-lookup"><span data-stu-id="0429c-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="0429c-111">ถ้าไม่ได้ระบุหมายเลขผลิตภัณฑ์ จะไม่มีการแสดงผลโมดูลกล่องการซื้ออย่างถูกต้องบนเพจ</span><span class="sxs-lookup"><span data-stu-id="0429c-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="0429c-112">ดังนั้น คุณสามารถใช้โมดูลในกล่องการซื้อบนหน้าที่มีเนื้อหาของผลิตภัณฑ์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0429c-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="0429c-113">เมื่อต้องการใช้บนหน้าเว็บที่ไม่เนื้อหาของผลิตภัณฑ์ (ตัวอย่างเช่น โฮมเพจ หรือหน้าการตลาด) คุณต้องทำการเลือกกำหนดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0429c-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="0429c-114">คุณสมบัติและช่องของกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-114">Buy box module properties and slots</span></span> 

<span data-ttu-id="0429c-115">ในหน้ารายละเอียดของผลิตภัณฑ์ กล่องการซื้อจะแบ่งออกเป็นสองภาค: ภาคสื่อทางด้านซ้าย และภาคเนื้อหาทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="0429c-115">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="0429c-116">ตามค่าเริ่มต้น อัตราส่วนของความกว้างของคอลัมน์สื่อที่มีความกว้างของคอลัมน์พื้นที่เนื้อหาคือ 2:1</span><span class="sxs-lookup"><span data-stu-id="0429c-116">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="0429c-117">บนอุปกรณ์เคลื่อนที่ ทั้งสองภูมิภาคจะเป็นแบบซ้อนกัน เพื่อให้พื้นที่หนึ่งปรากฏอยู่ด้านล่างของภาคอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="0429c-117">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="0429c-118">ชุดรูปแบบสามารถใช้ในการเลือกกำหนดความกว้างคอลัมน์และการจัดอันดับการซ้อน</span><span class="sxs-lookup"><span data-stu-id="0429c-118">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="0429c-119">โมดูลในกล่องการซื้อแสดงชื่อ คำอธิบาย ราคา และการให้คะแนนของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0429c-119">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="0429c-120">นอกจากนี้ยังให้ลูกค้าเลือกผลิตภัณฑ์ย่อยที่มีแอททริบิวต์ผลิตภัณฑ์ที่แตกต่างกัน เช่น ขนาด ลักษณะ และสี</span><span class="sxs-lookup"><span data-stu-id="0429c-120">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="0429c-121">เมื่อเลือกผลิตภัณฑ์ย่อย คุณสมบัติอื่นๆ ในกล่องการซื้อ (ตัวอย่าง เช่น คำอธิบายผลิตภัณฑ์และรูปภาพ) จะถูกอัพเดตเพื่อให้สะท้อนถึงข้อมูลตัวแปร</span><span class="sxs-lookup"><span data-stu-id="0429c-121">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="0429c-122">มีการเลือกตัวเลือกปริมาณไว้ เพื่อให้ลูกค้าสามารถระบุปริมาณของสินค้าที่จะซื้อได้</span><span class="sxs-lookup"><span data-stu-id="0429c-122">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="0429c-123">ปริมาณสูงสุดที่สามารถซื้อได้สามารถกำหนดได้ในการตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="0429c-123">The maximum quantity that can be purchased can be defined in the site settings.</span></span>
 
<span data-ttu-id="0429c-124">จากกล่องการซื้อ นอกจากนี้คุณยังสามารถทำการดำเนินการต่าง ๆ เช่น เพิ่มผลิตภัณฑ์ลงในรถเข็น เพิ่มผลิตภัณฑ์ลงในรายการโปรดของลูกค้า และเลือกสถานที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="0429c-124">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="0429c-125">การดำเนินการเหล่านี้สามารถดำเนินการกับผลิตภัณฑ์ หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="0429c-125">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="0429c-126">เมื่อต้องการเพิ่มผลิตภัณฑ์ลงในรายการโปรด ลูกค้าต้องล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="0429c-126">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="0429c-127">ชุดรูปแบบสามารถใช้ในการลบหรือเปลี่ยนแปลงลำดับของคุณสมบัติผลิตภัณฑ์ของกล่องการซื้อ และการควบคุมการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0429c-127">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="0429c-128">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="0429c-128">Module properties</span></span>

- <span data-ttu-id="0429c-129">**แท็กหัวเรื่อง** – คุณสมบัตินี้กำหนดป้ายชื่อเรื่องสำหรับชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0429c-129">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="0429c-130">ถ้ากล่องการซื้ออยู่ที่ด้านบนของหน้าคุณสมบัตินี้ควรถูกตั้งค่าเป็น **h1** เพื่อให้เป็นไปตามมาตรฐานการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="0429c-130">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="0429c-131">โมดูลที่สามารถใช้ในโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-131">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="0429c-132">**แกลเลอรีสื่อ** –โมดูลนี้ใช้ในการแสดงรูปภาพของผลิตภัณฑ์บนหน้ารายละเอียดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0429c-132">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="0429c-133">ซึ่งสามารถรองรับได้หลายรูป</span><span class="sxs-lookup"><span data-stu-id="0429c-133">It can support one to many images.</span></span> <span data-ttu-id="0429c-134">นอกจากนี้ยังสนับสนุนรูปภาพขนาดย่อ</span><span class="sxs-lookup"><span data-stu-id="0429c-134">It also supports thumbnail images.</span></span> <span data-ttu-id="0429c-135">ภาพขนาดย่อสามารถจัดเรียงอย่างใดอย่างหนึ่งตามแนวนอน (โดยเป็นแถวด้านล่างรูป) หรือในแนวตั้ง (เป็นคอลัมน์ที่อยู่ถัดจากรูปภาพ)</span><span class="sxs-lookup"><span data-stu-id="0429c-135">The thumbnail images can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="0429c-136">โมดูลที่แกลเลอรีสื่อสามารถเพิ่มเข้าไปในช่อง **สื่อ** ในโมดูลกล่องการซื้อได้</span><span class="sxs-lookup"><span data-stu-id="0429c-136">The media gallery module can be added to the **Media** slot in the buy box module.</span></span> <span data-ttu-id="0429c-137">ปัจจุบันสนับสนุนเฉพาะรูปภาพเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0429c-137">It currently supports only images.</span></span> 
- <span data-ttu-id="0429c-138">**ตัวเลือกร้านค้า** –โมดูลนี้แสดงรายการของร้านค้าใกล้เคียง ที่มีสินค้าพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="0429c-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="0429c-139">ซึ่งช่วยให้ผู้ใช้ป้อนสถานที่ เพื่อค้นหาร้านค้าที่อยู่ใกล้เคียง</span><span class="sxs-lookup"><span data-stu-id="0429c-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="0429c-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลตัวเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="0429c-140">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="0429c-141">การตั้งค่าโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-141">Buy box module settings</span></span>

<span data-ttu-id="0429c-142">โมดูลกล่องการซื้อมีสามการตั้งค่าที่สามารถตั้งค่าคอนฟิกได้: **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="0429c-142">Buy box modules have three settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="0429c-143">**ปริมาณสูงสุด** - คุณสมบัตินี้ใช้เพื่อระบุจำนวนสูงสุดของสินค้าแต่ละรายการที่สามารถเพิ่มเข้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="0429c-143">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="0429c-144">ตัวอย่างเช่น ผู้ค้าปลีกอาจตั้งให้สามารถขายผลิตภัณฑ์แต่ละอย่างได้เพียง 10 ชุด ในหนึ่งธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0429c-144">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="0429c-145">**การตรวจสอบสินค้าคงคลัง** – เมื่อมีการกำหนดค่า เป็น **จริง** สินค้าจะถูกเพืเมลงในรถเข็น เฉพาะหลังจากที่โมดูลกล่องการซื้อได้ตรวจสอบให้แน่ใจว่ามีสินค้าอยู่ในสต๊อก</span><span class="sxs-lookup"><span data-stu-id="0429c-145">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="0429c-146">การตรวจสอบสินค้าคงคลังนี้ดำเนินการทั้งสองอย่างสำหรับสถานการณ์ที่สินค้าจะถูกจัดส่ง และสำหรับสถานการณ์ที่จะมีการเบิกสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="0429c-146">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="0429c-147">ถ้าค่าถูกกำหนดเป็น **เท็จ** จะไม่มีการตรวจสอบสินค้าคงคลัง ก่อนที่จะมีการเพิ่มสินค้าลงในรถเข็นและใบสั่งถูกสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-147">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="0429c-148">**บัฟเฟอร์สินค้าคงคลัง** – ใช้คุณสมบัตินี้เพื่อระบุหมายเลขบัฟเฟอร์สำหรับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0429c-148">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="0429c-149">สินค้าคงคลังจะมีการเก็บรักษาในเวลาจริง และเมื่อลูกค้าหลายรายที่สั่งซื้อ อาจเป็นเรื่องยากที่จะรักษาการตรวจนับสินค้าคงคลังที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0429c-149">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="0429c-150">เมื่อมีการตรวจสอบสินค้าคงคลังแล้ว ถ้าสินค้าคงคลังน้อยกว่าจำนวนบัฟเฟอร์ ผลิตภัณฑ์จะถือว่าไม่มีในสต็อก</span><span class="sxs-lookup"><span data-stu-id="0429c-150">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="0429c-151">ดังนั้น เมื่อการขายเกิดขึ้นอย่างรวดเร็วผ่านหลายช่องทาง และการตรวจนับสินค้าคงคลังไม่ได้รับการซิงค์อย่างครบถ้วน มีความเสี่ยงน้อยกว่าที่สินค้าที่ไม่มีในสต๊อกจะถูกขาย</span><span class="sxs-lookup"><span data-stu-id="0429c-151">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="0429c-152">การโต้ตอบ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="0429c-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="0429c-153">โมดูลของกล่องการซื้อจะดึงข้อมูลผลิตภัณฑ์โดยใช้ Commerce Scale Unit APIs</span><span class="sxs-lookup"><span data-stu-id="0429c-153">The buy box module retrieves product information using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="0429c-154">รหัสผลิตภัณฑ์จากหน้ารายละเอียดผลิตภัณฑ์ใช้เพื่อดึงข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0429c-154">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="0429c-155">เพิ่มโมดูลในกล่องการซื้อไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="0429c-155">Add a buy box module to a page</span></span>

<span data-ttu-id="0429c-156">การเพิ่มโมดูลกล่องการซื้อไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0429c-156">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0429c-157">สร้างส่วนย่อยที่มีชื่อว่า **ส่วนย่อยของกล่องการซื้อ** และเพิ่มโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-157">Create a fragment that is named **buy box fragment**, and add a buy box module to it.</span></span>
1. <span data-ttu-id="0429c-158">ในช่อง **สื่อ** ของโมดูลกล่องการซื้อ เพิ่มโมดูลแกลเลอรี่สื่อ</span><span class="sxs-lookup"><span data-stu-id="0429c-158">In the **Media** slot of the buy box module, add a media gallery module.</span></span>
1. <span data-ttu-id="0429c-159">ในช่อง **ตัวเลือกร้านค้า** ของโมดูลกล่องการซื้อ ให้เพิ่มโมดูลตัวเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="0429c-159">In the **Store selector** slot of the buy box module, add a store selector module.</span></span>
1. <span data-ttu-id="0429c-160">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="0429c-160">Check in the page, and publish it.</span></span>
1. <span data-ttu-id="0429c-161">สร้างเท็มเพลตสำหรับหน้ารายละเอียดผลิตภัณฑ์ และตั้งชื่อว่า **เท็มเพลต PDP**</span><span class="sxs-lookup"><span data-stu-id="0429c-161">Create a template for a product details page, and name it **PDP template**.</span></span>
1. <span data-ttu-id="0429c-162">เพิ่มหน้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0429c-162">Add a default page.</span></span>
1. <span data-ttu-id="0429c-163">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มส่วนย่อยของกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-163">In the **Main** slot of the default page, add a buy box fragment.</span></span>
1. <span data-ttu-id="0429c-164">บันทึกแม่แบบ แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="0429c-164">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="0429c-165">ใช้เท็มเพลตที่คุณเพิ่งสร้างขึ้นเพื่อสร้างหน้าที่ชื่อ **หน้า PDP**</span><span class="sxs-lookup"><span data-stu-id="0429c-165">Use the template that you just created to create a page that is named **PDP page**.</span></span>
1. <span data-ttu-id="0429c-166">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มส่วนย่อยของกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-166">In the **Main** slot of the new page, add a buy box fragment.</span></span>
1. <span data-ttu-id="0429c-167">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="0429c-167">Save and preview the page.</span></span> <span data-ttu-id="0429c-168">เพิ่มพารามิเตอร์สตริงการสอบถาม **?productid=&lt;product id&gt;** ไปยัง URL ของหน้าแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0429c-168">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="0429c-169">ในลักษณะนี้ บริบทของผลิตภัณฑ์จะถูกใช้เพื่อโหลด และทำให้หน้าแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0429c-169">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="0429c-170">บันทึกหน้า แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="0429c-170">Save the page, finish editing it, and publish it.</span></span> <span data-ttu-id="0429c-171">กล่องการซื้อควรปรากฏขึ้นบนหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0429c-171">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0429c-172">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0429c-172">Additional resources</span></span>

[<span data-ttu-id="0429c-173">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0429c-173">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0429c-174">โมดูลตัวเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="0429c-174">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="0429c-175">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="0429c-175">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0429c-176">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="0429c-176">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0429c-177">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="0429c-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0429c-178">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0429c-178">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0429c-179">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="0429c-179">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0429c-180">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="0429c-180">Footer module</span></span>](author-footer-module.md)
