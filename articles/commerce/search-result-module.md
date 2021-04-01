---
title: โมดูลผลการค้นหา
description: หัวข้อนี้ครอบคลุมถึงโมดูลผลการค้นหาและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d852fe1a81b1e42484bc49ae136ef8613a2d3a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254780"
---
# <a name="search-results-module"></a><span data-ttu-id="4af2f-103">โมดูลผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4af2f-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4af2f-104">หัวข้อนี้ครอบคลุมถึงโมดูลผลการค้นหาและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4af2f-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4af2f-105">โมดูลผลการค้นหาจะส่งคืนผลการค้นหาผลิตภัณฑ์และรายการตัวคัดสรรที่ใช้ได้ของทั้งผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4af2f-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="4af2f-106">คุณสามารถใช้โมดูลผลการค้นหาบนไซต์ Dynamics 365 Commerce เพื่อแสดงหน้าของสถานการณ์ต่อไปนี้ได้</span><span class="sxs-lookup"><span data-stu-id="4af2f-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="4af2f-107">ผลการค้นหาที่เริ่มต้นโดยการค้นหาของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="4af2f-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="4af2f-108">ผลการค้นหาที่แสดงชุดเฉพาะของผลิตภัณฑ์ เช่น "เลือกซื้อสินค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="4af2f-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="4af2f-109">รายการของผลิตภัณฑ์ที่เป็นของประเภท</span><span class="sxs-lookup"><span data-stu-id="4af2f-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="4af2f-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับหน้าประเภทและผลการค้นหา โปรดดูที่ [ภาพรวมของหน้าเริ่มต้นและหน้าผลการค้นหา](category-search-page-overview.md)</span><span class="sxs-lookup"><span data-stu-id="4af2f-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="4af2f-111">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้าผลการค้นหาสำหรับประเภทบนไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="4af2f-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![ตัวอย่างของหน้าผลการค้นหาบนไซต์ Fabrikam](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="4af2f-113">คุณสมบัติโมดูลผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4af2f-113">Search results module properties</span></span>

<span data-ttu-id="4af2f-114">ตารางต่อไปนี้แสดงรายการคุณสมบัติของโมดูลผลการค้นหา พร้อมกับค่าและข้อความอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4af2f-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="4af2f-115">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="4af2f-115">Property</span></span> | <span data-ttu-id="4af2f-116">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="4af2f-116">Values</span></span> | <span data-ttu-id="4af2f-117">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4af2f-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="4af2f-118">สินค้าต่อหน้า</span><span class="sxs-lookup"><span data-stu-id="4af2f-118">Items per page</span></span> | <span data-ttu-id="4af2f-119">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="4af2f-119">Integer</span></span> | <span data-ttu-id="4af2f-120">จํานวนของสินค้าที่ควรแสดงในแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="4af2f-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="4af2f-121">อนุญาตให้ย้อนกลับบน PDP</span><span class="sxs-lookup"><span data-stu-id="4af2f-121">Allow back on PDP</span></span> | <span data-ttu-id="4af2f-122">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="4af2f-122">**True** or **False**</span></span> | <span data-ttu-id="4af2f-123">ถ้าตั้งค่าคุณสมบัตินี้เป็น **จริง** เมื่อผู้ใช้เลือกผลิตภัณฑ์ในหน้าผลการค้นหา การแสดงเส้นทางการนําทางในหน้ารายละเอียดผลิตภัณฑ์ (PDP) ที่เปิดจะแสดงลิงค์ "ย้อนกลับไปยังผลลัพธ์"</span><span class="sxs-lookup"><span data-stu-id="4af2f-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="4af2f-124">ขยายตัวคัดสรร</span><span class="sxs-lookup"><span data-stu-id="4af2f-124">Expand Refiners</span></span> | <span data-ttu-id="4af2f-125">**ทั้งหมด**, **1**, **2**, **3**, หรือ **4**</span><span class="sxs-lookup"><span data-stu-id="4af2f-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="4af2f-126">จํานวนของตัวปรับปรุงสูงสุดที่ควรขยายเมื่อมีการโหลดหน้า</span><span class="sxs-lookup"><span data-stu-id="4af2f-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="4af2f-127">ตัวอย่างเช่น ถ้าตั้งค่าคุณสมบัตินี้เป็น **3** ระบบก็จะขยายตัวปรับปรุงสามตัวแรกในหน้า</span><span class="sxs-lookup"><span data-stu-id="4af2f-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="4af2f-128">ซ่อนการแสดงการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="4af2f-128">Hide category hierarchy display</span></span> | <span data-ttu-id="4af2f-129">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="4af2f-129">**True** or **False**</span></span> | <span data-ttu-id="4af2f-130">ถ้าตั้งค่าคุณสมบัตินี้เป็น **จริง** การแสดงการจัดประเภทตามลำดับชั้นบนหน้าจะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="4af2f-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="4af2f-131">คุณสมบัตินี้ควรตั้งค่าเป็น **จริง** ถ้าคุณไม่ได้ใช้ [โมดูลการแสดงเส้นทาง](add-breadcrumb.md) เพื่อแสดงลำดับชั้นประเภท</span><span class="sxs-lookup"><span data-stu-id="4af2f-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="4af2f-132">มีคุณลักษณะของผลิตภัณฑ์ในผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4af2f-132">Include product attributes in search results</span></span> | <span data-ttu-id="4af2f-133">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="4af2f-133">**True** or **False**</span></span> | <span data-ttu-id="4af2f-134">หากตั้งค่าคุณสมบัตินี้เป็น **จริง** แอททริบิวต์จะถูกส่งคืนให้กับผลิตภัณฑ์ในผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4af2f-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="4af2f-135">แม้ว่าแอททริบิวต์เหล่านี้สามารถแสดงบนไซต์ Commerce ได้ แต่คุณจะต้องขยาย</span><span class="sxs-lookup"><span data-stu-id="4af2f-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="4af2f-136">แสดงราคาตัวแทน</span><span class="sxs-lookup"><span data-stu-id="4af2f-136">Show affiliation prices</span></span> | <span data-ttu-id="4af2f-137">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="4af2f-137">**True** or **False**</span></span> | <span data-ttu-id="4af2f-138">ถ้าคุณสมบัตินี้ถูกตั้งค่าเป็น **จริง** ราคาสังกัดของผลิตภัณฑ์จะแสดงขึ้นในผลการค้นหาเมื่อผู้ใช้ที่ลงชื่อเข้าใช้เรียกดูหน้า</span><span class="sxs-lookup"><span data-stu-id="4af2f-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="4af2f-139">ใน Dynamics 365 Commerce รุ่น 10.0.16 และที่ใหม่กว่านั้น การตั้งค่าคอนฟิก **แสดงราคาสังกัด** สามารถใช้เพื่อแสดงราคาในสังกัดบนหน้าได้</span><span class="sxs-lookup"><span data-stu-id="4af2f-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="4af2f-140">โมดูลที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="4af2f-140">Supported modules</span></span>

<span data-ttu-id="4af2f-141">โมดูลผลการค้นหาสนับสนุน [โมดูลมุมมองด่วน](quick-view-module.md) ซึ่งช่วยให้ผู้ใช้ดูข้อมูลผลิตภัณฑ์และเพิ่มสินค้าลงในรถเข็นจากหน้าผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4af2f-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="4af2f-142">เพิ่มโมดูลผลการค้นหาลงในหน้าประเภท</span><span class="sxs-lookup"><span data-stu-id="4af2f-142">Add a search results module to a category page</span></span>

<span data-ttu-id="4af2f-143">เมื่อต้องการเพิ่มโมดูลผลการค้นหาไปที่หน้าประเภท ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4af2f-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="4af2f-144">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="4af2f-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="4af2f-145">ในกล่องโต้ตอบ **แม่แบบใหม่** ให้ป้อนชื่อ **ผลการค้นหา** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4af2f-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="4af2f-146">ในช่อง **เนื้อหา** เลือกจุดไข่ปลา (...) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4af2f-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4af2f-147">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หน้าเริ่มต้น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4af2f-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4af2f-148">ในช่อง **หลัก** ของโมดูล **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (...) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4af2f-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4af2f-149">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4af2f-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4af2f-150">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (...) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4af2f-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4af2f-151">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **การแสดงเส้นทาง** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4af2f-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4af2f-152">ในบานหน้าต่างคุณสมบัติ **การแสดงเส้นทาง** ให้ป้อนค่า **1** สำหรับ **เกิดขึ้นต่ำสุด**</span><span class="sxs-lookup"><span data-stu-id="4af2f-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="4af2f-153">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (...) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4af2f-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4af2f-154">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ผลการค้นหา** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4af2f-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4af2f-155">ในบานหน้าต่างคุณสมบัติ **ผลการค้นหา** ให้ป้อนค่า **1** สำหรับ **เกิดขึ้นต่ำสุด** และจากนั้นตั้งค่าคุณสมบัติที่ต้องใช้อื่น ๆ ของโมดูลผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4af2f-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="4af2f-156">ด้วยการตั้งค่าคุณสมบัติเหล่านี้ในเท็มเพลต คุณแน่ใจหรือไม่ว่าการเลือกเลือกตั้งใด ๆ ที่หน้าประเภทเฉพาะจะรวมการตั้งค่าเหล่านี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4af2f-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="4af2f-157">เลือก **แก้ไขให้เสร็จสิ้น** และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่แม่แบบ</span><span class="sxs-lookup"><span data-stu-id="4af2f-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="4af2f-158">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="4af2f-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="4af2f-159">ในกล่องโต้ตอบ **เลือกแม่แบบ** ให้เลือกแม่แบบ **ผลการค้นหา** ที่คุณสร้าง ป้อน **หน้าประเภท** สำหรับ **ชื่อหน้า** และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4af2f-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="4af2f-160">เนื่องจากค่าทั้งหมดได้รับการตั้งค่าในแม่แบบนี้ คุณพร้อมจะเผยแพร่หน้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="4af2f-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="4af2f-161">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="4af2f-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4af2f-162">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4af2f-162">Additional resources</span></span>

[<span data-ttu-id="4af2f-163">ภาพรวมของหน้าเริ่มต้นของประเภทและหน้าผลการค้นหาค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4af2f-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="4af2f-164">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="4af2f-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4af2f-165">โมดูลมุมมองด่วน</span><span class="sxs-lookup"><span data-stu-id="4af2f-165">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]