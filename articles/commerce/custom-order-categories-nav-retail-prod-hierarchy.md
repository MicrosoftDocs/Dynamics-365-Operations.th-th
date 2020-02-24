---
title: เปลี่ยนลำดับการจัดเรียงสำหรับการจัดซื้อสินค้าเอนทิตี้
description: หัวข้อนี้อธิบายแนวคิดที่เกี่ยวข้องกับการควบคุมลำดับการแสดงผลสำหรับการจัดซื้อสินค้าที่เกี่ยวข้องกับเอนทิตี้อื่นๆใน Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024157"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="29a16-103">เปลี่ยนลำดับการจัดเรียงสำหรับการจัดซื้อสินค้าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="29a16-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="29a16-104">ผู้ค้าปลีกพิจารณาการค้นพบผลิตภัณฑ์เป็นเครื่องมือหลักสำหรับการโต้ตอบกับลูกค้าในทุกช่องทาง</span><span class="sxs-lookup"><span data-stu-id="29a16-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="29a16-105">ฟังก์ชันต่างๆสามารถช่วยลูกค้าในการค้นหาผลิตภัณฑ์ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="29a16-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="29a16-106">ตัวอย่างเช่น ลูกค้าสามารถเรียกดูประเภท การค้นหา เเละตัวกรองข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="29a16-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="29a16-107">หัวข้อนี้อธิบายแนวคิดที่เกี่ยวข้องกับการควบคุมลำดับการแสดงผลสำหรับการจัดซื้อสินค้าที่เกี่ยวข้องกับเอนทิตี้อื่นๆใน</span><span class="sxs-lookup"><span data-stu-id="29a16-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="29a16-108">นอกจากนี้ยังอธิบายวิธีการเปลี่ยนลำดับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="29a16-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="29a16-109">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="29a16-109">Overview</span></span>

<span data-ttu-id="29a16-110">การสนับสนุนสำหรับการเรียงลำดับเอนทิตี้ที่เกี่ยวข้องกับการจัดซื้อสินค้าที่หลายรายการได้รับการปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="29a16-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="29a16-111">ขณะนี้การสนับสนุนนี้มีความสอดคล้องดีขึ้นกับสถานการณ์จำลองของลูกค้าที่มีอยู่ซึ่งเป็นส่วนขยายที่จำเป็นก่อนหน้านี้สำหรับการใช้งานของคู่ค้า</span><span class="sxs-lookup"><span data-stu-id="29a16-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="29a16-112">ในรุ่น Retail ที่เก่ากว่ารุ่น 10.0.5 การจัดเรียงลำดับสำหรับประเภทในลำดับชั้นการนำทางจะจัดลำดับตามลำดับตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="29a16-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="29a16-113">ฟังก์ชันลำดับการเรียงใหม่แบบกำหนดเองช่วยให้ผู้จัดการฝ่ายจัดซื้อการจัดโครงแบบการเรียงสำหรับเอนทิตี้ที่เกี่ยวข้องกับการจัดซื้อสินค้าต่างๆไปยังไคลเอนต์ผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="29a16-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="29a16-114">ไคลเอนต์เหล่านี้รวมถึงสำนักงานใหญ่ (HQ) และศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="29a16-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="29a16-115">กำหนดค่าลำดับการแสดงผลสำหรับประเภทในลำดับชั้นผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="29a16-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="29a16-116">ก่อนที่คุณจะสามารถทำกระบวนงานนี้ให้เสร็จสมบูรณ์ได้ ข้อมูลสาธิตต้องถูกติดตั้งในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="29a16-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="29a16-117">ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ลำดับชั้นผลิตภัณฑ์เชิงพาณิชย์**</span><span class="sxs-lookup"><span data-stu-id="29a16-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="29a16-118">คลิก **แก้ไขการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="29a16-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="29a16-119">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="29a16-119">Click **Edit**.</span></span>
4. <span data-ttu-id="29a16-120">ในเเผนภูมิ ขยาย **ALL \> Action Sports**</span><span class="sxs-lookup"><span data-stu-id="29a16-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="29a16-121">ในเเผนภูมิ ขยาย **ALL \> Team Sports**</span><span class="sxs-lookup"><span data-stu-id="29a16-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="29a16-122">ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="29a16-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="29a16-123">(ตัวเลขสามารถเป็นค่าลบ)</span><span class="sxs-lookup"><span data-stu-id="29a16-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="29a16-124">ทำซ้ำขั้นตอนที่4ถึง6สำหรับประเภทเพิ่มเติมใดๆที่คุณต้องการเปลี่ยนแปลงลำดับ</span><span class="sxs-lookup"><span data-stu-id="29a16-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="29a16-125">ลำดับการแสดงผลสำหรับลำดับชั้นการนำทางของช่องทางจะปรากฏใน HQ สำหรับลำดับชั้นของผลิตภัณฑ์เชิงพาณิชย์และผลิตภัณฑ์ที่วางจำหน่ายตามประเภท</span><span class="sxs-lookup"><span data-stu-id="29a16-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![ลำดับชั้นผลิตภัณฑ์ที่กำหนดเองเรียงลำดับด้วยค่าลบ](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![เปิดตัวผลิตภัณฑ์ตามประเภทที่กำหนดเองเรียงลำดับตามลำดับชั้นของผลิตภัณฑ์](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="29a16-128">ตั้งค่าคอนฟิกลำดับการแสดงผลสำหรับประเภทในลำดับชั้นของช่องทางการนำทาง</span><span class="sxs-lookup"><span data-stu-id="29a16-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="29a16-129">ก่อนที่คุณจะสามารถทำกระบวนงานนี้ให้เสร็จสมบูรณ์ได้ ข้อมูลสาธิตต้องถูกติดตั้งในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="29a16-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="29a16-130">ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ประเภทการนำทางของช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="29a16-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="29a16-131">ในรายการ เลือก **ลำดับชั้นการนำทางแฟชั่น** </span><span class="sxs-lookup"><span data-stu-id="29a16-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="29a16-132">คลิก **แก้ไขการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="29a16-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="29a16-133">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="29a16-133">Click **Edit**.</span></span>
5. <span data-ttu-id="29a16-134">ในแผนภูมิ เลือก **Fashion \> Womenswear \> Womens Shoes**</span><span class="sxs-lookup"><span data-stu-id="29a16-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="29a16-135">ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="29a16-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="29a16-136">ในแผนภูมิ เลือก **Fashion \> Womenswear \> Tops**</span><span class="sxs-lookup"><span data-stu-id="29a16-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="29a16-137">เช่นเดียวกัน คุณยังสามารถกำหนดลำดับการจัดเรียงสำหรับประเภทย่อยได้</span><span class="sxs-lookup"><span data-stu-id="29a16-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="29a16-138">ในแผนภูมิ เลือก **Fashion \> Menswear \> Womens Shoes**</span><span class="sxs-lookup"><span data-stu-id="29a16-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="29a16-139">ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="29a16-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="29a16-140">ในแผนภูมิ เลือก **Fashion \> Menswear \> Coats & Jackets**</span><span class="sxs-lookup"><span data-stu-id="29a16-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="29a16-141">ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="29a16-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="29a16-142">ทำซ้ำสำหรับประเภทเพิ่มเติมใดๆที่คุณต้องการเปลี่ยนแปลงลำดับ</span><span class="sxs-lookup"><span data-stu-id="29a16-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="29a16-143">ลำดับการแสดงผลสำหรับลำดับชั้นการนำทางของช่องทางปรากฏใน HQ แค็ตตาล็อก และช่องทาง</span><span class="sxs-lookup"><span data-stu-id="29a16-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![ลำดับชั้นการนำทางของช่องทางเเบบกำหนดเองตามลำดับ](./media/ChannelNavCustomSorted.png)

![แค็ตตาล็อกการนำทางของช่องทางเรียงเเบบกำหนดเองตามลำดับชั้นการนำทางของช่องทาง](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS ที่มีประเภทการเรียงลำดับแบบกำหนดเอง](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="29a16-147">ตามค่าเริ่มต้น คุณลักษณะการเรียงลำดับเเบบกำหนดเองจะถูกปิด</span><span class="sxs-lookup"><span data-stu-id="29a16-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="29a16-148">เมื่อต้องการเรียนรู้วิธีการเปิดใช้งานลักษณะ เเละคุณลักษณะอื่นๆ ดูที่ [การจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview)</span><span class="sxs-lookup"><span data-stu-id="29a16-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
