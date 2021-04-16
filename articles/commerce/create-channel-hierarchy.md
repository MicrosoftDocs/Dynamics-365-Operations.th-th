---
title: สร้างลำดับชั้นการนำทางของช่องทาง
description: หัวข้อนี้จะอธิบายวิธีการสร้างลำดับชั้นการนำทางของช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 358f3d40c7a21184c20da342d6b2bf72dd4e7bbd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795846"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="5ed79-103">สร้างลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="5ed79-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5ed79-104">หัวข้อนี้จะอธิบายวิธีการสร้างลำดับชั้นการนำทางของช่องทางใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5ed79-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5ed79-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="5ed79-105">Overview</span></span>

<span data-ttu-id="5ed79-106">ลำดับชั้นการนำทางช่องทางถูกใช้ในการจัดกลุ่มและจัดระเบียบผลิตภัณฑ์ให้เป็นประเภท เพื่อให้สามารถเรียกดูผลิตภัณฑ์แบบออนไลน์หรือในการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="5ed79-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="5ed79-107">สร้างลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="5ed79-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="5ed79-108">ในการสร้างลำดับชั้นการนำทางของช่องทาง ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5ed79-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5ed79-109">ในบานหน้าต่างการนำทาง ไปที่ **โมดูล \> Retail และการค้า \> ผลิตภัณฑ์และประเภท \> ประเภทการนำทางช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="5ed79-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="5ed79-110">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="5ed79-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5ed79-111">ในกล่อง **ชื่อ** ป้อนชื่อลงไป</span><span class="sxs-lookup"><span data-stu-id="5ed79-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="5ed79-112">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายลงไป</span><span class="sxs-lookup"><span data-stu-id="5ed79-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="5ed79-113">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="5ed79-113">Select **Create**.</span></span>
1. <span data-ttu-id="5ed79-114">บนบานหน้าต่างการดำเนินการ เลือก **โหนดประเภทใหม่** เพื่อสร้างโหนดราก</span><span class="sxs-lookup"><span data-stu-id="5ed79-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="5ed79-115">ในกล่อง **ชื่อ** ป้อนชื่อลงไป</span><span class="sxs-lookup"><span data-stu-id="5ed79-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="5ed79-116">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายลงไป</span><span class="sxs-lookup"><span data-stu-id="5ed79-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="5ed79-117">ในกล่อง **ชื่อที่เรียกง่าย** ป้อนชื่อที่เรียกง่าย</span><span class="sxs-lookup"><span data-stu-id="5ed79-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="5ed79-118">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5ed79-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5ed79-119">รูปภาพต่อไปนี้แสดงโหนดรากตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="5ed79-119">The following image shows a example root node.</span></span>

![โหนดรากตัวอย่าง](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="5ed79-121">สร้างโหนดประเภทการนำทาง</span><span class="sxs-lookup"><span data-stu-id="5ed79-121">Create navigation category nodes</span></span>

<span data-ttu-id="5ed79-122">เมื่อต้องการสร้างโหนดประเภทการนำทางเพิ่มเติมใดๆ เพื่อแสดงถึงประเภทผลิตภัณฑ์บนช่องสัญญาณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5ed79-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="5ed79-123">ในบานหน้าต่างการนำทาง ให้เลือกโหนดหลักเพื่อเพิ่มประเภท</span><span class="sxs-lookup"><span data-stu-id="5ed79-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="5ed79-124">ในบานหน้าต่างการดำเนินการ ให้เลือก **โหนดประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="5ed79-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="5ed79-125">ในกล่อง **ชื่อ** ป้อนชื่อลงไป</span><span class="sxs-lookup"><span data-stu-id="5ed79-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="5ed79-126">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายลงไป</span><span class="sxs-lookup"><span data-stu-id="5ed79-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="5ed79-127">ในกล่อง **ชื่อที่เรียกง่าย** ป้อนชื่อที่เรียกง่าย</span><span class="sxs-lookup"><span data-stu-id="5ed79-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="5ed79-128">ในกล่อง **ลำดับการแสดงผล** ให้ป้อนลำดับการแสดงผล (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5ed79-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="5ed79-129">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5ed79-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5ed79-130">รูปภาพต่อไปนี้แสดงตัวอย่างของลำดับชั้นการนำทางช่องทางที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="5ed79-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![ลำดับชั้นช่องทางตัวอย่าง](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="5ed79-132">เพิ่มผลิตภัณฑ์ไปยังโหนดประเภท</span><span class="sxs-lookup"><span data-stu-id="5ed79-132">Add products to category nodes</span></span>

<span data-ttu-id="5ed79-133">เมื่อต้องการเพิ่มผลิตภัณฑ์ไปยังโหนดประเภท ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5ed79-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="5ed79-134">เลือกโหนดประเภท</span><span class="sxs-lookup"><span data-stu-id="5ed79-134">Select a category node.</span></span>
1. <span data-ttu-id="5ed79-135">ภายใต้ **ผลิตภัณฑ์** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="5ed79-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="5ed79-136">ค้นหาผลิตภัณฑ์ใหม่ที่คุณต้องการเพิ่มโดยใช้หมายเลขผลิตภัณฑ์หรือชื่อผลิตภัณฑ์ และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5ed79-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="5ed79-137">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5ed79-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="5ed79-138">การเพิ่มผลิตภัณฑ์ลงในโหนดในลำดับชั้นการนำทางช่องทางไม่เพียงพอสำหรับผลิตภัณฑ์ที่จะแสดงบนช่องทางที่เลือก ผลิตภัณฑ์ต้องถูกจัดประเภทไปยังผลิตภัณฑ์ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="5ed79-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="5ed79-139">รูปภาพต่อไปนี้แสดงโหนดตัวอย่างที่มีผลิตภัณฑ์ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5ed79-139">The following image shows an example node with products added.</span></span>

![ผลิตภัณฑ์ที่เพิ่มไปยังโหนดประเภท](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="5ed79-141">เพิ่มกลุ่มคุณลักษณะของผลิตภัณฑ์ไปยังโหนดประเภท</span><span class="sxs-lookup"><span data-stu-id="5ed79-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="5ed79-142">ต้องสร้างกลุ่มแอตทริบิวต์ก่อนที่คุณจะสามารถเพิ่มเข้าไปในโหนดในลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="5ed79-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="5ed79-143">เมื่อต้องการเพิ่มกลุ่มแอตทริบิวต์ผลิตภัณฑ์ไปยังโหนดประเภท ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5ed79-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="5ed79-144">เลือกโหนดประเภท</span><span class="sxs-lookup"><span data-stu-id="5ed79-144">Select a category node.</span></span>
1. <span data-ttu-id="5ed79-145">ภายใต้ **กลุ่มคุณลักษณะของผลิตภัณฑ์** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="5ed79-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="5ed79-146">ค้นหากลุ่มแอตทริบิวต์ที่คุณต้องการเพิ่ม แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5ed79-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="5ed79-147">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5ed79-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5ed79-148">รูปภาพต่อไปนี้แสดงโหนดตัวอย่างที่มีกลุ่มคุณลักษณะของผลิตภัณฑ์ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5ed79-148">The following image shows a sample node with product attribute groups added.</span></span>

![กลุ่มคุณลักษณะของผลิตภัณฑ์บนโหนด](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="5ed79-150">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5ed79-150">Additional resources</span></span>

[<span data-ttu-id="5ed79-151">ตั้งค่าการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="5ed79-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="5ed79-152">จัดการแอททริบิวต์และกลุ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="5ed79-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]