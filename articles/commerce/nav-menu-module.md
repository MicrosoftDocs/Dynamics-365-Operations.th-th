---
title: โมดูลเมนูนำทาง
description: หัวข้อนี้ครอบคลุมถึงโมดูลเมนูนำทางและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b112bb453e0840120c63038bf8d6897fbf5ff288
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798764"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="2ea74-103">โมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="2ea74-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2ea74-104">หัวข้อนี้ครอบคลุมถึงโมดูลเมนูนำทางและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2ea74-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2ea74-105">วัตถุประสงค์หลักของโมดูลนำทางเมนูคือเพื่ออนุญาตให้ผู้ใช้ไซต์สามารถเรียกดูผลิตภัณฑ์และหน้าของไซต์ตามลำดับชั้นการนำทางของช่องทางที่กำหนดไว้ในศูนย์ควบคุม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2ea74-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="2ea74-106">สินค้าที่ได้รับการตั้งค่าคอนฟิกไว้ในโมดูลตัวเลือกเมนูนำทางจะปรากฏเป็นการนำทางในส่วนหัวของไซต์</span><span class="sxs-lookup"><span data-stu-id="2ea74-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="2ea74-107">โมดูลเมนูนำทางยังสนับสนุนรายการเมนูแบบคงที่ที่เชื่อมโยงไปยังหน้าอื่นๆ บนไซต์อีคอมเมิร์ซด้วย</span><span class="sxs-lookup"><span data-stu-id="2ea74-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="2ea74-108">คุณสามารถเพิ่มโมดูลเมนูนำทางในโมดูลส่วนหัวของหน้าได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="2ea74-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="2ea74-109">ในชุดรูปแบบ Fabrikam เมนูนำทางจะแสดงสองระดับตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2ea74-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="2ea74-110">ในชุดรูปแบบชุดเริ่มต้น เมนูนำทางจะแสดงสามระดับตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2ea74-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="2ea74-111">เมื่อต้องการเปลี่ยนแปลงจำนวนระดับ จะต้องใช้ส่วนขยายสำหรับมุมมองในชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="2ea74-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="2ea74-112">ภาพประกอบต่อไปนี้แสดงตัวอย่างของเมนูนำทางสำหรับไซต์ Fabrikam ที่มีการจัดประเภทตามลำดับชั้นสองระดับและรายการเมนูแบบคงที่บางส่วน</span><span class="sxs-lookup"><span data-stu-id="2ea74-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="2ea74-113">![ตัวอย่างของโมดูลการนำทาง](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="2ea74-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="2ea74-114">คุณสมบัติของโมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="2ea74-114">Navigation menu module properties</span></span>

| <span data-ttu-id="2ea74-115">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="2ea74-115">Property name</span></span>             | <span data-ttu-id="2ea74-116">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2ea74-116">Value</span></span>                 | <span data-ttu-id="2ea74-117">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2ea74-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2ea74-118">ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="2ea74-118">Source</span></span>                  | <span data-ttu-id="2ea74-119">**การขายปลีก**, **การสร้างด้วยตนเอง**, **การขายปลีกและการสร้างด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="2ea74-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="2ea74-120">ค่าของ **การขายปลีก** จะช่วยให้สามารถแสดงลำดับชั้นการนำทางของช่องทางจากศูนย์ควบคุม Commerce เพื่อแสดงบนเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="2ea74-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="2ea74-121">ค่า **การสร้างด้วยตนเอง** จะช่วยให้สามารถระบุรายการเมนูแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="2ea74-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="2ea74-122">ค่าของ **การขายปลีกและการสร้างด้วยตนเอง** จะช่วยให้สามารถผสมผสานกันได้ทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="2ea74-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="2ea74-123">แสดงรูปภาพประเภท</span><span class="sxs-lookup"><span data-stu-id="2ea74-123">Show category images</span></span> | <span data-ttu-id="2ea74-124">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="2ea74-124">**True** or **False**</span></span>    | <span data-ttu-id="2ea74-125">เมื่อเปิดใช้งาน คุณสมบัตินี้จะแสดงรูปภาพประเภทบนเมนูนำทางตามที่กำหนดไว้ในศูนย์ควบคุม Commerce สำหรับแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="2ea74-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="2ea74-126">มีการเพิ่มใน Commerce รีลีส 10.0.14</span><span class="sxs-lookup"><span data-stu-id="2ea74-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="2ea74-127">แสดงโปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="2ea74-127">Show promotions</span></span> | <span data-ttu-id="2ea74-128">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="2ea74-128">**True** or **False**</span></span> | <span data-ttu-id="2ea74-129">เมื่อเปิดใช้งานคุณสมบัตินี้ คุณสามารถตั้งค่าคอนฟิกโปรโมชันได้โดยใช้รูปภาพ ลิงค์ และข้อความ</span><span class="sxs-lookup"><span data-stu-id="2ea74-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="2ea74-130">คุณสมบัตินี้ถูกเพิ่มลงใน Commerce รุ่น 10.0.17 แล้ว</span><span class="sxs-lookup"><span data-stu-id="2ea74-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="2ea74-131">เพิ่มโปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="2ea74-131">Add promotions</span></span> | <span data-ttu-id="2ea74-132">ข้อความ รูปภาพ หรือลิงก์</span><span class="sxs-lookup"><span data-stu-id="2ea74-132">Text, image, or link</span></span> | <span data-ttu-id="2ea74-133">เมื่อเปิดใช้งานคุณสมบัติ **แสดงโปรโมชัน** คุณสามารถเพิ่มข้อความ รูปภาพ หรือลิงค์เป็นเนื้อหาโปรโมชันในเมนูนําทางได้</span><span class="sxs-lookup"><span data-stu-id="2ea74-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="2ea74-134">เปิดใช้งานเมนูนำทางแบบหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="2ea74-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="2ea74-135">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="2ea74-135">**True** or **False**</span></span> | <span data-ttu-id="2ea74-136">เมื่อเปิดใช้คุณสมบัตินี้ เมนูนำทางสามารถแสดงลำดับชั้นการนำทางหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="2ea74-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="2ea74-137">คุณลักษณะนี้พร้อมใช้งานใน Commerce รุ่น 10.0.15</span><span class="sxs-lookup"><span data-stu-id="2ea74-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="2ea74-138">จำนวนของระดับ</span><span class="sxs-lookup"><span data-stu-id="2ea74-138">Number of levels</span></span> | <span data-ttu-id="2ea74-139">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="2ea74-139">integer</span></span> | <span data-ttu-id="2ea74-140">คุณสมบัตินี้กำหนดจำนวนของระดับที่ควรแสดงถ้าคุณสมบัติ **เมนูการนำทางหลายระดับ** ตั้งค่าเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="2ea74-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="2ea74-141">รายการเมนูแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="2ea74-141">Static menu item</span></span>| <span data-ttu-id="2ea74-142">อาร์เรย์ของค่า</span><span class="sxs-lookup"><span data-stu-id="2ea74-142">Array of values</span></span>| <span data-ttu-id="2ea74-143">รายการเมนูแบบคงที่เชื่อมโยงชื่อรายการเมนูกับลิงก์ไปยังหน้าของไซต์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="2ea74-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="2ea74-144">คุณสามารถสร้างรายการเมนูด้านล่างรายการเมนูอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2ea74-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="2ea74-145">ตามค่าเริ่มต้น เมนูแบบคงที่จะปรากฏที่ระดับรากและจะถูกผนวกเข้ากับลำดับชั้นการนำทางของช่องทาง ถ้ามีอยู่</span><span class="sxs-lookup"><span data-stu-id="2ea74-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="2ea74-146">แสดงเมนูราก</span><span class="sxs-lookup"><span data-stu-id="2ea74-146">Show root menu</span></span> | <span data-ttu-id="2ea74-147">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="2ea74-147">**True** or **False**</span></span> | <span data-ttu-id="2ea74-148">เมื่อเปิดใช้คุณสมบัตินี้ เมนูนำทางสามารถกำหนดได้ภายใต้รากที่กำหนดเอง (ตัวอย่างเช่น **ซื้อตอนนี้**)</span><span class="sxs-lookup"><span data-stu-id="2ea74-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="2ea74-149">คุณลักษณะนี้พร้อมใช้งานใน Dynamics 365 Commerce การเผยแพร่ 10.0.15</span><span class="sxs-lookup"><span data-stu-id="2ea74-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="2ea74-150">เมนูราก</span><span class="sxs-lookup"><span data-stu-id="2ea74-150">Root menu</span></span> | <span data-ttu-id="2ea74-151">สตริง</span><span class="sxs-lookup"><span data-stu-id="2ea74-151">string</span></span> | <span data-ttu-id="2ea74-152">คุณสมบัตินี้สามารถใช้ในการกำหนดข้อความสำหรับรากแบบกำหนดเองถ้าคุณสมบัติ **แสดงเมนูราก** ถูกตั้งค่าเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="2ea74-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="2ea74-153">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรูปภาพประเภทที่แสดงอยู่บนเมนูนำทางสำหรับไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="2ea74-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="2ea74-154">![ตัวอย่างของโมดูลนำทางที่มีรูปภาพประเภท](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="2ea74-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="2ea74-155">เพิ่มโมดูลเมนูนำทางให้กับโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="2ea74-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="2ea74-156">สำหรับรายละเอียดเกี่ยวกับวิธีการเพิ่มโมดูลเมนูนำทางให้กับโมดูลส่วนหัว ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="2ea74-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ea74-157">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2ea74-157">Additional resources</span></span>

[<span data-ttu-id="2ea74-158">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="2ea74-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2ea74-159">โมดูลการแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="2ea74-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="2ea74-160">โมดูลตัวเลือกไซต์</span><span class="sxs-lookup"><span data-stu-id="2ea74-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="2ea74-161">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="2ea74-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2ea74-162">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="2ea74-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="2ea74-163">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="2ea74-163">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
