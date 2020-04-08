---
title: โมดูลตัวเลือกร้านค้า
description: หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกร้านค้า และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157351"
---
# <a name="store-selector-module"></a><span data-ttu-id="8cace-103">โมดูลตัวเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="8cace-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8cace-104">หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกร้านค้า และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cace-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8cace-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="8cace-105">Overview</span></span>

<span data-ttu-id="8cace-106">โมดูลตัวเลือกร้านค้าใช้สำหรับสถานการณ์จำลองของลูกค้า "ซื้อออนไลน์ เบิกสินค้าในร้านค้า"" (BOPIS)</span><span class="sxs-lookup"><span data-stu-id="8cace-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="8cace-107">ซึ่งแสดงรายการของร้านค้าที่มีผลิตภัณฑ์อยู่สำหรับการเบิกสินค้า รวมทั้งชั่วโมงทำการของร้านค้าและสินค้าคงคลังของผลิตภัณฑ์สำหรับร้านค้าแต่ละร้าน</span><span class="sxs-lookup"><span data-stu-id="8cace-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="8cace-108">โมดูลตัวเลือกร้านค้าต้องใช้บริบทของผลิตภัณฑ์และที่ตั้งการค้นหาเพื่อค้นหาร้านค้า</span><span class="sxs-lookup"><span data-stu-id="8cace-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="8cace-109">ในกรณีที่ไม่มีสถานที่การค้นหา จะมีการตั้งค่าเริ่มต้นให้กับสถานที่เบราว์เซอร์ของลูกค้า หากลูกค้าให้ความยินยอม</span><span class="sxs-lookup"><span data-stu-id="8cace-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="8cace-110">โมดูลมีช่องป้อนข้อมูลซึ่งช่วยให้ลูกค้าสามารถป้อนสถานที่ (รหัสไปรษณีย์ หรือเมืองและรัฐ) เพื่อค้นหาร้านค้าที่อยู่ใกล้เคียง</span><span class="sxs-lookup"><span data-stu-id="8cace-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="8cace-111">โมดูลตัวเลือกร้านค้าทำงานร่วมกับ Application Programming Interface กำหนดพิกัดทางภูมิศาสตร์ของ Bing Maps (API) เพื่อแปลงสถานที่ที่ลูกค้าป้อนให้เป็นละติจูดและลองจิจูด</span><span class="sxs-lookup"><span data-stu-id="8cace-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="8cace-112">ต้องใช้คีย์ API ของ Bing Maps และต้องเพิ่มลงในหน้าพารามิเตอร์ที่ใช้ร่วมกันของ Commerce ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cace-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8cace-113">สามารถเพิ่มโมดูลตัวเลือกร้านค้าเข้าไปในโมดูลกล่องการซื้อบนหน้ารายละเอียดผลิตภัณฑ์ (PDP) เพื่อแสดงร้านค้าที่มีผลิตภัณฑ์พร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="8cace-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="8cace-114">นอกจากนี้ ยังสามารถเพิ่มเข้ากับโมดูลรถเข็นได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8cace-114">It can also be added to a cart module.</span></span> <span data-ttu-id="8cace-115">เมื่อเพิ่มไปที่โมดูลรถเข็น โมดูลตัวเลือกร้านค้าจะแสดงตัวเลือกการเบิกสินค้าสำหรับสินค้าในรายการในรถเข็นแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8cace-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="8cace-116">นอกจากนี้ ด้วยการเขียนโค้ดแบบกำหนดเอง คุณยังสามารถเพิ่มโมดูลไปยังหน้าหรือโมดูลอื่นๆ ผ่านส่วนขยายและการกำหนดเองได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8cace-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="8cace-117">สำหรับสถานการณ์จำลอง BOPIS ที่จะทำงาน ควรตั้งค่าคอนฟิกผลิตภัณฑ์ด้วยโหมดการจัดส่ง "การเบิกสินค้าของลูกค้า"</span><span class="sxs-lookup"><span data-stu-id="8cace-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="8cace-118">มิฉะนั้น จะไม่มีการแสดงโมดูลบนหน้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8cace-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="8cace-119">สำหรับรายละเอียดเกี่ยวกับวิธีการตั้งค่าคอนฟิกโหมดการจัดส่ง ให้ดูที่ [ตั้งค่าโหมดการจัดส่ง](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)</span><span class="sxs-lookup"><span data-stu-id="8cace-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="8cace-120">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกร้านค้าที่ใช้ใน PDP</span><span class="sxs-lookup"><span data-stu-id="8cace-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![ตัวอย่างของโมดูลตัวเลือกร้านค้า](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="8cace-122">การใช้งานโมดูลตัวเลือกร้านค้าในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="8cace-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="8cace-123">สามารถใช้โมดูลตัวเลือกร้านค้าในหน้ารายละเอียดผลิตภัณฑ์ (PDP) เพื่อค้นหาร้านค้าใกล้เคียงที่มีผลิตภัณฑ์พร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="8cace-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="8cace-124">สามารถใช้โมดูลตัวเลือกร้านค้าในหน้ารถเข็น เพื่อค้นหาร้านค้าใกล้เคียงที่ซึ่งมีผลิตภัณฑ์ในรถเข็นพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="8cace-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="8cace-125">คุณสมบัติของโมดูลตัวเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="8cace-125">Store selector module properties</span></span>

| <span data-ttu-id="8cace-126">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="8cace-126">Property name</span></span>             | <span data-ttu-id="8cace-127">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="8cace-127">Value</span></span>                 | <span data-ttu-id="8cace-128">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8cace-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="8cace-129">ค้นหารัศมี</span><span class="sxs-lookup"><span data-stu-id="8cace-129">Search radius</span></span> | <span data-ttu-id="8cace-130">ลำดับ</span><span class="sxs-lookup"><span data-stu-id="8cace-130">Number</span></span> | <span data-ttu-id="8cace-131">กำหนดรัศมีในการค้นหาสำหรับร้านค้าในหน่วยไมล์</span><span class="sxs-lookup"><span data-stu-id="8cace-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="8cace-132">ถ้าไม่มีการระบุค่า จะมีการใช้รัศมีการค้นหาเริ่มต้นเป็น 50 ไมล์</span><span class="sxs-lookup"><span data-stu-id="8cace-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="8cace-133">ข้อกำหนดในการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="8cace-133">Terms of Service</span></span> | <span data-ttu-id="8cace-134">URL</span><span class="sxs-lookup"><span data-stu-id="8cace-134">URL</span></span>    |  <span data-ttu-id="8cace-135">จำเป็นต้องมี URL เงื่อนไขของการให้บริการสำหรับบริการ Bing Maps</span><span class="sxs-lookup"><span data-stu-id="8cace-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="8cace-136">เพิ่มโมดูลตัวเลือกร้านค้าไปที่หน้า</span><span class="sxs-lookup"><span data-stu-id="8cace-136">Add a store selector module to a page</span></span>

<span data-ttu-id="8cace-137">โมดูลตัวเลือกร้านค้าต้องมีบริบทของผลิตภัณฑ์ เพื่อให้สามารถใช้งานได้ภายในโมดูลกล่องการซื้อและโมดูลรถเข็นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8cace-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="8cace-138">โมดูลตัวเลือกร้านค้าไม่ทำงานภายนอกโมดูลเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8cace-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="8cace-139">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเพิ่มโมดูลตัวเลือกร้านค้าไปยังโมดูลกล่องการซื้อ ให้ดูที่ [โมดูลกล่องการซื้อ](add-buy-box.md)</span><span class="sxs-lookup"><span data-stu-id="8cace-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="8cace-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเพิ่มโมดูลตัวเลือกร้านค้าไปยังโมดูลกล่องรถเข็น ให้ดูที่ [โมดูลรถเข็น](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="8cace-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8cace-141">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8cace-141">Additional resources</span></span>

[<span data-ttu-id="8cace-142">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8cace-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8cace-143">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="8cace-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8cace-144">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="8cace-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8cace-145">การแนะนำการใช้งานแบบด่วนของ PDP</span><span class="sxs-lookup"><span data-stu-id="8cace-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="8cace-146">การแนะนำการใช้งานแบบด่วนของรถเข็นและการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="8cace-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="8cace-147">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="8cace-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
