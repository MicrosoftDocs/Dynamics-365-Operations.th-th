---
title: โมดูลเมนูนำทาง
description: หัวข้อนี้ครอบคลุมถึงโมดูลเมนูนำทางและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055748"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="e0df6-103">โมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="e0df6-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e0df6-104">หัวข้อนี้ครอบคลุมถึงโมดูลเมนูนำทางและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e0df6-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e0df6-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e0df6-105">Overview</span></span>

<span data-ttu-id="e0df6-106">วัตถุประสงค์หลักของโมดูลนำทางเมนูคือเพื่ออนุญาตให้ผู้ใช้ไซต์สามารถเรียกดูผลิตภัณฑ์และหน้าของไซต์ตามลำดับชั้นการนำทางของช่องทางที่กำหนดไว้ในศูนย์ควบคุม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e0df6-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="e0df6-107">สินค้าที่ได้รับการตั้งค่าคอนฟิกไว้ในโมดูลตัวเลือกเมนูนำทางจะปรากฏเป็นการนำทางในส่วนหัวของไซต์</span><span class="sxs-lookup"><span data-stu-id="e0df6-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="e0df6-108">โมดูลเมนูนำทางยังสนับสนุนรายการเมนูแบบคงที่ที่เชื่อมโยงไปยังหน้าอื่นๆ บนไซต์อีคอมเมิร์ซด้วย</span><span class="sxs-lookup"><span data-stu-id="e0df6-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="e0df6-109">คุณสามารถเพิ่มโมดูลเมนูนำทางในโมดูลส่วนหัวของหน้าได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="e0df6-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="e0df6-110">ในชุดรูปแบบ Fabrikam เมนูนำทางจะแสดงสองระดับตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e0df6-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="e0df6-111">ในชุดรูปแบบชุดเริ่มต้น เมนูนำทางจะแสดงสามระดับตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e0df6-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="e0df6-112">เมื่อต้องการเปลี่ยนแปลงจำนวนระดับ จะต้องใช้ส่วนขยายสำหรับมุมมองในชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="e0df6-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="e0df6-113">ภาพประกอบต่อไปนี้แสดงตัวอย่างของเมนูนำทางสำหรับไซต์ Fabrikam ที่มีการจัดประเภทตามลำดับชั้นสองระดับและรายการเมนูแบบคงที่บางส่วน</span><span class="sxs-lookup"><span data-stu-id="e0df6-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="e0df6-114">![ตัวอย่างของโมดูลการนำทาง](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="e0df6-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="e0df6-115">คุณสมบัติของโมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="e0df6-115">Navigation menu module properties</span></span>

| <span data-ttu-id="e0df6-116">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="e0df6-116">Property name</span></span>             | <span data-ttu-id="e0df6-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="e0df6-117">Value</span></span>                 | <span data-ttu-id="e0df6-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e0df6-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e0df6-119">ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="e0df6-119">Source</span></span>                  | <span data-ttu-id="e0df6-120">**การขายปลีก** , **การสร้างด้วยตนเอง** , **การขายปลีกและการสร้างด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="e0df6-120">**Retail** , **Manual authoring** , **Retail and manual authoring**</span></span> | <span data-ttu-id="e0df6-121">ค่าของ **การขายปลีก** จะช่วยให้สามารถแสดงลำดับชั้นการนำทางของช่องทางจากศูนย์ควบคุม Commerce เพื่อแสดงบนเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="e0df6-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="e0df6-122">ค่า **การสร้างด้วยตนเอง** จะช่วยให้สามารถระบุรายการเมนูแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="e0df6-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="e0df6-123">ค่าของ **การขายปลีกและการสร้างด้วยตนเอง** จะช่วยให้สามารถผสมผสานกันได้ทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="e0df6-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="e0df6-124">แสดงรูปภาพประเภท</span><span class="sxs-lookup"><span data-stu-id="e0df6-124">Show category images</span></span> | <span data-ttu-id="e0df6-125">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="e0df6-125">**True** or **False**</span></span>    | <span data-ttu-id="e0df6-126">เมื่อเปิดใช้งาน คุณสมบัตินี้จะแสดงรูปภาพประเภทบนเมนูนำทางตามที่กำหนดไว้ในศูนย์ควบคุม Commerce สำหรับแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="e0df6-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="e0df6-127">มีการเพิ่มใน Commerce รีลีส 10.0.14</span><span class="sxs-lookup"><span data-stu-id="e0df6-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="e0df6-128">เปิดใช้งานเมนูนำทางแบบหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="e0df6-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="e0df6-129">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="e0df6-129">**True** or **False**</span></span> | <span data-ttu-id="e0df6-130">เมื่อเปิดใช้คุณสมบัตินี้ เมนูนำทางสามารถแสดงลำดับชั้นการนำทางหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="e0df6-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="e0df6-131">คุณลักษณะนี้พร้อมใช้งานใน Dynamics 365 Commerce การเผยแพร่ 10.0.15</span><span class="sxs-lookup"><span data-stu-id="e0df6-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="e0df6-132">จำนวนของระดับ</span><span class="sxs-lookup"><span data-stu-id="e0df6-132">Number of levels</span></span> | <span data-ttu-id="e0df6-133">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="e0df6-133">integer</span></span> | <span data-ttu-id="e0df6-134">คุณสมบัตินี้กำหนดจำนวนของระดับที่ควรแสดงถ้าคุณสมบัติ **เมนูการนำทางหลายระดับ** ตั้งค่าเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="e0df6-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="e0df6-135">รายการเมนูแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="e0df6-135">Static menu item</span></span>| <span data-ttu-id="e0df6-136">อาร์เรย์ของค่า</span><span class="sxs-lookup"><span data-stu-id="e0df6-136">Array of values</span></span>| <span data-ttu-id="e0df6-137">รายการเมนูแบบคงที่เชื่อมโยงชื่อรายการเมนูกับลิงก์ไปยังหน้าของไซต์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="e0df6-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="e0df6-138">คุณสามารถสร้างรายการเมนูด้านล่างรายการเมนูอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e0df6-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="e0df6-139">ตามค่าเริ่มต้น เมนูแบบคงที่จะปรากฏที่ระดับรากและจะถูกผนวกเข้ากับลำดับชั้นการนำทางของช่องทาง ถ้ามีอยู่</span><span class="sxs-lookup"><span data-stu-id="e0df6-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="e0df6-140">แสดงเมนูราก</span><span class="sxs-lookup"><span data-stu-id="e0df6-140">Show root menu</span></span> | <span data-ttu-id="e0df6-141">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="e0df6-141">**True** or **False**</span></span> | <span data-ttu-id="e0df6-142">เมื่อเปิดใช้คุณสมบัตินี้ เมนูนำทางสามารถกำหนดได้ภายใต้รากที่กำหนดเอง (ตัวอย่างเช่น **ซื้อตอนนี้** )</span><span class="sxs-lookup"><span data-stu-id="e0df6-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now** ).</span></span> <span data-ttu-id="e0df6-143">คุณลักษณะนี้พร้อมใช้งานใน Dynamics 365 Commerce การเผยแพร่ 10.0.15</span><span class="sxs-lookup"><span data-stu-id="e0df6-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="e0df6-144">เมนูราก</span><span class="sxs-lookup"><span data-stu-id="e0df6-144">Root menu</span></span> | <span data-ttu-id="e0df6-145">สตริง</span><span class="sxs-lookup"><span data-stu-id="e0df6-145">string</span></span> | <span data-ttu-id="e0df6-146">คุณสมบัตินี้สามารถใช้ในการกำหนดข้อความสำหรับรากแบบกำหนดเองถ้าคุณสมบัติ **แสดงเมนูราก** ถูกตั้งค่าเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="e0df6-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="e0df6-147">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรูปภาพประเภทที่แสดงอยู่บนเมนูนำทางสำหรับไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e0df6-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="e0df6-148">![ตัวอย่างของโมดูลนำทางที่มีรูปภาพประเภท](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="e0df6-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="e0df6-149">เพิ่มโมดูลเมนูนำทางให้กับโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="e0df6-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="e0df6-150">สำหรับรายละเอียดเกี่ยวกับวิธีการเพิ่มโมดูลเมนูนำทางให้กับโมดูลส่วนหัว ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="e0df6-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0df6-151">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e0df6-151">Additional resources</span></span>

[<span data-ttu-id="e0df6-152">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="e0df6-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e0df6-153">โมดูลการแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="e0df6-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="e0df6-154">โมดูลตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="e0df6-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="e0df6-155">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="e0df6-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e0df6-156">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="e0df6-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="e0df6-157">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="e0df6-157">Header module</span></span>](author-header-module.md)
