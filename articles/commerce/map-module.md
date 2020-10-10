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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d2cbc67a186a76647a4f7ddc7942b15d3e469ece
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817217"
---
# <a name="map-module"></a><span data-ttu-id="10ab8-103">โมดูลแผนที่</span><span class="sxs-lookup"><span data-stu-id="10ab8-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="10ab8-104">หัวข้อนี้ครอบคลุมถึงโมดูลแผนที่และอธิบายวิธีการกำหนดค่าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="10ab8-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="10ab8-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="10ab8-105">Overview</span></span>

<span data-ttu-id="10ab8-106">โมดูลแผนที่แสดงสถานที่เก็บบนแผนที่แบบโต้ตอบซึ่งแสดงโดยใช้การ [ควบคุมเว็บของ Bing Maps V8](https://docs.microsoft.com/bingmaps/v8-web-control/)</span><span class="sxs-lookup"><span data-stu-id="10ab8-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="10ab8-107">ต้องใช้คีย์ API ของ Bing Maps และต้องเพิ่มลงในหน้าพารามิเตอร์ที่ใช้ร่วมกันในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="10ab8-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="10ab8-108">โมดูลแผนที่มีมุมมองต่างๆ เช่น ถนน สภาพอากาศ และทางเดิน ผู้ใช้สามารถเลือกที่จะดูที่ตั้งแผนที่ได้</span><span class="sxs-lookup"><span data-stu-id="10ab8-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="10ab8-109">นอกจากนี้ยังอนุญาตให้มีการโต้ตอบ เช่น การซูม และการใช้สถานที่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="10ab8-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="10ab8-110">โมดูลแแผนที่จะทำงานร่วมกับโมดูลการเลือกร้านค้าเพื่อกำหนดสถานที่เก็บทางภูมิศาสตร์ของร้านค้าที่ต้องแสดงบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="10ab8-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="10ab8-111">การเลือกร้านค้าและโมดูลแผนที่จะโต้ตอบเมื่อผู้ใช้เลือกร้านค้าในหนึ่งในโมดูลเหล่านี้บนหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="10ab8-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="10ab8-112">แผนผังอาจขยายสำหรับสถานการณ์อื่นๆนอกเหนือจากการโต้ตอบกับโมดูลการเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="10ab8-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="10ab8-113">อย่างไรก็ตามต้องใช้การเลือกกำหนดโมดูล</span><span class="sxs-lookup"><span data-stu-id="10ab8-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="10ab8-114">โมดูลการแม็ปมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.13</span><span class="sxs-lookup"><span data-stu-id="10ab8-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="10ab8-115">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลแผนที่ที่ใช้ในหน้าที่ตั้งร้าน</span><span class="sxs-lookup"><span data-stu-id="10ab8-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![ตัวอย่างของโมดูลตัวเลือกร้านค้า](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="10ab8-117">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="10ab8-117">Module properties</span></span>

| <span data-ttu-id="10ab8-118">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="10ab8-118">Property name</span></span>             | <span data-ttu-id="10ab8-119">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="10ab8-119">Value</span></span>                 | <span data-ttu-id="10ab8-120">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="10ab8-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="10ab8-121">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="10ab8-121">Heading</span></span> | <span data-ttu-id="10ab8-122">Text</span><span class="sxs-lookup"><span data-stu-id="10ab8-122">Text</span></span> | <span data-ttu-id="10ab8-123">หัวข้อสำหรับโมดูล</span><span class="sxs-lookup"><span data-stu-id="10ab8-123">The heading for the module.</span></span> |
| <span data-ttu-id="10ab8-124">ตัวเลือกหมุดยึด: ไอคอนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="10ab8-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="10ab8-125">รูป</span><span class="sxs-lookup"><span data-stu-id="10ab8-125">Image</span></span> | <span data-ttu-id="10ab8-126">รูปสัญลักษณ์หมุดยึดเพื่อใช้สำหรับร้านค้าที่แสดงอยู่บนแผนที่</span><span class="sxs-lookup"><span data-stu-id="10ab8-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="10ab8-127">ตัวเลือกหมุดยึด: ไอคอนที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="10ab8-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="10ab8-128">รูป</span><span class="sxs-lookup"><span data-stu-id="10ab8-128">Image</span></span> | <span data-ttu-id="10ab8-129">รูปสัญลักษณ์หมุดยึดเพื่อใช้สำหรับร้านค้าที่เลือกบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="10ab8-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="10ab8-130">ตัวเลือกหมุดยึด: สีของไอคอนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="10ab8-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="10ab8-131">สตริงของอักขระ</span><span class="sxs-lookup"><span data-stu-id="10ab8-131">Character string</span></span> | <span data-ttu-id="10ab8-132">ค่าข้อความหรือเลขฐานสิบหกสำหรับสีของสัญลักษณ์หมุดยึดบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="10ab8-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="10ab8-133">ตัวเลือกหมุดยึด: สีของไอคอนที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="10ab8-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="10ab8-134">สตริงของอักขระ</span><span class="sxs-lookup"><span data-stu-id="10ab8-134">Character string</span></span> | <span data-ttu-id="10ab8-135">ค่าข้อความหรือเลขฐานสิบหกสำหรับสีของสัญลักษณ์หมุดยึดที่เลือกบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="10ab8-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="10ab8-136">แสดงดัชนี</span><span class="sxs-lookup"><span data-stu-id="10ab8-136">Show index</span></span> | <span data-ttu-id="10ab8-137">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="10ab8-137">**True** or **False**</span></span> | <span data-ttu-id="10ab8-138">ถ้าคุณสมบัตินี้ได้รับการตั้งค่าเป็น **จริง** สัญลักษณ์หมุดยึดทั้งหมดที่บ่งชี้ถึงร้านค้าจะแสดงดัชนี</span><span class="sxs-lookup"><span data-stu-id="10ab8-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="10ab8-139">ดัชนีนี้จะตรงกับดัชนีในมุมมองรายการที่จะแสดงโมดูลของตัวเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="10ab8-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="10ab8-140">เพิ่ม URL การแม็ปที่อนุญาตให้กับคำสั่งนโยบายความปลอดภัยของเนื้อหาของไซต์</span><span class="sxs-lookup"><span data-stu-id="10ab8-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="10ab8-141">สำหรับโมดูลแผนที่เพื่อโต้ตอบกับ Bing Maps คุณต้องตรวจสอบให้แน่ใจว่าได้อนุญาตให้มีการแม็ป URL ต่อไปนี้ (หรือที่เรียกอีกอย่างว่า "ผู้ใช้ที่ได้รับอนุญาต") ตามนโยบายความปลอดภัยเนื้อหาของไซต์ (CSP) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="10ab8-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="10ab8-142">การตั้งค่านี้ดำเนินการในโปรแกรมสร้างไซต์ Commerce โดยการเพิ่ม URL ที่อนุญาตให้กับคำสั่ง CSP ไซต์ต่างๆ (ตัวอย่างเช่น **img-src**)</span><span class="sxs-lookup"><span data-stu-id="10ab8-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="10ab8-143">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [นโยบายความปลอดภัยของเนื้อหา](manage-csp.md)</span><span class="sxs-lookup"><span data-stu-id="10ab8-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="10ab8-144">ไปที่คำสั่ง **connect-src** เพิ่ม **&#42;bing.com**</span><span class="sxs-lookup"><span data-stu-id="10ab8-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="10ab8-145">ไปที่คำสั่ง **img-src** เพิ่ม **&#42;virtualearth.net**</span><span class="sxs-lookup"><span data-stu-id="10ab8-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="10ab8-146">ไปที่คำสั่ง **script-src** เพิ่ม **&#42;.bing.com, &#42;.virtualearth.net**</span><span class="sxs-lookup"><span data-stu-id="10ab8-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="10ab8-147">ไปที่คำสั่ง **script style-src** เพิ่ม **&#42;.bing.com**</span><span class="sxs-lookup"><span data-stu-id="10ab8-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="10ab8-148">เพิ่มโมดูลแผนที่ไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="10ab8-148">Add a map module to a page</span></span>

<span data-ttu-id="10ab8-149">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกโมดูลแผนที่บนหน้า โปรดดูที่ [โมดูลการเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="10ab8-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="10ab8-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="10ab8-150">Additional resources</span></span>

[<span data-ttu-id="10ab8-151">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="10ab8-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="10ab8-152">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="10ab8-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="10ab8-153">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="10ab8-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="10ab8-154">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="10ab8-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="10ab8-155">จัดการ Bing Maps สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="10ab8-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="10ab8-156">การควบคุมเว็บของ Bing Maps V8</span><span class="sxs-lookup"><span data-stu-id="10ab8-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
