---
title: เปลี่ยนลำดับการจัดเรียงสำหรับการจัดซื้อสินค้าเอนทิตี้
description: หัวข้อนี้อธิบายแนวคิดที่เกี่ยวข้องกับการควบคุมลำดับการแสดงผลสำหรับการจัดซื้อสินค้าที่เกี่ยวข้องกับเอนทิตี้อื่นๆใน Dynamics 365 Commerce
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 54929f924bd9c2b59dec453cf580e0b2bc149d38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799480"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="f14e1-103">เปลี่ยนลำดับการจัดเรียงสำหรับการจัดซื้อสินค้าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="f14e1-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f14e1-104">ผู้ค้าปลีกพิจารณาการค้นพบผลิตภัณฑ์เป็นเครื่องมือหลักสำหรับการโต้ตอบกับลูกค้าในทุกช่องทาง</span><span class="sxs-lookup"><span data-stu-id="f14e1-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="f14e1-105">ฟังก์ชันต่างๆสามารถช่วยลูกค้าในการค้นหาผลิตภัณฑ์ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="f14e1-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="f14e1-106">ตัวอย่างเช่น ลูกค้าสามารถเรียกดูประเภท การค้นหา เเละตัวกรองข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="f14e1-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="f14e1-107">หัวข้อนี้อธิบายแนวคิดที่เกี่ยวข้องกับการควบคุมลำดับการแสดงผลสำหรับการจัดซื้อสินค้าที่เกี่ยวข้องกับเอนทิตี้อื่นๆใน</span><span class="sxs-lookup"><span data-stu-id="f14e1-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="f14e1-108">นอกจากนี้ยังอธิบายวิธีการเปลี่ยนลำดับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="f14e1-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="f14e1-109">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="f14e1-109">Overview</span></span>

<span data-ttu-id="f14e1-110">การสนับสนุนสำหรับการเรียงลำดับเอนทิตี้ที่เกี่ยวข้องกับการจัดซื้อสินค้าที่หลายรายการได้รับการปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="f14e1-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="f14e1-111">ขณะนี้การสนับสนุนนี้มีความสอดคล้องดีขึ้นกับสถานการณ์จำลองของลูกค้าที่มีอยู่ซึ่งเป็นส่วนขยายที่จำเป็นก่อนหน้านี้สำหรับการใช้งานของคู่ค้า</span><span class="sxs-lookup"><span data-stu-id="f14e1-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="f14e1-112">ในรุ่น Retail ที่เก่ากว่ารุ่น 10.0.5 การจัดเรียงลำดับสำหรับประเภทในลำดับชั้นการนำทางจะจัดลำดับตามลำดับตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="f14e1-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="f14e1-113">ฟังก์ชันลำดับการเรียงใหม่แบบกำหนดเองช่วยให้ผู้จัดการฝ่ายจัดซื้อการจัดโครงแบบการเรียงสำหรับเอนทิตี้ที่เกี่ยวข้องกับการจัดซื้อสินค้าต่างๆไปยังไคลเอนต์ผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="f14e1-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="f14e1-114">ไคลเอนต์เหล่านี้รวมถึงสำนักงานใหญ่ (HQ) และศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="f14e1-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="f14e1-115">กำหนดค่าลำดับการแสดงผลสำหรับประเภทในลำดับชั้นผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f14e1-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="f14e1-116">ก่อนที่คุณจะสามารถทำกระบวนงานนี้ให้เสร็จสมบูรณ์ได้ ข้อมูลสาธิตต้องถูกติดตั้งในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="f14e1-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="f14e1-117">ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ลำดับชั้นผลิตภัณฑ์เชิงพาณิชย์**</span><span class="sxs-lookup"><span data-stu-id="f14e1-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="f14e1-118">คลิก **แก้ไขการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="f14e1-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="f14e1-119">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f14e1-119">Click **Edit**.</span></span>
4. <span data-ttu-id="f14e1-120">ในเเผนภูมิ ขยาย **ALL \> Action Sports**</span><span class="sxs-lookup"><span data-stu-id="f14e1-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="f14e1-121">ในเเผนภูมิ ขยาย **ALL \> Team Sports**</span><span class="sxs-lookup"><span data-stu-id="f14e1-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="f14e1-122">ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f14e1-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="f14e1-123">(ตัวเลขสามารถเป็นค่าลบ)</span><span class="sxs-lookup"><span data-stu-id="f14e1-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="f14e1-124">ทำซ้ำขั้นตอนที่4ถึง6สำหรับประเภทเพิ่มเติมใดๆที่คุณต้องการเปลี่ยนแปลงลำดับ</span><span class="sxs-lookup"><span data-stu-id="f14e1-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="f14e1-125">ลำดับการแสดงผลสำหรับลำดับชั้นการนำทางของช่องทางจะปรากฏใน HQ สำหรับลำดับชั้นของผลิตภัณฑ์เชิงพาณิชย์และผลิตภัณฑ์ที่วางจำหน่ายตามประเภท</span><span class="sxs-lookup"><span data-stu-id="f14e1-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![ลำดับชั้นผลิตภัณฑ์ที่กำหนดเองเรียงลำดับด้วยค่าลบ](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![เปิดตัวผลิตภัณฑ์ตามประเภทที่กำหนดเองเรียงลำดับตามลำดับชั้นของผลิตภัณฑ์](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="f14e1-128">ตั้งค่าคอนฟิกลำดับการแสดงผลสำหรับประเภทในลำดับชั้นของช่องทางการนำทาง</span><span class="sxs-lookup"><span data-stu-id="f14e1-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="f14e1-129">ก่อนที่คุณจะสามารถทำกระบวนงานนี้ให้เสร็จสมบูรณ์ได้ ข้อมูลสาธิตต้องถูกติดตั้งในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="f14e1-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="f14e1-130">ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ประเภทการนำทางของช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="f14e1-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="f14e1-131">ในรายการ เลือก **ลำดับชั้นการนำทางแฟชั่น** </span><span class="sxs-lookup"><span data-stu-id="f14e1-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="f14e1-132">คลิก **แก้ไขการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="f14e1-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="f14e1-133">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f14e1-133">Click **Edit**.</span></span>
5. <span data-ttu-id="f14e1-134">ในแผนภูมิ เลือก **Fashion \> Womenswear \> Womens Shoes**</span><span class="sxs-lookup"><span data-stu-id="f14e1-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="f14e1-135">ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f14e1-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="f14e1-136">ในแผนภูมิ เลือก **Fashion \> Womenswear \> Tops**</span><span class="sxs-lookup"><span data-stu-id="f14e1-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="f14e1-137">เช่นเดียวกัน คุณยังสามารถกำหนดลำดับการจัดเรียงสำหรับประเภทย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f14e1-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="f14e1-138">ในแผนภูมิ เลือก **Fashion \> Menswear \> Womens Shoes**</span><span class="sxs-lookup"><span data-stu-id="f14e1-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="f14e1-139">ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f14e1-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="f14e1-140">ในแผนภูมิ เลือก **Fashion \> Menswear \> Coats & Jackets**</span><span class="sxs-lookup"><span data-stu-id="f14e1-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="f14e1-141">ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f14e1-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="f14e1-142">ทำซ้ำสำหรับประเภทเพิ่มเติมใดๆที่คุณต้องการเปลี่ยนแปลงลำดับ</span><span class="sxs-lookup"><span data-stu-id="f14e1-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="f14e1-143">ลำดับการแสดงผลสำหรับลำดับชั้นการนำทางของช่องทางปรากฏใน HQ แค็ตตาล็อก และช่องทาง</span><span class="sxs-lookup"><span data-stu-id="f14e1-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![ลำดับชั้นการนำทางของช่องทางเเบบกำหนดเองตามลำดับ](./media/ChannelNavCustomSorted.png)

![แค็ตตาล็อกการนำทางของช่องทางเรียงเเบบกำหนดเองตามลำดับชั้นการนำทางของช่องทาง](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS ที่มีประเภทการเรียงลำดับแบบกำหนดเอง](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="f14e1-147">ตามค่าเริ่มต้น คุณลักษณะการเรียงลำดับเเบบกำหนดเองจะถูกปิด</span><span class="sxs-lookup"><span data-stu-id="f14e1-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="f14e1-148">เมื่อต้องการเรียนรู้วิธีการเปิดใช้งานลักษณะ เเละคุณลักษณะอื่นๆ ดูที่ [การจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview)</span><span class="sxs-lookup"><span data-stu-id="f14e1-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]