---
title: ลำดับชั้นของการค้า
description: บทความนี้อธิบายลำดับชั้นใน Dynamics 365 Commerce
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ae0e2d068d40b61bd1bd258eac3a0e4b5f399e6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791982"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="08efe-103">ลำดับชั้นของการค้า</span><span class="sxs-lookup"><span data-stu-id="08efe-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="08efe-104">บทความนี้อธิบายลำดับชั้นใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="08efe-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="08efe-105">คุณสามารถสร้างลำดับชั้นประเภทเพื่อจัดการผลิตภัณฑ์ที่คุณขายโดยผ่านช่องทาง</span><span class="sxs-lookup"><span data-stu-id="08efe-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="08efe-106">คุณสามารถใช้ลำดับชั้นของผลิตภัณฑ์เพื่อจัดประเภทหรือกลุ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="08efe-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="08efe-107">จากนั้นคุณสามารถใช้ผลิตภัณฑ์เหล่านี้เพื่อสร้างการจัดประเภทผลิตภัณฑ์และโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="08efe-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="08efe-108">คุณสามารถมอบหมายคุณลักษณะของผลิตภัณฑ์และคุณสมบัติ มอบหมายโครงสร้างการกำหนดราคา รวมถึงผลิตภัณฑ์ในโปรโมชันผลิตภัณฑ์ และใช้ผลิตภัณฑ์สำหรับการรายงาน</span><span class="sxs-lookup"><span data-stu-id="08efe-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="08efe-109">คุณสามารถสร้างลำดับชั้นประเภทหนึ่งเพื่อแสดงถึงผลิตภัณฑ์และประเภทในองค์กรของคุณทั้งหมด และจากนั้นใช้การจัดประเภทตามลำดับชั้นสำหรับวัตถุประสงค์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="08efe-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="08efe-110">อีกทางหนึ่งคือ คุณสามารถสร้างลำดับชั้นประเภทหลายรายการสำหรับวัตถุประสงค์พิเศษ เช่น การส่งเสริมการขายผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="08efe-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="08efe-111">เมื่อคุณสร้างเป็นลำดับชั้นของผลิตภัณฑ์ คุณต้องมอบหมายชนิดของการจัดประเภทตามลำดับชั้นเพื่อระบุวัตถุประสงค์ของการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="08efe-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="08efe-112">ตัวอย่างเช่น เฉพาะลำดับชั้นผลิตภัณฑ์ที่ถูกมอบหมายให้เป็นชนิด **ลำดับชั้นการนำทางการค้า** จะถูกอ้างอิงเมื่อคุณเรียกดูผลิตภัณฑ์ตามประเภทแบบออนไลน์ หรือ ในการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="08efe-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="08efe-113">ชนิดของลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="08efe-113">Hierarchy types</span></span>

<span data-ttu-id="08efe-114">ตารางต่อไปนี้แสดงรายการชนิดการจัดประเภทตามลำดับชั้นที่พร้อมใช้งานและวัตถุประสงค์ทั่วไปของแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="08efe-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="08efe-115">ชนิดของการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="08efe-115">Category hierarchy type</span></span>       | <span data-ttu-id="08efe-116">วัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="08efe-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="08efe-117">ลำดับขั้นผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="08efe-117">Product hierarchy</span></span>      | <span data-ttu-id="08efe-118">ใช้ชนิดของลำดับชั้นนี้เพื่อกำหนดลำดับชั้นของผลิตภัณฑ์โดยรวมสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="08efe-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="08efe-119">คุณสามารถใช้ชนิดลำดับชั้นสำหรับการจัดซื้อ การกำหนดราคา และโปรโมชัน รายงาน และการวางแผนการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="08efe-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="08efe-120">ลำดับชั้นของผลิตภัณฑ์เดียวเท่านั้นสามารถกำหนดชนิดของลำดับชั้นนี้</span><span class="sxs-lookup"><span data-stu-id="08efe-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="08efe-121">ลำดับชั้นเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="08efe-121">Supplemental hierarchy</span></span> | <span data-ttu-id="08efe-122">ใช้ชนิดลำดับชั้นสำหรับลำดับชั้นการจัดประเภทเพิ่มเติมใด ๆ ที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="08efe-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="08efe-123">ตัวอย่างเช่น ในฤดูใบไม้ผลิ คุณมีโปรโมชันสำหรับชุดว่ายน้ำ</span><span class="sxs-lookup"><span data-stu-id="08efe-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="08efe-124">ดังนั้น คุณรวมผลิตภัณฑ์ชุดว่ายน้ำของคุณในลำดับชั้นของประเภทที่แยกต่างหาก และใช้การกำหนดราคาโปรโมชันไปยังประเภทผลิตภัณฑ์ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="08efe-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="08efe-125">ลำดับชั้นการนำทาง</span><span class="sxs-lookup"><span data-stu-id="08efe-125">Navigation hierarchy</span></span>   | <span data-ttu-id="08efe-126">ใช้ชนิดลำดับชั้นเพื่อจัดกลุ่มและการจัดระเบียบผลิตภัณฑ์ให้เป็นประเภทเพื่อให้สามารถถูกเรียกดูผลิตภัณฑ์แบบออนไลน์ หรือ ใน POS</span><span class="sxs-lookup"><span data-stu-id="08efe-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="08efe-127">การใช้ลำดับชั้นประเภทเพื่อจัดโครงสร้างผลิตภัณฑ์ของคุณ คุณสามารถตั้งค่า และรักษาคุณลักษณะของผลิตภัณฑ์และคุณสมบัติในระดับประเภท</span><span class="sxs-lookup"><span data-stu-id="08efe-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="08efe-128">คุณลักษณะและคุณสมบัติเหล่านี้รวมถึงการตั้งค่าสำหรับมิติของผลิตภัณฑ์และการตั้งค่าของ POS</span><span class="sxs-lookup"><span data-stu-id="08efe-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="08efe-129">ผลิตภัณฑ์ใด ๆ ที่คุณมอบหมายให้กับประเภทจะสืบทอดคุณลักษณะและคุณสมบัติที่คุณกำหนด</span><span class="sxs-lookup"><span data-stu-id="08efe-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="08efe-130">คุณยังสามารถคัดลอกการตั้งค่าคุณสมบัติสำหรับผลิตภัณฑ์ใด ๆ กับหลายผลิตภัณฑ์ในประเภทที่เลือกพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="08efe-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]