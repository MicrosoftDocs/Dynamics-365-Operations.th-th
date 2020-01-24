---
title: ภาพรวมของร้านค้าออนไลน์
description: หัวข้อนี้จะกล่าวถึงร้านค้าออนไลน์ใน Dynamics 365 Commerce
author: stuharg
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bicyclingfool
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: df474776ed30f6011a0f317d840349c513f3bc8c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914736"
---
# <a name="online-store-overview"></a><span data-ttu-id="66155-103">ภาพรวมของร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="66155-103">Online store overview</span></span>
[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="66155-104">หัวข้อนี้จะแนะนำแนวคิดของร้านค้าออนไลน์และอธิบายวิธีการใช้ร้านค้าออนไลน์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="66155-104">This topic introduces the concept of an online store and explains how online stores are used in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="66155-105">นอกจากนี้ ยังมีการเชื่อมโยงไปยังข้อมูลเพิ่มเติมเกี่ยวกับร้านค้าออนไลน์และข้อมูลเกี่ยวกับวิธีการตั้งค่าร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="66155-105">It also provides a link to more information about online stores and information about how to set up an online store.</span></span>

<span data-ttu-id="66155-106">ก่อนที่คุณจะสามารถสร้างไซต์ของคุณใน Dynamics 365 Commerce ต้องสร้างร้านค้าออนไลน์อย่างน้อยหนึ่งร้าน</span><span class="sxs-lookup"><span data-stu-id="66155-106">Before you can build your site in Dynamics 365 Commerce, at least one online store must be set up.</span></span> <span data-ttu-id="66155-107">ใน Dynamics 365 Commerce คุณใช้ร้านค้าออนไลน์เพื่อสร้างผลิตภัณฑ์ การกำหนดราคา ภาษา วิธีการชำระเงิน โหมดการจัดส่ง ศูนย์เติมสินค้า และด้านอื่นๆ ของประสบการณ์ออนไลน์ที่ควรจะพร้อมใช้งานสำหรับลูกค้าของคุณ.</span><span class="sxs-lookup"><span data-stu-id="66155-107">In Dynamics 365 Commerce, you use an online store to establish the products, pricing, languages, payment methods, delivery modes, fulfillment centers, and other aspects of the online experience that should be available to your customers.</span></span>

<span data-ttu-id="66155-108">มีเพียงร้านค้าออนไลน์เดียวเท่านั้นที่จะได้รับการตั้งค่า ก่อนที่คุณจะสามารถเริ่มต้นใช้งาน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="66155-108">Only one online store has to be set up before you can get started with Dynamics 365 Commerce.</span></span> <span data-ttu-id="66155-109">อย่างไรก็ตาม ไซต์ Dynamics 365 Commerce เดียวสามารถให้ประสบการณ์การใช้งานแบบออนไลน์สำหรับร้านค้าออนไลน์หลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="66155-109">However, a single Dynamics 365 Commerce site can provide the online experience for multiple online stores.</span></span> <span data-ttu-id="66155-110">ตัวอย่างเช่น ถ้าร้านค้าออนไลน์หลายแห่งมีการตั้งค่าเพื่อสนับสนุนภูมิภาคทางภูมิศาสตร์ที่แตกต่างกัน หน้าชุดเดียวสามารถใช้เพื่อให้ประสบการณ์ที่ไม่ซ้ำกันที่กำหนดโดยแต่ละร้านค้า</span><span class="sxs-lookup"><span data-stu-id="66155-110">For example, if multiple online stores are set up to support different geographical regions, a single set of pages can be used to provide the unique experiences that are defined by each store.</span></span> <span data-ttu-id="66155-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกไซต์เพื่อสนับสนุนร้านค้าออนไลน์หลายแห่ง ให้ดู [เชื่อมโยงไซต์แบบออนไลน์กับช่องทาง](associate-site-online-store.md)</span><span class="sxs-lookup"><span data-stu-id="66155-111">For more information about how to configure a site to support multiple online stores, see [Associate an online site with a channel](associate-site-online-store.md).</span></span>

<span data-ttu-id="66155-112">หลังจากตั้งค่าร้านค้าออนไลน์แล้ว จะสามารถเชื่อมโยงกับไซต์ Dynamics 365 Commerce ที่จะทำหน้าที่เป็นหน้าร้านออนไลน์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="66155-112">After an online store is set up, it can be associated with the Dynamics 365 Commerce site that will serve as your online storefront.</span></span> <span data-ttu-id="66155-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับร้านค้าออนไลน์และวิธีการตั้งค่า ให้ดูที่ [การตั้งค่าร้านค้าออนไลน์](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores)</span><span class="sxs-lookup"><span data-stu-id="66155-113">For more information about online stores and how to set them up, see [Set up online stores](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66155-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="66155-114">Additional resources</span></span>

[<span data-ttu-id="66155-115">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="66155-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="66155-116">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="66155-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="66155-117">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="66155-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="66155-118">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="66155-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="66155-119">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="66155-119">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="66155-120">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="66155-120">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="66155-121">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="66155-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
