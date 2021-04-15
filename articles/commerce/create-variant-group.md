---
title: การสร้างกลุ่มตัวแปร
description: หัวข้อนี้อธิบายวิธีสร้างขนาด สไตล์ หรือสีของกลุ่มตัวแปรสำหรับผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0462958d8225de145a8d886b096f96cd3f2cb5c5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799552"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="01e70-103">สร้างกลุ่มตัวแปร</span><span class="sxs-lookup"><span data-stu-id="01e70-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="01e70-104">หัวข้อนี้อธิบายวิธีสร้างขนาด สไตล์ หรือสีของกลุ่มตัวแปรสำหรับผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="01e70-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="01e70-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="01e70-105">Overview</span></span>

<span data-ttu-id="01e70-106">Dynamics 365 Commerce รองรับตัวแปรต่าง ๆ สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01e70-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="01e70-107">เหมาะที่จะตั้งค่ากลุ่มตัวแปรสำหรับประเภทผลิตภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="01e70-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="01e70-108">ตัวอย่างเช่น สามารถสร้างกลุ่มขนาดสำหรับเสื้อยืดที่มีขนาดเล็กพิเศษ เล็ก กลาง ใหญ่ และใหญ่พิเศษ หรือสามารถสร้างกลุ่มสีเพื่อรวมสีที่มีทั้งหมดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01e70-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="01e70-109">ควรเพิ่มกลุ่มตัวแปรก่อนที่จะเพิ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01e70-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="01e70-110">ในหัวข้อนี้ กลุ่มขนาดจะถูกสร้างขึ้นและกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="01e70-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="01e70-111">กระบวนการที่คล้ายกันสามารถใช้สำหรับการเพิ่มและกำหนดค่ากลุ่มลักษณะและกลุ่มสี</span><span class="sxs-lookup"><span data-stu-id="01e70-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="01e70-112">การสร้างกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="01e70-112">Create a size group</span></span>

<span data-ttu-id="01e70-113">ทำตามขั้นตอนเหล่านี้เพื่อสร้างกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="01e70-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="01e70-114">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> กลุ่มตัวแปร \> กลุ่มขนาด**</span><span class="sxs-lookup"><span data-stu-id="01e70-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="01e70-115">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="01e70-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="01e70-116">ในกล่อง **กลุ่มขนาด** ป้อนชื่อสำหรับกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="01e70-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="01e70-117">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายที่เหมาะสมลงไป</span><span class="sxs-lookup"><span data-stu-id="01e70-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="01e70-118">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="01e70-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="01e70-119">เพิ่มแอตทริบิวต์ในกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="01e70-119">Add attributes to the size group</span></span>

<span data-ttu-id="01e70-120">เมื่อต้องการเพิ่มแอตทริบิวต์ไปยังกลุ่มขนาด ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="01e70-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="01e70-121">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> กลุ่มตัวแปร \> กลุ่มขนาด**</span><span class="sxs-lookup"><span data-stu-id="01e70-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="01e70-122">ในบานหน้าต่างนำทาง ให้เลือกกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="01e70-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="01e70-123">ใต้ **บรรทัดกลุ่มขนาด** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="01e70-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="01e70-124">ในกล่อง **ขนาด** ป้อนสตริงที่แทนขนาด (ตัวอย่างเช่น "XL")</span><span class="sxs-lookup"><span data-stu-id="01e70-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="01e70-125">ในกล่อง **ชื่อขนาด** ป้อนชื่อสำหรับขนาด (ตัวอย่างเช่น "ใหญ่พิเศษ")</span><span class="sxs-lookup"><span data-stu-id="01e70-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="01e70-126">ในกล่อง **การเติมเต็มน้ำหนัก** ให้ป้อนตัวเลขที่แสดงถึงน้ำหนักการเติมเต็ม</span><span class="sxs-lookup"><span data-stu-id="01e70-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="01e70-127">ในกล่อง **หมายเลขในบาร์โค้ด** ให้ป้อนตัวเลขที่แสดงถึงบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="01e70-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="01e70-128">ในกล่อง **ลำดับการแสดงผล** ให้ป้อนหมายเลขที่แทนลำดับการแสดงผล</span><span class="sxs-lookup"><span data-stu-id="01e70-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="01e70-129">เมื่อเพิ่มขนาดเสร็จแล้ว ให้เลือก **บันทึก** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="01e70-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="01e70-130">ภาพต่อไปนี้แสดงตัวอย่างของกลุ่มขนาดสำหรับ "ขนาดเสื้อเชิ้ตลำลอง"</span><span class="sxs-lookup"><span data-stu-id="01e70-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![การสร้างกลุ่มขนาด](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="01e70-132">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="01e70-132">Additional resources</span></span>

[<span data-ttu-id="01e70-133">ภาพรวมของข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01e70-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="01e70-134">ตั้งค่าผลิตภัณฑ์ขายปลีก</span><span class="sxs-lookup"><span data-stu-id="01e70-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="01e70-135">มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01e70-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]