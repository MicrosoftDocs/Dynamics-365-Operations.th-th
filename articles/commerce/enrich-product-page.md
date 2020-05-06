---
title: ทำให้หน้าผลิตภัณฑ์สมบูรณ์
description: หัวข้อนี้จะอธิบายวิธีการทำให้หน้าผลิตภัณฑ์สมบูรณ์ใน Microsoft Dynamics 365 Commerce
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12508a80c440894ec6e2073b5e550846480e6c45
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269831"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="3b99c-103">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3b99c-104">หัวข้อนี้จะอธิบายวิธีการทำให้หน้าผลิตภัณฑ์สมบูรณ์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3b99c-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3b99c-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="3b99c-105">Overview</span></span>

<span data-ttu-id="3b99c-106">โดยค่าเริ่มต้น ไซต์ของคุณจะใช้หน้าทั่วไปเพื่อแสดงข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="3b99c-107">หน้านี้ประกอบด้วยข้อมูลพื้นฐานเกี่ยวกับผลิตภัณฑ์และตัวควบคุมที่จำเป็นต้องใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="3b99c-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="3b99c-108">อย่างไรก็ตามคุณสามารถเสริมข้อมูลที่มาจาก Commerce Scale Unit ด้วยภาพหรือข้อความเพิ่มเติมสำหรับผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3b99c-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="3b99c-109">กระบวนการนี้เรียกว่าการทำให้สินค้าในหน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="3b99c-110">ในหลายกรณี คุณจะต้องใช้เนื้อหาเพิ่มเติมเฉพาะสำหรับผลิตภัณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b99c-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="3b99c-111">เมื่อคุณไปยัง **การขายปลีกและการค้า** ในเครื่องมือการเขียน คุณจะเห็นรายการสินค้าจากช่องทางที่ได้รับมอบหมายให้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="3b99c-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="3b99c-112">ในรายการนี้คอลัมน์ **สมบูรณ์** บ่งชี้ว่าหน้าผลิตภัณฑ์ของผลิตภัณฑ์สมบูรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3b99c-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="3b99c-113">ถ้ามีเครื่องหมายถูกในคอลัมน์ จะมีหน้าผลิตภัณฑ์ที่สมบูรณ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="3b99c-114">ถ้าไม่มีเครื่องหมายถูก จะใช้หน้าผลิตภัณฑ์เริ่มต้นและเนื้อหาสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="3b99c-115">คุณสามารถดูตัวอย่างทั้งหน้าของประเภทที่สมบูรณ์และไม่สมบูรณ์สำหรับผลิตภัณฑ์ โดยการเลือกชื่อผลิตภัณฑ์ในรายการ</span><span class="sxs-lookup"><span data-stu-id="3b99c-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="3b99c-116">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-116">Enrich a product page</span></span>

<span data-ttu-id="3b99c-117">เมื่อต้องการทำให้ผลิตภัณฑ์สมบูรณ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b99c-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="3b99c-118">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="3b99c-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="3b99c-119">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="3b99c-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="3b99c-120">เลือกผลิตภัณฑ์ที่ไม่มีหน้าผลิตภัณฑ์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="3b99c-121">ในบานหน้าต่างการดำเนินการ เลือก **ทำให้หน้าผลิตภัณฑ์สมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="3b99c-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="3b99c-122">เลือก **แม่แบบ PDP** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3b99c-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b99c-123">ในแผนภูมิเค้าร่างของหน้าทางด้านซ้าย ให้ขยายช่อง **หลัก**</span><span class="sxs-lookup"><span data-stu-id="3b99c-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="3b99c-124">เลือกปุ่มจุดไข่ปลา (**...**) สำหรับช่อง **หลัก** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="3b99c-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="3b99c-125">เลือก **คอนเทนเนอร์ 2** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3b99c-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b99c-126">เลือกปุ่มจุดไข่ปลาสำหรับ **คอนเทนเนอร์ 2** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="3b99c-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="3b99c-127">เลือก **คุณลักษณะ** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3b99c-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b99c-128">ในบานหน้าต่างคุณสมบัติทางด้านขวาในฟิลด์ **Rich Text** ให้ป้อนคำอธิบายที่อัพเดตของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="3b99c-129">ในฟิลด์ **ส่วนหัว** ให้ป้อนข้อความส่วนหัวแล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3b99c-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="3b99c-130">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="3b99c-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="3b99c-131">ในฟิลด์ **ข้อคิดเห็น** ป้อน **ทำให้ผลิตภัณฑ์สมบูรณ์**  แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3b99c-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b99c-132">เลือก **แสดงตัวอย่าง** เพื่อเเสดงตัวอน่างหน้าผลิตภัณฑ์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="3b99c-133">เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="3b99c-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="3b99c-134">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="3b99c-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b99c-135">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3b99c-135">Additional resources</span></span>

[<span data-ttu-id="3b99c-136">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3b99c-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="3b99c-137">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="3b99c-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="3b99c-138">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="3b99c-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="3b99c-139">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="3b99c-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="3b99c-140">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="3b99c-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="3b99c-141">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b99c-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="3b99c-142">ตรวจสอบการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="3b99c-142">Verify page content accessibility</span></span>](verify-accessibility.md)
