---
title: เลือกกำหนดการนำทางของไซต์
description: หัวข้อนี้จะอธิบายเกี่ยวกับวิธีการสร้างลำดับชั้นการนำทางออนไลน์ที่กำหนดเองเพื่อจัดการผลิตภัณฑ์ของคุณสำหรับการเรียกดูบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799360"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="db76f-103">เลือกกำหนดการนำทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="db76f-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db76f-104">หัวข้อนี้จะอธิบายเกี่ยวกับวิธีการสร้างลำดับชั้นการนำทางออนไลน์ที่กำหนดเองเพื่อจัดการผลิตภัณฑ์ของคุณสำหรับการเรียกดูบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="db76f-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="db76f-105">หน้าร้านออนไลน์โดยทั่วไปจะให้ลูกค้าค้นพบและเลือกดูผลิตภัณฑ์โดยใช้การนำทางตามประเภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="db76f-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="db76f-106">โดยทั่วไปจะมีการจัดเรียงตามแท็บที่ด้านบนของหน้าหรือโดยแถบนำทางทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="db76f-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="db76f-107">ใน Dynamics 365 Commerce คุณสามารถสร้างและจัดการโครงสร้างลำดับชั้นของการนำทางประเภทของคุณและผลิตภัณฑ์ที่รวมอยู่ในประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="db76f-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="db76f-108">สร้างลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="db76f-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="db76f-109">ในการสร้างลำดับชั้นการนำทางของช่องทาง ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="db76f-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="db76f-110">ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ประเภทและการจัดการผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="db76f-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="db76f-111">เลือก **การจัดประเภทตามลำดับชั้น** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="db76f-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="db76f-112">ตั้งชื่อการลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="db76f-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db76f-113">ประเภทสูงสุดที่คุณสร้างคือโหนดประเภทราก</span><span class="sxs-lookup"><span data-stu-id="db76f-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="db76f-114">จะไม่มีการแสดงบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="db76f-114">It won't be shown on your site.</span></span> <span data-ttu-id="db76f-115">เมื่อต้องการสร้างการจัดประเภทตามลำดับชั้นที่โหนดระดับบนสุดหนึ่งๆ จะแสดงบนไซต์ของคุณ ให้สร้างและตั้งชื่อประเภทเป็นรองของประเภทราก</span><span class="sxs-lookup"><span data-stu-id="db76f-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="db76f-116">เลือก **โหนดประเภทใหม่** และตั้งชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="db76f-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="db76f-117">ดำเนินการต่อเพื่อสร้างประเภทระดับเดียวกันและประเภทรองตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="db76f-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="db76f-118">ขณะนี้คุณสามารถกำหนดผลิตภัณฑ์ให้กับแต่ละประเภทที่คุณสร้างไว้ภายใต้ประเภทระดับบนสุด</span><span class="sxs-lookup"><span data-stu-id="db76f-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="db76f-119">การกำหนดลำดับของประเภทด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="db76f-119">Customize the order of categories</span></span>

<span data-ttu-id="db76f-120">ตามค่าเริ่มต้นประเภทที่คุณกำหนดจะปรากฏตามลำดับตัวอักษรบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="db76f-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="db76f-121">คุณยังสามารถกำหนดลำดับการแสดงผลของประเภทได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="db76f-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="db76f-122">กำหนดชนิดของการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="db76f-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="db76f-123">ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ประเภทและการจัดการผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="db76f-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="db76f-124">เลือก **การจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="db76f-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="db76f-125">จากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดประเภทตามลำดับชั้น** ในกลุ่ม **การตั้งค่า** ให้เลือก **เชื่อมโยงการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="db76f-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="db76f-126">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="db76f-126">Select **New**.</span></span>
1. <span data-ttu-id="db76f-127">ในฟิลด์ **ชนิดของลำดับชั้นของประเภท** เลือก **ลำดับชั้นการนำทางของช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="db76f-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="db76f-128">ในฟิลด์ **การจัดประเภทตามลำดับชั้น** ให้เลือกลำดับชั้นการนำทางช่องทางที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="db76f-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="db76f-129">เผยแพร่ลำดับชั้นการนำทางใหม่หรือที่มีการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="db76f-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="db76f-130">เมื่อต้องการให้ลำดับชั้นการนำทางพร้อมใช้งานสำหรับหน้าร้านออนไลน์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="db76f-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="db76f-131">ไปยัง **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ประเภทช่องทางและแอตทริบิวต์ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="db76f-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="db76f-132">ในแผนภูมิด้านซ้ายให้เลือกร้านค้าออนไลน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="db76f-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="db76f-133">เลือก **เผยแพร่การอัพเดตช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="db76f-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="db76f-134">ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="db76f-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="db76f-135">ในรายการนี้ ให้ค้นหาและเลือก **Job 1040**</span><span class="sxs-lookup"><span data-stu-id="db76f-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="db76f-136">เลือก **รันเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="db76f-136">Select **Run now**.</span></span>
1. <span data-ttu-id="db76f-137">ทำซ้ำขั้นตอนที่ 5 และ 6 สำหรับงาน 1070 และ 1150</span><span class="sxs-lookup"><span data-stu-id="db76f-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="db76f-138">แสดงประเภทบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="db76f-138">Show categories on your site</span></span>

<span data-ttu-id="db76f-139">เมื่อต้องการแสดงการจัดประเภทตามลำดับชั้นบนหน้าร้านออนไลน์ของคุณ คุณต้องเพิ่มโมดูลของเมนูนำทางในตำแหน่งที่เหมาะสมในเท็มเพลตหรือส่วน</span><span class="sxs-lookup"><span data-stu-id="db76f-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="db76f-140">จากนั้นโมดูลเมนูการนำทางจะแสดงลำดับชั้นการนำทางของคุณ หากคุณเผยแพร่ลำดับชั้นนำทางไปยังช่องทางที่ไซต์ของคุณเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="db76f-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="db76f-141">โมดูลของเมนูนำทางที่รวมอยู่ในไลบรารีโมดูล ช่วยให้ผู้ใช้สามารถนำทางไปยังประเภทที่ไม่มีประเภทย่อยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="db76f-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="db76f-142">ถ้าลูกค้าของคุณควรสามารถนำทางไปยังประเภทที่มีประเภทย่อยคุณต้องกำหนดโมดูลของเมนูนำทางด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="db76f-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="db76f-143">เพิ่มตัวเลือกการนำทางแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="db76f-143">Add custom navigation options</span></span>

<span data-ttu-id="db76f-144">คุณสามารถเพิ่มตัวเลือกการนำทางที่ไม่ได้เป็นส่วนหนึ่งของการจัดประเภทตามลำดับชั้นของผลิตภัณฑ์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="db76f-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="db76f-145">ตัวอย่างเช่น เมื่อสิ้นสุดรายการของประเภทผลิตภัณฑ์ คุณสามารถเพิ่มรายการ **ติดต่อเรา** ที่ชี้ไปยังหน้าผู้ติดต่อที่คุณได้สร้างไว้สำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="db76f-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="db76f-146">เมื่อต้องการเพิ่มตัวเลือกการนำทางแบบกำหนดเองลงในเมนูนำทางของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="db76f-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="db76f-147">ในเท็มเพลตหรือส่วนที่คุณต้องการกำหนดเอง ให้เลือกโมดูลเมนูการนำทาง</span><span class="sxs-lookup"><span data-stu-id="db76f-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="db76f-148">ในบานหน้าต่างคุณสมบัติบนแท็บ **ข้อมูล** ให้เลือก **เพิ่มสินค้า** เพื่อสร้างสินค้านำทางของระบบการจัดการเนื้อหา (CMS) ใหม่</span><span class="sxs-lookup"><span data-stu-id="db76f-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="db76f-149">ป้อนข้อความลิงก์และ URL</span><span class="sxs-lookup"><span data-stu-id="db76f-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="db76f-150">ทำซ้ำขั้นตอนที่ 2 และ 3 เพื่อเพิ่มตัวเลือกนำทางแบบกำหนดเองเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="db76f-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="db76f-151">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว ให้เลือก **บันทึก** เพื่อบันทึกเท็มเพลตหรือส่วน และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="db76f-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db76f-152">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="db76f-152">Additional resources</span></span>

[<span data-ttu-id="db76f-153">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="db76f-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="db76f-154">ใช้งานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="db76f-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="db76f-155">ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="db76f-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="db76f-156">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="db76f-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="db76f-157">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="db76f-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="db76f-158">สร้าง URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="db76f-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="db76f-159">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="db76f-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
