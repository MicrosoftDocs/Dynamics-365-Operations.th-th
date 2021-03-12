---
title: สร้างลำดับชั้นของผลิตภัณฑ์ใหม่
description: หัวข้อนี้อธิบายวิธีสร้างลำดับชั้นของผลิตภัณฑ์ใหม่ใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7d0c792a8590be474b05dea262ae11d15e0ada3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965233"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="4dbba-103">สร้างลำดับชั้นของผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="4dbba-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4dbba-104">หัวข้อนี้อธิบายวิธีสร้างลำดับชั้นของผลิตภัณฑ์ใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4dbba-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4dbba-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="4dbba-105">Overview</span></span>

<span data-ttu-id="4dbba-106">Dynamics 365 Commerce รองรับช่องทางการขายปลีกที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="4dbba-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="4dbba-107">ช่องทางการขายปลีกเหล่านี้รวมร้านค้าออนไลน์ ศูนย์บริการ และร้านค้าปลีก (เรียกอีกอย่างหนึ่งว่า ร้านค้าที่ให้บริการจริง)</span><span class="sxs-lookup"><span data-stu-id="4dbba-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="4dbba-108">ช่องทางของร้านค้าปลีกแต่ละช่องสามารถมีวิธีการชำระเงินของตัวเอง กลุ่มราคา การลงทะเบียนรวมระบบขายหน้าร้าน (POS) บัญชีรายได้ และบัญชีรายจ่าย และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="4dbba-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="4dbba-109">คุณต้องตั้งค่าองค์ประกอบเหล่านี้ทั้งหมดก่อนคุณจึงจะสามารถสร้างช่องทางร้านค้าปลีกได้</span><span class="sxs-lookup"><span data-stu-id="4dbba-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="4dbba-110">ลำดับชั้นผลิตภัณฑ์เชิงพาณิชย์ใช้เพื่อกำหนดลำดับชั้นผลิตภัณฑ์โดยรวมสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="4dbba-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="4dbba-111">คุณสามารถใช้ลำดับชั้นผลิตภัณฑ์เชิงพาณิชย์สำหรับการขายสินค้า การกำหนดราคาและการส่งเสริมการขาย การรายงาน และการวางแผนการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="4dbba-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="4dbba-112">สามารถกำหนดลำดับชั้นผลิตภัณฑ์เชิงพาณิชย์ได้เพียงหนึ่งรายการต่อองค์กร</span><span class="sxs-lookup"><span data-stu-id="4dbba-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="4dbba-113">สร้างและกำหนดค่าลำดับชั้นของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4dbba-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="4dbba-114">ทำตามขั้นตอนเหล่านี้เพื่อสร้างการกำหนดค่าลำดับชั้นผลิตภัณฑ์เชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="4dbba-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="4dbba-115">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ลำดับชั้นผลิตภัณฑ์เชิงพาณิชย์**</span><span class="sxs-lookup"><span data-stu-id="4dbba-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="4dbba-116">หากยังไม่มีลำดับชั้น บน **บานหน้าต่างการดำเนินการ** เลือก **ใหม่** เพื่อสร้างรากของลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="4dbba-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="4dbba-117">ภายใต้ **ทั่วไป**:</span><span class="sxs-lookup"><span data-stu-id="4dbba-117">Under **General**:</span></span>
    1. <span data-ttu-id="4dbba-118">ในกล่อง **ชื่อ** ป้อนชื่อลงไป</span><span class="sxs-lookup"><span data-stu-id="4dbba-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="4dbba-119">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายลงไป</span><span class="sxs-lookup"><span data-stu-id="4dbba-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="4dbba-120">ในกล่อง **ชื่อที่เรียกง่าย** ป้อนชื่อที่เรียกง่าย</span><span class="sxs-lookup"><span data-stu-id="4dbba-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="4dbba-121">ตั้งค่า **เปิดใช้งาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="4dbba-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="4dbba-122">เพิ่มโหนดของลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="4dbba-122">Add hierarchy nodes</span></span>

<span data-ttu-id="4dbba-123">เพื่อเพิ่มโหนดของลำดับชั้น ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4dbba-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="4dbba-124">ในบานหน้าต่างการดำเนินการ ให้เลือก **การจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="4dbba-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="4dbba-125">เลือกโหนดหลักที่คุณต้องการเพิ่มโหนดใหม่เข้าไป และจากนั้นเลือก **ประเภทโหนดใหม่**</span><span class="sxs-lookup"><span data-stu-id="4dbba-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="4dbba-126">ในส่วน **ทั่วไป** ป้อน **ชื่อ**, **คำอธิบาย**, **ชื่อที่เรียกง่าย** และ **คำสำคัญ**</span><span class="sxs-lookup"><span data-stu-id="4dbba-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="4dbba-127">ภายใต้ **ทั่วไป**:</span><span class="sxs-lookup"><span data-stu-id="4dbba-127">Under **General**:</span></span>
    1. <span data-ttu-id="4dbba-128">ในกล่อง **ชื่อ** ป้อนชื่อลงไป</span><span class="sxs-lookup"><span data-stu-id="4dbba-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="4dbba-129">ในกล่อง **คำอธิบาย** ป้อนคำอธิบายลงไป</span><span class="sxs-lookup"><span data-stu-id="4dbba-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="4dbba-130">ในกล่อง **ชื่อที่เรียกง่าย** ป้อนชื่อที่เรียกง่าย</span><span class="sxs-lookup"><span data-stu-id="4dbba-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="4dbba-131">ในกล่อง **คำสำคัญ** ให้ป้อนคำสำคัญที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4dbba-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="4dbba-132">ในกล่อง **ลำดับการแสดงผล** ให้ป้อนหมายเลขสำหรับลำดับการแสดงผล (ไม่จำเป็นต้องระบุ)</span><span class="sxs-lookup"><span data-stu-id="4dbba-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="4dbba-133">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4dbba-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="4dbba-134">ทำซ้ำขั้นตอนด้านบนเพื่อเพิ่มโหนดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4dbba-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="4dbba-135">รูปภาพต่อไปนี้แสดงการสร้างโหนดลำดับชั้นของผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="4dbba-135">The following image shows the creation of a new product hierarchy node.</span></span>

![สร้างลำดับชั้นของผลิตภัณฑ์](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="4dbba-137">การตั้งค่าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4dbba-137">Other settings</span></span>

<span data-ttu-id="4dbba-138">สามารถกำหนดกลุ่มแอตทริบิวต์ประเภทให้กับแต่ละกลุ่มได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="4dbba-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="4dbba-139">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4dbba-139">Additional resources</span></span>

[<span data-ttu-id="4dbba-140">ลำดับชั้นของการค้า</span><span class="sxs-lookup"><span data-stu-id="4dbba-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="4dbba-141">จัดการประเภทของผลิตภัณฑ์และผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="4dbba-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="4dbba-142">เปลี่ยนลำดับการจัดเรียงสำหรับเอนทิตี้การขาย</span><span class="sxs-lookup"><span data-stu-id="4dbba-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
