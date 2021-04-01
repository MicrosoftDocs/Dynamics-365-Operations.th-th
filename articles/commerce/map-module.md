---
title: โมดูลแผนที่
description: หัวข้อนี้ครอบคลุมถึงโมดูลแผนที่และอธิบายวิธีการกำหนดค่าใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 74991a2979540dab344f39976005250637fab29c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252593"
---
# <a name="map-module"></a><span data-ttu-id="67033-103">โมดูลการแม็ป</span><span class="sxs-lookup"><span data-stu-id="67033-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="67033-104">หัวข้อนี้ครอบคลุมถึงโมดูลแผนที่และอธิบายวิธีการกำหนดค่าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="67033-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="67033-105">โมดูลแผนที่แสดงสถานที่เก็บบนแผนที่แบบโต้ตอบซึ่งแสดงโดยใช้การ [ควบคุมเว็บของ Bing Maps V8](https://docs.microsoft.com/bingmaps/v8-web-control/)</span><span class="sxs-lookup"><span data-stu-id="67033-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="67033-106">ต้องใช้คีย์ API ของ Bing Maps และต้องเพิ่มลงในหน้าพารามิเตอร์ที่ใช้ร่วมกันในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="67033-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="67033-107">โมดูลแผนที่มีมุมมองต่างๆ เช่น ถนน สภาพอากาศ และทางเดิน ผู้ใช้สามารถเลือกที่จะดูที่ตั้งแผนที่ได้</span><span class="sxs-lookup"><span data-stu-id="67033-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="67033-108">นอกจากนี้ยังอนุญาตให้มีการโต้ตอบ เช่น การซูม และการใช้สถานที่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="67033-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="67033-109">โมดูลแแผนที่จะทำงานร่วมกับโมดูลการเลือกร้านค้าเพื่อกำหนดสถานที่เก็บทางภูมิศาสตร์ของร้านค้าที่ต้องแสดงบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="67033-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="67033-110">การเลือกร้านค้าและโมดูลแผนที่จะโต้ตอบเมื่อผู้ใช้เลือกร้านค้าในหนึ่งในโมดูลเหล่านี้บนหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="67033-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="67033-111">แผนผังอาจขยายสำหรับสถานการณ์อื่นๆนอกเหนือจากการโต้ตอบกับโมดูลการเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="67033-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="67033-112">อย่างไรก็ตามต้องใช้การเลือกกำหนดโมดูล</span><span class="sxs-lookup"><span data-stu-id="67033-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="67033-113">โมดูลการแม็ปมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.13</span><span class="sxs-lookup"><span data-stu-id="67033-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="67033-114">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลแผนที่ที่ใช้ในหน้าที่ตั้งร้าน</span><span class="sxs-lookup"><span data-stu-id="67033-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![ตัวอย่างของโมดูลตัวเลือกร้านค้า](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="67033-116">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="67033-116">Module properties</span></span>

| <span data-ttu-id="67033-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="67033-117">Property name</span></span>             | <span data-ttu-id="67033-118">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="67033-118">Value</span></span>                 | <span data-ttu-id="67033-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="67033-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="67033-120">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="67033-120">Heading</span></span> | <span data-ttu-id="67033-121">Text</span><span class="sxs-lookup"><span data-stu-id="67033-121">Text</span></span> | <span data-ttu-id="67033-122">หัวข้อสำหรับโมดูล</span><span class="sxs-lookup"><span data-stu-id="67033-122">The heading for the module.</span></span> |
| <span data-ttu-id="67033-123">ตัวเลือกหมุดยึด: ไอคอนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="67033-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="67033-124">รูป</span><span class="sxs-lookup"><span data-stu-id="67033-124">Image</span></span> | <span data-ttu-id="67033-125">รูปสัญลักษณ์หมุดยึดเพื่อใช้สำหรับร้านค้าที่แสดงอยู่บนแผนที่</span><span class="sxs-lookup"><span data-stu-id="67033-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="67033-126">ตัวเลือกหมุดยึด: ไอคอนที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="67033-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="67033-127">รูป</span><span class="sxs-lookup"><span data-stu-id="67033-127">Image</span></span> | <span data-ttu-id="67033-128">รูปสัญลักษณ์หมุดยึดเพื่อใช้สำหรับร้านค้าที่เลือกบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="67033-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="67033-129">ตัวเลือกหมุดยึด: สีของไอคอนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="67033-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="67033-130">สตริงของอักขระ</span><span class="sxs-lookup"><span data-stu-id="67033-130">Character string</span></span> | <span data-ttu-id="67033-131">ค่าข้อความหรือเลขฐานสิบหกสำหรับสีของสัญลักษณ์หมุดยึดบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="67033-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="67033-132">ตัวเลือกหมุดยึด: สีของไอคอนที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="67033-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="67033-133">สตริงของอักขระ</span><span class="sxs-lookup"><span data-stu-id="67033-133">Character string</span></span> | <span data-ttu-id="67033-134">ค่าข้อความหรือเลขฐานสิบหกสำหรับสีของสัญลักษณ์หมุดยึดที่เลือกบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="67033-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="67033-135">แสดงดัชนี</span><span class="sxs-lookup"><span data-stu-id="67033-135">Show index</span></span> | <span data-ttu-id="67033-136">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="67033-136">**True** or **False**</span></span> | <span data-ttu-id="67033-137">ถ้าคุณสมบัตินี้ได้รับการตั้งค่าเป็น **จริง** สัญลักษณ์หมุดยึดทั้งหมดที่บ่งชี้ถึงร้านค้าจะแสดงดัชนี</span><span class="sxs-lookup"><span data-stu-id="67033-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="67033-138">ดัชนีนี้จะตรงกับดัชนีในมุมมองรายการที่จะแสดงโมดูลของตัวเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="67033-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="67033-139">เพิ่ม URL การแม็ปที่อนุญาตให้กับคำสั่งนโยบายความปลอดภัยของเนื้อหาของไซต์</span><span class="sxs-lookup"><span data-stu-id="67033-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="67033-140">สำหรับโมดูลแผนที่เพื่อโต้ตอบกับ Bing Maps คุณต้องตรวจสอบให้แน่ใจว่าได้อนุญาตให้มีการแม็ป URL ต่อไปนี้ตามนโยบายความปลอดภัยเนื้อหาของไซต์ (CSP) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="67033-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="67033-141">การตั้งค่านี้ดำเนินการในโปรแกรมสร้างไซต์ Commerce โดยการเพิ่ม URL ที่อนุญาตให้กับคำสั่ง CSP ไซต์ต่างๆ (ตัวอย่างเช่น **img-src**)</span><span class="sxs-lookup"><span data-stu-id="67033-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="67033-142">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [นโยบายความปลอดภัยของเนื้อหา](manage-csp.md)</span><span class="sxs-lookup"><span data-stu-id="67033-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="67033-143">ไปที่คำสั่ง **connect-src** เพิ่ม **&#42;bing.com**</span><span class="sxs-lookup"><span data-stu-id="67033-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="67033-144">ไปที่คำสั่ง **img-src** เพิ่ม **&#42;virtualearth.net**</span><span class="sxs-lookup"><span data-stu-id="67033-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="67033-145">ไปที่คำสั่ง **script-src** เพิ่ม **&#42;.bing.com, &#42;.virtualearth.net**</span><span class="sxs-lookup"><span data-stu-id="67033-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="67033-146">ไปที่คำสั่ง **script style-src** เพิ่ม **&#42;.bing.com**</span><span class="sxs-lookup"><span data-stu-id="67033-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="67033-147">เพิ่มโมดูลแผนที่ไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="67033-147">Add a map module to a page</span></span>

<span data-ttu-id="67033-148">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกโมดูลแผนที่บนหน้า โปรดดูที่ [โมดูลการเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="67033-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="67033-149">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="67033-149">Additional resources</span></span>

[<span data-ttu-id="67033-150">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="67033-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="67033-151">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="67033-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="67033-152">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="67033-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="67033-153">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="67033-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="67033-154">จัดการ Bing Maps สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="67033-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="67033-155">การควบคุมเว็บของ Bing Maps V8</span><span class="sxs-lookup"><span data-stu-id="67033-155">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]