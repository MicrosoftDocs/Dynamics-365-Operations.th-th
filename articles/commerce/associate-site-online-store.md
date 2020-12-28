---
title: เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์
description: หัวข้อนี้อธิบายถึงวิธีการผูกไซต์ Microsoft Dynamics 365 Commerce ของคุณกับร้านค้าออนไลน์หนึ่งแห่งขึ้นไป
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6ae02d34499275fa303358f7dae4d3835d438e1
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517341"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="a8780-103">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="a8780-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8780-104">หัวข้อนี้อธิบายถึงวิธีการผูกไซต์ Microsoft Dynamics 365 Commerce ของคุณกับร้านค้าออนไลน์หนึ่งแห่งขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="a8780-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="a8780-105">หลังจากที่คุณได้เตรียมใช้งานสภาพแวดล้อมอีคอมเมิร์ซ Dynamics 365 Commerce ของคุณ โดยใช้พอร์ทัล Microsoft Dynamics Lifecycle Services (LCS) คุณพร้อมที่จะสร้างเว็บไซต์อีคอมเมิร์ซแรกของคุณ</span><span class="sxs-lookup"><span data-stu-id="a8780-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="a8780-106">เนื่องจากเป็นส่วนหนึ่งของการสร้างไซต์เริ่มต้น คุณเชื่อมโยงไซต์กับร้านค้าออนไลน์ที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a8780-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="a8780-107">ขั้นตอนนี้ผูกไซต์กับช่องทางออนไลน์ และให้ไซต์แสดงลำดับชั้นการนำทาง ผลิตภัณฑ์ ประเภท ราคา ตัวเลือกการจัดส่ง และข้อมูลอื่นๆ ที่คุณได้กำหนดไว้ในร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="a8780-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="a8780-108">เมื่อต้องการสร้างไซต์ใหม่และเชื่อมโยงร้านค้าออนไลน์กับไซต์ ใน LCS เลือกลิงค์สำหรับสภาพแวดล้อมการสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="a8780-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="a8780-109">หลังจากนั้น บนเพจสำหรับสภาพแวดล้อมการสร้างไซต์ ให้เลือก **ไซต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a8780-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="a8780-110">ในกล่องโต้ตอบ **ไซต์ใหม่** คุณต้องระบุข้อมูลพื้นฐานเกี่ยวกับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a8780-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="a8780-111">สำหรับคำอธิบายที่สมบูรณ์ของข้อมูลที่คุณต้องระบุ ดูที่ [การสร้างไซต์อีคอมเมิร์ซใหม่](create-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="a8780-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="a8780-112">หลังจากที่สร้างไซต์แล้ว คุณสามารถตรวจสอบว่ามีการเชื่อมโยงกับร้านค้าออนไลน์ของคุณ โดยเลือกแท็บ **ผลิตภัณฑ์** คุณควรเห็นการจัดประเภทของผลิตภัณฑ์ที่ถูกปันส่วนให้กับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="a8780-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="a8780-113">นอกจากนี้คุณยังสามารถใช้ฟิลด์แบบหล่นลงที่ด้านบนซ้ายของเพจ เพื่อเข้าถึงผลิตภัณฑ์ตามประเภท</span><span class="sxs-lookup"><span data-stu-id="a8780-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8780-114">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a8780-114">Additional resources</span></span>

[<span data-ttu-id="a8780-115">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="a8780-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a8780-116">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="a8780-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a8780-117">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="a8780-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a8780-118">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="a8780-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a8780-119">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="a8780-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a8780-120">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="a8780-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a8780-121">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a8780-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a8780-122">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="a8780-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a8780-123">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="a8780-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a8780-124">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="a8780-124">Enable location-based store detection</span></span>](enable-store-detection.md)
