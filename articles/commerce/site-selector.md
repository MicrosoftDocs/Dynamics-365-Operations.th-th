---
title: โมดูลตัวเลือกไซต์
description: หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกไซต์และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055841"
---
# <a name="site-selector-module"></a><span data-ttu-id="7513d-103">โมดูลตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="7513d-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7513d-104">หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกไซต์และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7513d-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7513d-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="7513d-105">Overview</span></span>

<span data-ttu-id="7513d-106">เมื่อธุรกิจมีไซต์ที่แตกต่างกันในตลาด ภูมิภาค และตำแหน่งที่ตั้ง ผู้ใช้เว็บไซต์ต้องมีวิธีการง่ายๆ ในการสลับไปมาระหว่างไซต์ต่างๆ และเลือกไซต์การซื้อสินค้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7513d-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="7513d-107">เพื่อให้ตอบรับกับสถานการณ์จำลองนี้ โมดูลของตัวเลือกไซต์จะช่วยให้ผู้ใช้สามารถเรียกดูระหว่างไซต์ต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="7513d-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="7513d-108">โมดูลการเลือกไซต์ต้องมีการตั้งค่าคอนฟิกกับรายการไซต์ (ตลาด ภูมิภาค หรือสถานที่ตั้ง) ซึ่งผู้ใช้ไซต์สามารถเลือกดูได้</span><span class="sxs-lookup"><span data-stu-id="7513d-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="7513d-109">โมดูลตัวเลือกไซต์มีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.14</span><span class="sxs-lookup"><span data-stu-id="7513d-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="7513d-110">ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกไซต์ที่แนะนำในส่วนหัวของหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="7513d-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![ตัวอย่างของโมดูลตัวเลือกไซต์ในส่วนหัวของหน้าไซต์](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="7513d-112">คุณสมบัติของโมดูลตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="7513d-112">Site selector module properties</span></span>

| <span data-ttu-id="7513d-113">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="7513d-113">Property name</span></span> | <span data-ttu-id="7513d-114">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="7513d-114">Value</span></span>                 | <span data-ttu-id="7513d-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7513d-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="7513d-116">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="7513d-116">Heading</span></span>       | <span data-ttu-id="7513d-117">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="7513d-117">Text</span></span>                  | <span data-ttu-id="7513d-118">หัวข้อสำหรับโมดูล</span><span class="sxs-lookup"><span data-stu-id="7513d-118">The heading for the module.</span></span> |
| <span data-ttu-id="7513d-119">ตัวเลือกของไซต์</span><span class="sxs-lookup"><span data-stu-id="7513d-119">Site options</span></span>  | <span data-ttu-id="7513d-120">ชื่อ รูปภาพ URL</span><span class="sxs-lookup"><span data-stu-id="7513d-120">Name, Image, URL</span></span>      | <span data-ttu-id="7513d-121">คุณสมบัตินี้จะระบุชื่อ ลิงก์ไปยังโฮมเพจของไซต์ และรูปภาพเสริมที่จะแสดงสำหรับแต่ละไซต์ที่รวมอยู่ในโมดูล</span><span class="sxs-lookup"><span data-stu-id="7513d-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="7513d-122">รูปอาจเป็นแฟล็กหรือบางอย่างที่เป็นตัวแทนของตลาด ภูมิภาค หรือตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="7513d-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="7513d-123">เพิ่มโมดูลตัวเลือกไซต์ไปที่หน้า</span><span class="sxs-lookup"><span data-stu-id="7513d-123">Add a site selector module to a page</span></span>

<span data-ttu-id="7513d-124">โมดูลตัวเลือกไซต์สามารถเพิ่มเข้าไปใน [โมดูลของส่วนหัว](author-header-module.md) ภายใต้ช่องตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="7513d-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="7513d-125">หลังจากที่เพิ่มแล้ว คุณสามารถกำหนดส่วนหัวของโมดูลและตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="7513d-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7513d-126">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7513d-126">Additional resources</span></span>

[<span data-ttu-id="7513d-127">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="7513d-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7513d-128">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="7513d-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7513d-129">โมดูลการแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="7513d-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="7513d-130">โมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="7513d-130">Navigation menu module</span></span>](nav-menu-module.md)
