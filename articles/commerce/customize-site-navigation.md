---
title: เลือกกำหนดการนำทางของไซต์
description: หัวข้อนี้จะอธิบายเกี่ยวกับวิธีการสร้างลำดับชั้นการนำทางออนไลน์ที่กำหนดเองได้ เพื่อจัดระเบียบผลิตภัณฑ์ของคุณสำหรับการเรียกดูบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: bicyclingfool
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae7696dcb5cdd99cd46b89ed1de1b03c16146e2d
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269670"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="e7aa4-103">เลือกกำหนดการนำทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="e7aa4-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e7aa4-104">หัวข้อนี้จะอธิบายเกี่ยวกับวิธีการสร้างลำดับชั้นการนำทางออนไลน์ที่กำหนดเองได้ เพื่อจัดระเบียบผลิตภัณฑ์ของคุณสำหรับการเรียกดูบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="e7aa4-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e7aa4-105">Overview</span></span>

<span data-ttu-id="e7aa4-106">หน้าร้านออนไลน์โดยทั่วไปจะให้ลูกค้าค้นพบและเลือกดูผลิตภัณฑ์โดยใช้การนำทางตามประเภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7aa4-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="e7aa4-107">โดยทั่วไปจะมีการจัดเรียงตามแท็บที่ด้านบนของหน้าหรือโดยแถบนำทางทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="e7aa4-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="e7aa4-108">ใน Dynamics 365 Commerce คุณสามารถสร้างและจัดการโครงสร้างลำดับชั้นของการนำทางประเภทของคุณและผลิตภัณฑ์ที่รวมอยู่ในประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="e7aa4-109">สร้างลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="e7aa4-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="e7aa4-110">ในการสร้างลำดับชั้นการนำทางของช่องทาง ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e7aa4-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="e7aa4-111">ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ประเภทและการจัดการผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="e7aa4-112">เลือก **การจัดประเภทตามลำดับชั้น** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="e7aa4-113">ตั้งชื่อการลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="e7aa4-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7aa4-114">ประเภทสูงสุดที่คุณสร้างคือโหนดประเภทราก</span><span class="sxs-lookup"><span data-stu-id="e7aa4-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="e7aa4-115">จะไม่มีการแสดงบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-115">It won't be shown on your site.</span></span> <span data-ttu-id="e7aa4-116">เมื่อต้องการสร้างการจัดประเภทตามลำดับชั้นที่โหนดระดับบนสุดหนึ่งๆ จะแสดงบนไซต์ของคุณ ให้สร้างและตั้งชื่อประเภทเป็นรองของประเภทราก</span><span class="sxs-lookup"><span data-stu-id="e7aa4-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="e7aa4-117">เลือก **โหนดประเภทใหม่** และตั้งชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="e7aa4-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="e7aa4-118">ดำเนินการต่อเพื่อสร้างประเภทระดับเดียวกันและประเภทรองตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="e7aa4-119">ขณะนี้คุณสามารถกำหนดผลิตภัณฑ์ให้กับแต่ละประเภทที่คุณสร้างไว้ภายใต้ประเภทระดับบนสุด</span><span class="sxs-lookup"><span data-stu-id="e7aa4-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="e7aa4-120">การกำหนดลำดับของประเภทด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="e7aa4-120">Customize the order of categories</span></span>

<span data-ttu-id="e7aa4-121">ตามค่าเริ่มต้นประเภทที่คุณกำหนดจะปรากฏตามลำดับตัวอักษรบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="e7aa4-122">คุณยังสามารถกำหนดลำดับการแสดงผลของประเภทได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="e7aa4-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="e7aa4-123">กำหนดชนิดของการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="e7aa4-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="e7aa4-124">ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ประเภทและการจัดการผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="e7aa4-125">เลือก **การจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="e7aa4-126">จากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดประเภทตามลำดับชั้น** ในกลุ่ม **การตั้งค่า** ให้เลือก **เชื่อมโยงการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="e7aa4-127">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-127">Select **New**.</span></span>
1. <span data-ttu-id="e7aa4-128">ในฟิลด์ **ชนิดของลำดับชั้นของประเภท** เลือก **ลำดับชั้นการนำทางของช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="e7aa4-129">ในฟิลด์ **การจัดประเภทตามลำดับชั้น** ให้เลือกลำดับชั้นการนำทางช่องทางที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e7aa4-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="e7aa4-130">เผยแพร่ลำดับชั้นการนำทางใหม่หรือที่มีการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="e7aa4-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="e7aa4-131">เมื่อต้องการให้ลำดับชั้นการนำทางพร้อมใช้งานสำหรับหน้าร้านออนไลน์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e7aa4-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="e7aa4-132">ไปยัง **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ประเภทช่องทางและแอตทริบิวต์ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="e7aa4-133">ในแผนภูมิด้านซ้ายให้เลือกร้านค้าออนไลน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="e7aa4-134">เลือก **เผยแพร่การอัพเดตช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="e7aa4-135">ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="e7aa4-136">ในรายการนี้ ให้ค้นหาและเลือก **Job 1040**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="e7aa4-137">เลือก **รันเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="e7aa4-137">Select **Run now**.</span></span>
1. <span data-ttu-id="e7aa4-138">ทำซ้ำขั้นตอนที่ 5 และ 6 สำหรับงาน 1070 และ 1150</span><span class="sxs-lookup"><span data-stu-id="e7aa4-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="e7aa4-139">แสดงประเภทบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-139">Show categories on your site</span></span>

<span data-ttu-id="e7aa4-140">เมื่อต้องการแสดงการจัดประเภทตามลำดับชั้นบนหน้าร้านออนไลน์ของคุณ คุณต้องเพิ่มโมดูลของเมนูนำทางในตำแหน่งที่เหมาะสมในเท็มเพลตหรือส่วน</span><span class="sxs-lookup"><span data-stu-id="e7aa4-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="e7aa4-141">จากนั้นโมดูลเมนูการนำทางจะแสดงลำดับชั้นการนำทางของคุณ หากคุณเผยแพร่ลำดับชั้นนำทางไปยังช่องทางที่ไซต์ของคุณเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="e7aa4-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="e7aa4-142">โมดูลของเมนูนำทางที่รวมอยู่ในชุดเริ่มต้นของร้านค้าช่วยให้ผู้ใช้สามารถนำทางไปยังประเภทที่ไม่มีประเภทย่อยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e7aa4-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="e7aa4-143">ถ้าลูกค้าของคุณควรสามารถนำทางไปยังประเภทที่มีประเภทย่อยคุณต้องกำหนดโมดูลของเมนูนำทางด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="e7aa4-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="e7aa4-144">เพิ่มตัวเลือกการนำทางแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="e7aa4-144">Add custom navigation options</span></span>

<span data-ttu-id="e7aa4-145">คุณสามารถเพิ่มตัวเลือกการนำทางที่ไม่ได้เป็นส่วนหนึ่งของการจัดประเภทตามลำดับชั้นของผลิตภัณฑ์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="e7aa4-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="e7aa4-146">ตัวอย่างเช่น เมื่อสิ้นสุดรายการของประเภทผลิตภัณฑ์ คุณสามารถเพิ่มรายการ **ติดต่อเรา** ที่ชี้ไปยังหน้าผู้ติดต่อที่คุณได้สร้างไว้สำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="e7aa4-147">เมื่อต้องการเพิ่มตัวเลือกการนำทางแบบกำหนดเองลงในเมนูนำทางของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e7aa4-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="e7aa4-148">ในเท็มเพลตหรือส่วนที่คุณต้องการกำหนดเอง ให้เลือกโมดูลเมนูการนำทาง</span><span class="sxs-lookup"><span data-stu-id="e7aa4-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="e7aa4-149">ในบานหน้าต่างคุณสมบัติบนแท็บ **ข้อมูล** ให้เลือก **เพิ่มสินค้า** เพื่อสร้างสินค้านำทางของระบบการจัดการเนื้อหา (CMS) ใหม่</span><span class="sxs-lookup"><span data-stu-id="e7aa4-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="e7aa4-150">ป้อนข้อความลิงก์และ URL</span><span class="sxs-lookup"><span data-stu-id="e7aa4-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="e7aa4-151">ทำซ้ำขั้นตอนที่ 2 และ 3 เพื่อเพิ่มตัวเลือกนำทางแบบกำหนดเองเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e7aa4-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="e7aa4-152">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว ให้เลือก **บันทึก** เพื่อบันทึกเท็มเพลตหรือส่วน และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="e7aa4-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7aa4-153">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e7aa4-153">Additional resources</span></span>

[<span data-ttu-id="e7aa4-154">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="e7aa4-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e7aa4-155">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="e7aa4-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="e7aa4-156">ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="e7aa4-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="e7aa4-157">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="e7aa4-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="e7aa4-158">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="e7aa4-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="e7aa4-159">สร้าง URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="e7aa4-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="e7aa4-160">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="e7aa4-160">Work with publish groups</span></span>](publish-groups.md)
