---
title: "ลำดับชั้นการขายปลีก"
description: "บทความนี้อธิบายถึงลำดับชั้นการขายปลีกใน Microsoft Dynamics 365 for Retail"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 817696566473bc5f31a7ff11c04291351dfd4764
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="retail-hierarchies"></a><span data-ttu-id="5ee00-103">ลำดับชั้นการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5ee00-103">Retail hierarchies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5ee00-104">บทความนี้อธิบายถึงลำดับชั้นการขายปลีกใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="5ee00-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="5ee00-105">คุณสามารถสร้างลำดับชั้นประเภทการขายปลีกเพื่อจัดการผลิตภัณฑ์ที่คุณขายโดยผ่านช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5ee00-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="5ee00-106">คุณสามารถใช้ลำดับชั้นของผลิตภัณฑ์ขายปลีกเพื่อจัดประเภทหรือกลุ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5ee00-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="5ee00-107">จากนั้นคุณสามารถใช้ผลิตภัณฑ์เหล่านี้เพื่อสร้างการจัดประเภทผลิตภัณฑ์และโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="5ee00-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="5ee00-108">คุณสามารถมอบหมายคุณลักษณะของผลิตภัณฑ์และคุณสมบัติ มอบหมายโครงสร้างการกำหนดราคา รวมถึงผลิตภัณฑ์ในโปรโมชันผลิตภัณฑ์ และใช้ผลิตภัณฑ์สำหรับการรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ee00-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="5ee00-109">คุณสามารถสร้างลำดับชั้นประเภทขายปลีกหนึ่งเพื่อแสดงถึงผลิตภัณฑ์และประเภทในองค์กรของคุณทั้งหมด และจากนั้นใช้การจัดประเภทตามลำดับชั้นสำหรับวัตถุประสงค์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5ee00-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="5ee00-110">อีกทางหนึ่งคือ คุณสามารถสร้างลำดับชั้นประเภทการขายปลีกหลายรายการสำหรับวัตถุประสงค์พิเศษ เช่น การส่งเสริมการขายผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5ee00-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="5ee00-111">เมื่อคุณสร้างเป็นลำดับชั้นของผลิตภัณฑ์ขายปลีก คุณต้องมอบหมายชนิดของการจัดประเภทตามลำดับชั้นเพื่อระบุวัตถุประสงค์ของการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="5ee00-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="5ee00-112">ตัวอย่างเช่น เฉพาะลำดับชั้นผลิตภัณฑ์ที่ถูกมอบหมายให้เป็นชนิด **ลำดับชั้นการนำทางการขายปลีก** จะถูกอ้างอิงเมื่อคุณเรียกดูผลิตภัณฑ์ตามประเภทแบบออนไลน์ หรือ ในการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="5ee00-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="5ee00-113">ชนิดลำดับชั้นการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5ee00-113">Retail hierarchy types</span></span>
<span data-ttu-id="5ee00-114">ตารางต่อไปนี้แสดงรายการชนิดการจัดประเภทการขายปลีกตามลำดับชั้นที่พร้อมใช้งานและวัตถุประสงค์ทั่วไปของแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="5ee00-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="5ee00-115">ชนิดของการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="5ee00-115">Category hierarchy type</span></span>       | <span data-ttu-id="5ee00-116">วัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="5ee00-116">Purpose</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee00-117">ลำดับชั้นของผลิตภัณฑ์เพื่อการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5ee00-117">Retail product hierarchy</span></span>      | <span data-ttu-id="5ee00-118">ใช้ชนิดของลำดับชั้นนี้เพื่อกำหนดลำดับชั้นของผลิตภัณฑ์โดยรวมสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ee00-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="5ee00-119">คุณสามารถใช้ชนิดลำดับชั้นสำหรับการจัดซื้อ การกำหนดราคา และโปรโมชัน รายงาน และการวางแผนการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="5ee00-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="5ee00-120">ลำดับชั้นของผลิตภัณฑ์ขายปลีกเดียวเท่านั้นสามารถกำหนดชนิดของลำดับชั้นนี้</span><span class="sxs-lookup"><span data-stu-id="5ee00-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span>                                       |
| <span data-ttu-id="5ee00-121">ลำดับชั้นการขายปลีกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5ee00-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="5ee00-122">ใช้ชนิดลำดับชั้นสำหรับลำดับชั้นการจัดประเภทการขายปลีกเพิ่มเติมใด ๆ ที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="5ee00-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="5ee00-123">ตัวอย่างเช่น ในฤดูใบไม้ผลิ คุณมีโปรโมชันสำหรับชุดว่ายน้ำ</span><span class="sxs-lookup"><span data-stu-id="5ee00-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="5ee00-124">ดังนั้น คุณรวมผลิตภัณฑ์ชุดว่ายน้ำของคุณในลำดับชั้นของประเภทที่แยกต่างหาก และใช้การกำหนดราคาโปรโมชันไปยังประเภทผลิตภัณฑ์ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="5ee00-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="5ee00-125">ลำดับชั้นการนำทางของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5ee00-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="5ee00-126">ใช้ชนิดลำดับชั้นเพื่อจัดกลุ่มและการจัดระเบียบผลิตภัณฑ์ให้เป็นประเภทเพื่อให้สามารถถูกเรียกดูผลิตภัณฑ์แบบออนไลน์ หรือ ใน POS</span><span class="sxs-lookup"><span data-stu-id="5ee00-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span>                                                                                                                                                                                       |

<span data-ttu-id="5ee00-127">การใช้ลำดับชั้นประเภทการขายปลีกเพื่อจัดโครงสร้างผลิตภัณฑ์ของคุณ คุณสามารถตั้งค่า และรักษาคุณลักษณะของผลิตภัณฑ์และคุณสมบัติในระดับประเภท</span><span class="sxs-lookup"><span data-stu-id="5ee00-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="5ee00-128">คุณลักษณะและคุณสมบัติเหล่านี้รวมถึงการตั้งค่าสำหรับมิติของผลิตภัณฑ์และการตั้งค่าของ POS</span><span class="sxs-lookup"><span data-stu-id="5ee00-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="5ee00-129">ผลิตภัณฑ์ใด ๆ ที่คุณมอบหมายให้กับประเภทจะสืบทอดคุณลักษณะและคุณสมบัติที่คุณกำหนด</span><span class="sxs-lookup"><span data-stu-id="5ee00-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="5ee00-130">คุณยังสามารถคัดลอกการตั้งค่าคุณสมบัติสำหรับผลิตภัณฑ์ใด ๆ กับหลายผลิตภัณฑ์ในประเภทที่เลือกพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="5ee00-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>




