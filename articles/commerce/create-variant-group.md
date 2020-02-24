---
title: การสร้างกลุ่มตัวแปร
description: หัวข้อนี้อธิบายวิธีสร้างกลุ่มตัวแปรขนาด ลักษณะ หรือสีของผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b9acd41c000b22e6c74b0d636a7f58917e4b5ac5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001886"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="36de9-103">การสร้างกลุ่มตัวแปร</span><span class="sxs-lookup"><span data-stu-id="36de9-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="36de9-104">หัวข้อนี้อธิบายวิธีสร้างกลุ่มตัวแปรขนาด ลักษณะ หรือสีของผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="36de9-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="36de9-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="36de9-105">Overview</span></span>

<span data-ttu-id="36de9-106">Dynamics 365 Commerce รองรับตัวแปรต่าง ๆ สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36de9-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="36de9-107">เหมาะที่จะตั้งค่ากลุ่มตัวแปรสำหรับประเภทผลิตภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="36de9-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="36de9-108">ตัวอย่างเช่น สามารถสร้างกลุ่มขนาดสำหรับเสื้อยืดที่มีขนาดเล็กพิเศษ เล็ก กลาง ใหญ่ และใหญ่พิเศษ หรือสามารถสร้างกลุ่มสีเพื่อรวมสีที่มีทั้งหมดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36de9-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="36de9-109">ควรเพิ่มกลุ่มตัวแปรก่อนที่จะเพิ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36de9-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="36de9-110">ในหัวข้อนี้ กลุ่มขนาดจะถูกสร้างขึ้นและกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="36de9-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="36de9-111">กระบวนการที่คล้ายกันสามารถใช้สำหรับการเพิ่มและกำหนดค่ากลุ่มลักษณะและกลุ่มสี</span><span class="sxs-lookup"><span data-stu-id="36de9-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="36de9-112">การสร้างกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="36de9-112">Create a size group</span></span>

<span data-ttu-id="36de9-113">ทำตามขั้นตอนเหล่านี้เพื่อสร้างกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="36de9-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="36de9-114">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> กลุ่มตัวแปร \> กลุ่มขนาด**</span><span class="sxs-lookup"><span data-stu-id="36de9-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="36de9-115">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="36de9-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="36de9-116">ในกล่อง **กลุ่มขนาด** ป้อนชื่อสำหรับกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="36de9-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="36de9-117">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายที่เหมาะสมลงไป</span><span class="sxs-lookup"><span data-stu-id="36de9-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="36de9-118">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="36de9-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="36de9-119">เพิ่มแอตทริบิวต์ในกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="36de9-119">Add attributes to the size group</span></span>

<span data-ttu-id="36de9-120">เมื่อต้องการเพิ่มแอตทริบิวต์ไปยังกลุ่มขนาด ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="36de9-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="36de9-121">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> กลุ่มตัวแปร \> กลุ่มขนาด**</span><span class="sxs-lookup"><span data-stu-id="36de9-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="36de9-122">ในบานหน้าต่างนำทาง ให้เลือกกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="36de9-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="36de9-123">ใต้ **บรรทัดกลุ่มขนาด** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="36de9-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="36de9-124">ในกล่อง **ขนาด** ป้อนสตริงที่แทนขนาด (ตัวอย่างเช่น "XL")</span><span class="sxs-lookup"><span data-stu-id="36de9-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="36de9-125">ในกล่อง **ชื่อขนาด** ป้อนชื่อสำหรับขนาด (ตัวอย่างเช่น "ใหญ่พิเศษ")</span><span class="sxs-lookup"><span data-stu-id="36de9-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="36de9-126">ในกล่อง **การเติมเต็มน้ำหนัก** ให้ป้อนตัวเลขที่แสดงถึงน้ำหนักการเติมเต็ม</span><span class="sxs-lookup"><span data-stu-id="36de9-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="36de9-127">ในกล่อง **หมายเลขในบาร์โค้ด** ให้ป้อนตัวเลขที่แสดงถึงบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="36de9-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="36de9-128">ในกล่อง **ลำดับการแสดงผล** ให้ป้อนหมายเลขที่แทนลำดับการแสดงผล</span><span class="sxs-lookup"><span data-stu-id="36de9-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="36de9-129">เมื่อเพิ่มขนาดเสร็จแล้ว ให้เลือก **บันทึก** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="36de9-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="36de9-130">ภาพต่อไปนี้แสดงตัวอย่างของกลุ่มขนาดสำหรับ "ขนาดเสื้อเชิ้ตลำลอง"</span><span class="sxs-lookup"><span data-stu-id="36de9-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![การสร้างกลุ่มขนาด](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="36de9-132">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="36de9-132">Additional resources</span></span>

[<span data-ttu-id="36de9-133">ภาพรวมของข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36de9-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="36de9-134">ตั้งค่าผลิตภัณฑ์ขายปลีก</span><span class="sxs-lookup"><span data-stu-id="36de9-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="36de9-135">มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36de9-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
