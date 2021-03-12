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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ed00836c435bd391e5edef1f6a99889c80f45211
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985597"
---
# <a name="site-selector-module"></a><span data-ttu-id="8ff30-103">โมดูลตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="8ff30-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ff30-104">หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกไซต์และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8ff30-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ff30-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="8ff30-105">Overview</span></span>

<span data-ttu-id="8ff30-106">เมื่อธุรกิจมีไซต์ที่แตกต่างกันในตลาด ภูมิภาค และตำแหน่งที่ตั้ง ผู้ใช้เว็บไซต์ต้องมีวิธีการง่ายๆ ในการสลับไปมาระหว่างไซต์ต่างๆ และเลือกไซต์การซื้อสินค้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8ff30-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="8ff30-107">เพื่อให้ตอบรับกับสถานการณ์จำลองนี้ โมดูลของตัวเลือกไซต์จะช่วยให้ผู้ใช้สามารถเรียกดูระหว่างไซต์ต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="8ff30-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="8ff30-108">โมดูลการเลือกไซต์ต้องมีการตั้งค่าคอนฟิกกับรายการไซต์ (ตลาด ภูมิภาค หรือสถานที่ตั้ง) ซึ่งผู้ใช้ไซต์สามารถเลือกดูได้</span><span class="sxs-lookup"><span data-stu-id="8ff30-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="8ff30-109">โมดูลตัวเลือกไซต์มีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.14</span><span class="sxs-lookup"><span data-stu-id="8ff30-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="8ff30-110">ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกไซต์ที่แนะนำในส่วนหัวของหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="8ff30-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![ตัวอย่างของโมดูลตัวเลือกไซต์ในส่วนหัวของหน้าไซต์](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="8ff30-112">คุณสมบัติของโมดูลตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="8ff30-112">Site selector module properties</span></span>

| <span data-ttu-id="8ff30-113">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="8ff30-113">Property name</span></span> | <span data-ttu-id="8ff30-114">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="8ff30-114">Value</span></span>                 | <span data-ttu-id="8ff30-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8ff30-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="8ff30-116">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="8ff30-116">Heading</span></span>       | <span data-ttu-id="8ff30-117">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="8ff30-117">Text</span></span>                  | <span data-ttu-id="8ff30-118">หัวข้อสำหรับโมดูล</span><span class="sxs-lookup"><span data-stu-id="8ff30-118">The heading for the module.</span></span> |
| <span data-ttu-id="8ff30-119">ตัวเลือกของไซต์</span><span class="sxs-lookup"><span data-stu-id="8ff30-119">Site options</span></span>  | <span data-ttu-id="8ff30-120">ชื่อ รูปภาพ URL</span><span class="sxs-lookup"><span data-stu-id="8ff30-120">Name, Image, URL</span></span>      | <span data-ttu-id="8ff30-121">คุณสมบัตินี้จะระบุชื่อ ลิงก์ไปยังโฮมเพจของไซต์ และรูปภาพเสริมที่จะแสดงสำหรับแต่ละไซต์ที่รวมอยู่ในโมดูล</span><span class="sxs-lookup"><span data-stu-id="8ff30-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="8ff30-122">รูปอาจเป็นแฟล็กหรือบางอย่างที่เป็นตัวแทนของตลาด ภูมิภาค หรือตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="8ff30-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="8ff30-123">เพิ่มโมดูลตัวเลือกไซต์ไปที่หน้า</span><span class="sxs-lookup"><span data-stu-id="8ff30-123">Add a site selector module to a page</span></span>

<span data-ttu-id="8ff30-124">โมดูลตัวเลือกไซต์สามารถเพิ่มเข้าไปใน [โมดูลของส่วนหัว](author-header-module.md) ภายใต้ช่องตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="8ff30-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="8ff30-125">หลังจากที่เพิ่มแล้ว คุณสามารถกำหนดส่วนหัวของโมดูลและตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="8ff30-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ff30-126">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8ff30-126">Additional resources</span></span>

[<span data-ttu-id="8ff30-127">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="8ff30-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8ff30-128">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="8ff30-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8ff30-129">โมดูลการแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="8ff30-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="8ff30-130">โมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="8ff30-130">Navigation menu module</span></span>](nav-menu-module.md)
