---
title: โมดูลเมนูนำทาง
description: หัวข้อนี้ครอบคลุมถึงโมดูลเมนูนำทางและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817885"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="8db9a-103">โมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="8db9a-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="8db9a-104">หัวข้อนี้ครอบคลุมถึงโมดูลเมนูนำทางและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8db9a-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8db9a-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="8db9a-105">Overview</span></span>

<span data-ttu-id="8db9a-106">วัตถุประสงค์หลักของโมดูลนำทางเมนูคือเพื่ออนุญาตให้ผู้ใช้ไซต์สามารถเรียกดูผลิตภัณฑ์และหน้าของไซต์ตามลำดับชั้นการนำทางของช่องทางที่กำหนดไว้ในศูนย์ควบคุม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8db9a-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="8db9a-107">สินค้าที่ได้รับการตั้งค่าคอนฟิกไว้ในโมดูลตัวเลือกเมนูนำทางจะปรากฏเป็นการนำทางในส่วนหัวของไซต์</span><span class="sxs-lookup"><span data-stu-id="8db9a-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="8db9a-108">โมดูลเมนูนำทางยังสนับสนุนรายการเมนูแบบคงที่ที่เชื่อมโยงไปยังหน้าอื่นๆ บนไซต์อีคอมเมิร์ซด้วย</span><span class="sxs-lookup"><span data-stu-id="8db9a-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="8db9a-109">คุณสามารถเพิ่มโมดูลเมนูนำทางในโมดูลส่วนหัวของหน้าได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8db9a-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="8db9a-110">ในชุดรูปแบบ Fabrikam เมนูนำทางจะแสดงสองระดับตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8db9a-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="8db9a-111">ในชุดรูปแบบชุดเริ่มต้น เมนูนำทางจะแสดงสามระดับตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8db9a-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="8db9a-112">เมื่อต้องการเปลี่ยนแปลงจำนวนระดับ จะต้องใช้ส่วนขยายสำหรับมุมมองในชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="8db9a-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="8db9a-113">ภาพประกอบต่อไปนี้แสดงตัวอย่างของเมนูนำทางสำหรับไซต์ Fabrikam ที่มีการจัดประเภทตามลำดับชั้นสองระดับและรายการเมนูแบบคงที่บางส่วน</span><span class="sxs-lookup"><span data-stu-id="8db9a-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="8db9a-114">![ตัวอย่างของโมดูลการนำทาง](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="8db9a-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="8db9a-115">คุณสมบัติของโมดูลเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="8db9a-115">Navigation menu module properties</span></span>

| <span data-ttu-id="8db9a-116">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="8db9a-116">Property name</span></span>             | <span data-ttu-id="8db9a-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="8db9a-117">Value</span></span>                 | <span data-ttu-id="8db9a-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8db9a-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="8db9a-119">ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="8db9a-119">Source</span></span>                  | <span data-ttu-id="8db9a-120">**การขายปลีก**, **การสร้างด้วยตนเอง**, **การขายปลีกและการสร้างด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="8db9a-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="8db9a-121">ค่าของ **การขายปลีก** จะช่วยให้สามารถแสดงลำดับชั้นการนำทางของช่องทางจากศูนย์ควบคุม Commerce เพื่อแสดงบนเมนูนำทาง</span><span class="sxs-lookup"><span data-stu-id="8db9a-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="8db9a-122">ค่า **การสร้างด้วยตนเอง** จะช่วยให้สามารถระบุรายการเมนูแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="8db9a-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="8db9a-123">ค่าของ **การขายปลีกและการสร้างด้วยตนเอง** จะช่วยให้สามารถผสมผสานกันได้ทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="8db9a-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="8db9a-124">แสดงรูปภาพประเภท</span><span class="sxs-lookup"><span data-stu-id="8db9a-124">Show category images</span></span> | <span data-ttu-id="8db9a-125">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="8db9a-125">**True** or **False**</span></span>    | <span data-ttu-id="8db9a-126">เมื่อเปิดใช้งาน คุณสมบัตินี้จะแสดงรูปภาพประเภทบนเมนูนำทางตามที่กำหนดไว้ในศูนย์ควบคุม Commerce สำหรับแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="8db9a-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="8db9a-127">มีการเพิ่มใน Commerce รีลีส 10.0.14</span><span class="sxs-lookup"><span data-stu-id="8db9a-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="8db9a-128">รายการเมนูแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="8db9a-128">Static menu item</span></span>| <span data-ttu-id="8db9a-129">อาร์เรย์ของค่า</span><span class="sxs-lookup"><span data-stu-id="8db9a-129">Array of values</span></span>| <span data-ttu-id="8db9a-130">รายการเมนูแบบคงที่เชื่อมโยงชื่อรายการเมนูกับลิงก์ไปยังหน้าของไซต์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="8db9a-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="8db9a-131">คุณสามารถสร้างรายการเมนูด้านล่างรายการเมนูอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="8db9a-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="8db9a-132">ตามค่าเริ่มต้น เมนูแบบคงที่จะปรากฏที่ระดับรากและจะถูกผนวกเข้ากับลำดับชั้นการนำทางของช่องทาง ถ้ามีอยู่</span><span class="sxs-lookup"><span data-stu-id="8db9a-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="8db9a-133">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรูปภาพประเภทที่แสดงอยู่บนเมนูนำทางสำหรับไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="8db9a-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="8db9a-134">![ตัวอย่างของโมดูลนำทางที่มีรูปภาพประเภท](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="8db9a-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="8db9a-135">เพิ่มโมดูลเมนูนำทางให้กับโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="8db9a-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="8db9a-136">สำหรับรายละเอียดเกี่ยวกับวิธีการเพิ่มโมดูลเมนูนำทางให้กับโมดูลส่วนหัว ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="8db9a-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8db9a-137">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8db9a-137">Additional resources</span></span>

[<span data-ttu-id="8db9a-138">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="8db9a-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8db9a-139">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="8db9a-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8db9a-140">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="8db9a-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="8db9a-141">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="8db9a-141">Header module</span></span>](author-header-module.md)
