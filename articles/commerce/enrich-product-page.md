---
title: ทำให้หน้าผลิตภัณฑ์สมบูรณ์
description: หัวข้อนี้จะอธิบายวิธีการทำให้หน้าผลิตภัณฑ์สมบูรณ์ใน Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799067"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="4bd91-103">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4bd91-104">หัวข้อนี้จะอธิบายวิธีการทำให้หน้าผลิตภัณฑ์สมบูรณ์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4bd91-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4bd91-105">โดยค่าเริ่มต้น ไซต์ของคุณจะใช้หน้าทั่วไปเพื่อแสดงข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="4bd91-106">หน้านี้ประกอบด้วยข้อมูลพื้นฐานเกี่ยวกับผลิตภัณฑ์และตัวควบคุมที่จำเป็นต้องใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="4bd91-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="4bd91-107">อย่างไรก็ตามคุณสามารถเสริมข้อมูลที่มาจาก Commerce Scale Unit ด้วยภาพหรือข้อความเพิ่มเติมสำหรับผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="4bd91-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="4bd91-108">กระบวนการนี้เรียกว่าการทำให้สินค้าในหน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="4bd91-109">ในหลายกรณี คุณจะต้องใช้เนื้อหาเพิ่มเติมเฉพาะสำหรับผลิตภัณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4bd91-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="4bd91-110">เมื่อคุณไปยัง **การขายปลีกและการค้า** ในเครื่องมือการเขียน คุณจะเห็นรายการสินค้าจากช่องทางที่ได้รับมอบหมายให้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="4bd91-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="4bd91-111">ในรายการนี้คอลัมน์ **สมบูรณ์** บ่งชี้ว่าหน้าผลิตภัณฑ์ของผลิตภัณฑ์สมบูรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="4bd91-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="4bd91-112">ถ้ามีเครื่องหมายถูกในคอลัมน์ จะมีหน้าผลิตภัณฑ์ที่สมบูรณ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="4bd91-113">ถ้าไม่มีเครื่องหมายถูก จะใช้หน้าผลิตภัณฑ์เริ่มต้นและเนื้อหาสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="4bd91-114">คุณสามารถดูตัวอย่างทั้งหน้าของประเภทที่สมบูรณ์และไม่สมบูรณ์สำหรับผลิตภัณฑ์ โดยการเลือกชื่อผลิตภัณฑ์ในรายการ</span><span class="sxs-lookup"><span data-stu-id="4bd91-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="4bd91-115">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-115">Enrich a product page</span></span>

<span data-ttu-id="4bd91-116">เมื่อต้องการทำให้ผลิตภัณฑ์สมบูรณ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4bd91-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="4bd91-117">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="4bd91-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4bd91-118">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="4bd91-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="4bd91-119">เลือกผลิตภัณฑ์ที่ไม่มีหน้าผลิตภัณฑ์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="4bd91-120">ในบานหน้าต่างการดำเนินการ เลือก **ทำให้หน้าผลิตภัณฑ์สมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="4bd91-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="4bd91-121">เลือก **แม่แบบ PDP** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4bd91-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="4bd91-122">ในแผนภูมิเค้าร่างของหน้าทางด้านซ้าย ให้ขยายช่อง **หลัก**</span><span class="sxs-lookup"><span data-stu-id="4bd91-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="4bd91-123">เลือกปุ่มจุดไข่ปลา (**...**) สำหรับช่อง **หลัก** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4bd91-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4bd91-124">เลือก **คอนเทนเนอร์ 2** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4bd91-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="4bd91-125">เลือกปุ่มจุดไข่ปลาสำหรับ **คอนเทนเนอร์ 2** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4bd91-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4bd91-126">เลือก **คุณลักษณะ** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4bd91-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="4bd91-127">ในบานหน้าต่างคุณสมบัติทางด้านขวาในฟิลด์ **Rich Text** ให้ป้อนคำอธิบายที่อัพเดตของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="4bd91-128">ในฟิลด์ **ส่วนหัว** ให้ป้อนข้อความส่วนหัวแล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4bd91-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="4bd91-129">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="4bd91-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4bd91-130">ในฟิลด์ **ข้อคิดเห็น** ป้อน **ทำให้ผลิตภัณฑ์สมบูรณ์**  แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4bd91-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="4bd91-131">เลือก **แสดงตัวอย่าง** เพื่อเเสดงตัวอน่างหน้าผลิตภัณฑ์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="4bd91-132">เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="4bd91-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="4bd91-133">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="4bd91-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4bd91-134">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4bd91-134">Additional resources</span></span>

[<span data-ttu-id="4bd91-135">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4bd91-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="4bd91-136">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="4bd91-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="4bd91-137">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="4bd91-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="4bd91-138">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="4bd91-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="4bd91-139">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="4bd91-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="4bd91-140">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4bd91-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="4bd91-141">ตรวจสอบการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="4bd91-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="4bd91-142">สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์บน URL</span><span class="sxs-lookup"><span data-stu-id="4bd91-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
