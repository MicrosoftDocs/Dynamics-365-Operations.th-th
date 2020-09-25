---
title: โมดูลกล่องการซื้อ
description: หัวข้อนี้ครอบคลุมโมดูลกล่องการฃื้อ และอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 6556ee8acf1e24a9f6ceddb622960cb3ac891852
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761308"
---
# <a name="buy-box-module"></a><span data-ttu-id="6054d-103">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="6054d-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6054d-104">หัวข้อนี้ครอบคลุมโมดูลกล่องการฃื้อ และอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6054d-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6054d-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="6054d-105">Overview</span></span>

<span data-ttu-id="6054d-106">โดยทั่วไปแล้วข้อกำหนด *กล่องการซื้อ* อ้างถึงพื้นที่ของเพจรายละเอียดผลิตภัณฑ์ที่อยู่ "เหนือโฟลด์" และที่โฮสต์ข้อมูลที่สำคัญทั้งหมดที่จำเป็นต่อการทำการซื้อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6054d-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="6054d-107">(พื้นที่ที่อยู่ "เหนือโฟลด์" จะปรากฏขึ้นเมื่อมีการโหลดหน้าแรก ดังนั้นผู้ใช้จึงไม่ต้องเลื่อนลงเพื่อดูรายการนั้น)</span><span class="sxs-lookup"><span data-stu-id="6054d-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="6054d-108">โมดูลกล่องการซื้อคือตู้คอนเทนเนอร์พิเศษที่ใช้เพื่อโฮสต์โมดูลทั้งหมดที่แสดงอยู่ในพื้นที่กล่องการซื้อของหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6054d-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="6054d-109">URL ของหน้ารายละเอียดผลิตภัณฑ์รวมถึงรหัสผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6054d-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="6054d-110">ข้อมูลทั้งหมดที่จำเป็นต้องใช้ในการแสดงโมดูลกล่องการซื้อ จะได้รับมาจากรหัสผลิตภัณฑ์นี้</span><span class="sxs-lookup"><span data-stu-id="6054d-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="6054d-111">ถ้าไม่ได้ระบุหมายเลขผลิตภัณฑ์ จะไม่มีการแสดงผลโมดูลกล่องการซื้ออย่างถูกต้องบนเพจ</span><span class="sxs-lookup"><span data-stu-id="6054d-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="6054d-112">ดังนั้น คุณสามารถใช้โมดูลในกล่องการซื้อบนหน้าที่มีเนื้อหาของผลิตภัณฑ์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6054d-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="6054d-113">เมื่อต้องการใช้บนหน้าเว็บที่ไม่เนื้อหาของผลิตภัณฑ์ (ตัวอย่างเช่น โฮมเพจ หรือหน้าการตลาด) คุณต้องทำการเลือกกำหนดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6054d-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="6054d-114">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลกล่องการซื้อบนหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6054d-114">The following image shows an example of a buy box module on a product details page.</span></span>

![ตัวอย่างของโมดูลกล่องการซื้อ](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="6054d-116">คุณสมบัติและช่องของกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="6054d-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="6054d-117">ในหน้ารายละเอียดของผลิตภัณฑ์ กล่องการซื้อจะแบ่งออกเป็นสองภาค: ภาคสื่อทางด้านซ้าย และภาคเนื้อหาทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="6054d-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="6054d-118">ตามค่าเริ่มต้น อัตราส่วนของความกว้างของคอลัมน์สื่อที่มีความกว้างของคอลัมน์พื้นที่เนื้อหาคือ 2:1</span><span class="sxs-lookup"><span data-stu-id="6054d-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="6054d-119">บนอุปกรณ์เคลื่อนที่ ทั้งสองภูมิภาคจะเป็นแบบซ้อนกัน เพื่อให้พื้นที่หนึ่งปรากฏอยู่ด้านล่างของภาคอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="6054d-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="6054d-120">ชุดรูปแบบสามารถใช้ในการเลือกกำหนดความกว้างคอลัมน์และการจัดอันดับการซ้อน</span><span class="sxs-lookup"><span data-stu-id="6054d-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="6054d-121">โมดูลในกล่องการซื้อแสดงชื่อ คำอธิบาย ราคา และการให้คะแนนของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6054d-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="6054d-122">นอกจากนี้ยังให้ลูกค้าเลือกผลิตภัณฑ์ย่อยที่มีแอททริบิวต์ผลิตภัณฑ์ที่แตกต่างกัน เช่น ขนาด ลักษณะ และสี</span><span class="sxs-lookup"><span data-stu-id="6054d-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="6054d-123">เมื่อเลือกผลิตภัณฑ์ย่อย คุณสมบัติอื่นๆ ในกล่องการซื้อ (ตัวอย่าง เช่น คำอธิบายผลิตภัณฑ์และรูปภาพ) จะถูกอัปเดตเพื่อให้สะท้อนถึงข้อมูลตัวแปร</span><span class="sxs-lookup"><span data-stu-id="6054d-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="6054d-124">มีการเลือกตัวเลือกปริมาณไว้ เพื่อให้ลูกค้าสามารถระบุปริมาณของสินค้าที่จะซื้อได้</span><span class="sxs-lookup"><span data-stu-id="6054d-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="6054d-125">ปริมาณสูงสุดที่สามารถซื้อได้สามารถกำหนดได้ในการตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="6054d-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="6054d-126">จากกล่องการซื้อ นอกจากนี้คุณยังสามารถทำการดำเนินการต่าง ๆ เช่น เพิ่มผลิตภัณฑ์ลงในรถเข็น เพิ่มผลิตภัณฑ์ลงในรายการโปรดของลูกค้า และเลือกสถานที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="6054d-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="6054d-127">การดำเนินการเหล่านี้สามารถดำเนินการกับผลิตภัณฑ์ หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="6054d-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="6054d-128">เมื่อต้องการเพิ่มผลิตภัณฑ์ลงในรายการโปรด ลูกค้าต้องล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="6054d-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="6054d-129">ชุดรูปแบบสามารถใช้ในการลบหรือเปลี่ยนแปลงลำดับของคุณสมบัติผลิตภัณฑ์ของกล่องการซื้อ และการควบคุมการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6054d-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="6054d-130">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="6054d-130">Module properties</span></span>

- <span data-ttu-id="6054d-131">**แท็กหัวเรื่อง** – คุณสมบัตินี้กำหนดป้ายชื่อเรื่องสำหรับชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6054d-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="6054d-132">ถ้ากล่องการซื้ออยู่ที่ด้านบนของหน้าคุณสมบัตินี้ควรถูกตั้งค่าเป็น **h1** เพื่อให้เป็นไปตามมาตรฐานการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="6054d-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

- <span data-ttu-id="6054d-133">**เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"** - คุณสมบัตินี้ช่วยให้กล่องการซื้อสามารถแสดงลิงก์ไปยังผลิตภัณฑ์ที่มีลักษณะคล้ายคลึงกับสินค้าที่ดูอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="6054d-133">**Enable "shop similar looks" recommendations** - This property allows the buy box to show links to products that look similar to the currently viewed item.</span></span> <span data-ttu-id="6054d-134">คุณลักษณะนี้พร้อมใช้งานใน Commerce รีลีส 10.0.13 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="6054d-134">This feature is available in Commerce release 10.0.13 and later.</span></span>

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="6054d-135">โมดูลที่สามารถใช้ในโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="6054d-135">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="6054d-136">**แกลเลอรีสื่อ** –โมดูลนี้ใช้ในการแสดงรูปภาพของผลิตภัณฑ์บนหน้ารายละเอียดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6054d-136">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="6054d-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลแกลเลอรี่สื่อ](media-gallery-module.md)</span><span class="sxs-lookup"><span data-stu-id="6054d-137">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="6054d-138">**ตัวเลือกร้านค้า** –โมดูลนี้แสดงรายการของร้านค้าใกล้เคียง ที่มีสินค้าพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="6054d-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="6054d-139">ซึ่งช่วยให้ผู้ใช้ป้อนสถานที่ เพื่อค้นหาร้านค้าที่อยู่ใกล้เคียง</span><span class="sxs-lookup"><span data-stu-id="6054d-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="6054d-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลตัวเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="6054d-140">For more information about this module, see [Store selector module](store-selector.md).</span></span>
- <span data-ttu-id="6054d-141">**การแชร์ทางสังคม** - สามารถเพิ่มโมดูลนี้ลงในกล่องการซื้อเพื่อให้ผู้ใช้สามารถแชร์ข้อมูลผลิตภัณฑ์บนสื่อสังคม</span><span class="sxs-lookup"><span data-stu-id="6054d-141">**Social share** - This module can be added to the buy box to allow users to share product information on social media.</span></span> <span data-ttu-id="6054d-142">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลการแชร์ทางสังคม](social-share-module.md)</span><span class="sxs-lookup"><span data-stu-id="6054d-142">For more information, see [Social share module](social-share-module.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="6054d-143">การตั้งค่าโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="6054d-143">Buy box module settings</span></span>

<span data-ttu-id="6054d-144">โมดูลกล่องการซื้อต่อไปนี้สามารถตั้งค่าคอนฟิกได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย**:</span><span class="sxs-lookup"><span data-stu-id="6054d-144">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="6054d-145">**จำนวนรายการสูงสุดในรถเข็น** – คุณสมบัตินี้ใช้เพื่อระบุจำนวนสูงสุดของสินค้าแต่ละรายการที่สามารถเพิ่มเข้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="6054d-145">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="6054d-146">ตัวอย่างเช่น ผู้ค้าปลีกอาจตั้งให้สามารถขายผลิตภัณฑ์แต่ละอย่างได้เพียง 10 ชุด ในหนึ่งธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6054d-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="6054d-147">**สินค้าคงคลัง** – สำหรับข้อมูลเกี่ยวกับวิธีการใช้การตั้งค่าสินค้าคงคลัง ให้ดูที่ [ใช้การตั้งค่าสินค้าคงคลัง](inventory-settings.md)</span><span class="sxs-lookup"><span data-stu-id="6054d-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="6054d-148">**เพิ่มลงในรถเข็น** - คุณสมบัตินี้ใช้เพื่อระบุลักษณะการทำงานหลังจากที่มีการเพิ่มสินค้าลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="6054d-148">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="6054d-149">ค่าที่เป็นไปได้คือ **นำทางไปยังรถเข็น** **อย่านำทางไปยังรถเข็น** และ **แสดงการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="6054d-149">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="6054d-150">เมื่อมีการตั้งค่าให้ **นำทางไปยังรถเข็น** ผู้ใช้จะถูกส่งไปยังหน้ารถเข็นหลังจากที่เพิ่มสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="6054d-150">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="6054d-151">เมื่อมีการตั้งค่าให้ **อย่านำทางไปยังรถเข็น** ผู้ใช้จะไม่ถูกส่งไปยังหน้ารถเข็นหลังจากที่เพิ่มสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="6054d-151">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="6054d-152">เมื่อมีการตั้งค่าให้ **แสดงการแจ้งเตือน** ผู้ใช้จะแสดงการแจ้งเตือนการยืนยันและสามารถดำเนินการเรียกดูบนหน้ารายละเอียดผลิตภัณฑ์ต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="6054d-152">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="6054d-153">รูปภาพต่อไปนี้แสดงตัวอย่างของการแจ้งยืนยันการยืนยัน "เพิ่มไปยังรถเข็น" บนไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="6054d-153">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![ตัวอย่างของโมดูลการแจ้งเตือน](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="6054d-155">การโต้ตอบ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="6054d-155">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="6054d-156">โมดูลของกล่องการซื้อจะดึงข้อมูลผลิตภัณฑ์โดยใช้ Application Programming Interface (API) ของ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="6054d-156">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="6054d-157">รหัสผลิตภัณฑ์จากหน้ารายละเอียดผลิตภัณฑ์ใช้เพื่อดึงข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6054d-157">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="6054d-158">เพิ่มโมดูลในกล่องการซื้อไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="6054d-158">Add a buy box module to a page</span></span>

<span data-ttu-id="6054d-159">การเพิ่มโมดูลกล่องการซื้อไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6054d-159">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6054d-160">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="6054d-160">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="6054d-161">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **กล่องการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="6054d-161">In the **New fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="6054d-162">ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับ **ส่วนย่อยกล่องการซื้อ** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6054d-162">Under **Fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="6054d-163">ในช่อง **แกลเลอรีสื่อ** ของโมดูลกล่องการซื้อ ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="6054d-163">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6054d-164">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **แกลเลอรีสื่อ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6054d-164">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6054d-165">ในช่อง **โมดูลตัวเลือก** ของโมดูลกล่องการซื้อ ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="6054d-165">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6054d-166">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ตัวเลือกร้านค้า** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6054d-166">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6054d-167">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="6054d-167">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6054d-168">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="6054d-168">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="6054d-169">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพล PDP** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6054d-169">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="6054d-170">ในช่อง **เนื้อหา** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="6054d-170">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6054d-171">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หน้าเริ่มต้น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6054d-171">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6054d-172">ในช่อง **หลัก** ของหน้าเริ่มต้น เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="6054d-172">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="6054d-173">ในกล่องโต้ตอบ **เลือกส่วนย่อย** ให้เลือกส่วนย่อย **ส่วนย่อยกล่องการซื้อ** ที่คุณสร้างไว้ก่อนหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6054d-173">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="6054d-174">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="6054d-174">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6054d-175">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="6054d-175">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="6054d-176">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือกเท็มเพลตของ **เท็มเพลต PDP**</span><span class="sxs-lookup"><span data-stu-id="6054d-176">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="6054d-177">ใต้ **ชื่อของหน้า** ให้ป้อน **หน้า PDP** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6054d-177">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="6054d-178">ในช่อง **หลัก** ของหน้าใหม่ เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="6054d-178">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="6054d-179">ในกล่องโต้ตอบ **เลือกส่วนย่อย** ให้เลือกส่วนย่อย **ส่วนย่อยกล่องการซื้อ** ที่คุณสร้างไว้ก่อนหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6054d-179">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="6054d-180">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="6054d-180">Save and preview the page.</span></span> <span data-ttu-id="6054d-181">เพิ่มพารามิเตอร์สตริงการสอบถาม **?productid=&lt;product id&gt;** ไปยัง URL ของหน้าแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6054d-181">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="6054d-182">ในลักษณะนี้ บริบทของผลิตภัณฑ์จะถูกใช้เพื่อโหลด และทำให้หน้าแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6054d-182">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="6054d-183">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="6054d-183">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="6054d-184">กล่องการซื้อควรปรากฏขึ้นบนหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6054d-184">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6054d-185">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6054d-185">Additional resources</span></span>

[<span data-ttu-id="6054d-186">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6054d-186">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6054d-187">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="6054d-187">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="6054d-188">โมดูลแกลเลอรี่สื่อ</span><span class="sxs-lookup"><span data-stu-id="6054d-188">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="6054d-189">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="6054d-189">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6054d-190">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="6054d-190">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6054d-191">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="6054d-191">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6054d-192">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="6054d-192">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6054d-193">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="6054d-193">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6054d-194">โมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="6054d-194">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="6054d-195">โมดูลการแชร์ทางสังคม</span><span class="sxs-lookup"><span data-stu-id="6054d-195">Social share module</span></span>](social-share-module.md)

[<span data-ttu-id="6054d-196">คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="6054d-196">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
