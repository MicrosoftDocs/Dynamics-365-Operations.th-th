---
title: ทำให้หน้าผลิตภัณฑ์สมบูรณ์
description: หัวข้อนี้จะอธิบายวิธีการทำให้หน้าผลิตภัณฑ์สมบูรณ์ใน Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: ef9e65b2027a41ca152afaf20ac2fb9a69cd9b96
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698153"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="39092-103">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="39092-103">Enrich a product page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="39092-104">หัวข้อนี้จะอธิบายวิธีการทำให้หน้าผลิตภัณฑ์สมบูรณ์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39092-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="39092-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="39092-105">Overview</span></span>

<span data-ttu-id="39092-106">โดยค่าเริ่มต้น ไซต์ของคุณจะใช้หน้าทั่วไปเพื่อแสดงข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="39092-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="39092-107">หน้านี้ประกอบด้วยข้อมูลพื้นฐานเกี่ยวกับผลิตภัณฑ์และตัวควบคุมที่จำเป็นต้องใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="39092-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="39092-108">อย่างไรก็ตาม คุณสามารถให้ข้อมูลเพิ่มเติมเกี่ยวกับข้อมูลที่มาจากเซิร์ฟเวอร์ Retail โดยมีรูปภาพหรือข้อความเพิ่มเติมสำหรับผลิตภัณฑ์หนึ่ง ๆ</span><span class="sxs-lookup"><span data-stu-id="39092-108">However, you can supplement the information that comes from the Retail Server with additional images or text for a specific product.</span></span> <span data-ttu-id="39092-109">กระบวนการนี้เรียกว่าการทำให้สินค้าในหน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="39092-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="39092-110">ในหลายกรณี คุณจะต้องใช้เนื้อหาเพิ่มเติมเฉพาะสำหรับผลิตภัณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="39092-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="39092-111">เมื่อคุณไปที่ **Retail** ในเครื่องมือการสร้าง คุณจะเห็นรายการผลิตภัณฑ์จากช่องทางที่กำหนดให้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="39092-111">When you go to **Retail** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="39092-112">ในรายการนี้คอลัมน์ **สมบูรณ์** บ่งชี้ว่าหน้าผลิตภัณฑ์ของผลิตภัณฑ์สมบูรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="39092-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="39092-113">ถ้ามีเครื่องหมายถูกในคอลัมน์ จะมีหน้าผลิตภัณฑ์ที่สมบูรณ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="39092-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="39092-114">ถ้าไม่มีเครื่องหมายถูก จะใช้หน้าผลิตภัณฑ์เริ่มต้นและเนื้อหาสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="39092-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="39092-115">คุณสามารถดูตัวอย่างทั้งหน้าของประเภทที่สมบูรณ์และไม่สมบูรณ์สำหรับผลิตภัณฑ์ โดยการเลือกชื่อผลิตภัณฑ์ในรายการ</span><span class="sxs-lookup"><span data-stu-id="39092-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="39092-116">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="39092-116">Enrich a product page</span></span>

<span data-ttu-id="39092-117">เมื่อต้องการทำให้ผลิตภัณฑ์สมบูรณ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="39092-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="39092-118">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="39092-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="39092-119">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="39092-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="39092-120">เลือกผลิตภัณฑ์ที่ไม่มีหน้าผลิตภัณฑ์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="39092-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="39092-121">ในบานหน้าต่างการดำเนินการ เลือก **ทำให้หน้าผลิตภัณฑ์สมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="39092-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="39092-122">เลือก **แม่แบบ PDP** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39092-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="39092-123">ในแผนภูมิเค้าร่างของหน้าทางด้านซ้าย ให้ขยายช่อง **หลัก**</span><span class="sxs-lookup"><span data-stu-id="39092-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="39092-124">เลือกปุ่มจุดไข่ปลา (**...**) สำหรับช่อง **หลัก** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39092-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="39092-125">เลือก **คอนเทนเนอร์ 2** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39092-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="39092-126">เลือกปุ่มจุดไข่ปลาสำหรับ **คอนเทนเนอร์ 2** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="39092-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="39092-127">เลือก **คุณลักษณะ** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39092-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="39092-128">ในบานหน้าต่างคุณสมบัติทางด้านขวาในฟิลด์ **Rich Text** ให้ป้อนคำอธิบายที่อัพเดตของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="39092-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="39092-129">ในฟิลด์ **ส่วนหัว** ให้ป้อนข้อความส่วนหัวแล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39092-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="39092-130">เลือก **บันทึก** แล้วจากนั้น เลือก **เช็คอิน**</span><span class="sxs-lookup"><span data-stu-id="39092-130">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="39092-131">ในฟิลด์ **ข้อคิดเห็น** ป้อน **ทำให้ผลิตภัณฑ์สมบูรณ์**  แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39092-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="39092-132">เลือก **แสดงตัวอย่าง** เพื่อเเสดงตัวอน่างหน้าผลิตภัณฑ์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="39092-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="39092-133">เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="39092-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="39092-134">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="39092-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39092-135">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="39092-135">Additional resources</span></span>

[<span data-ttu-id="39092-136">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="39092-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="39092-137">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="39092-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="39092-138">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="39092-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="39092-139">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="39092-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="39092-140">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="39092-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="39092-141">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="39092-141">Enrich a category landing page</span></span>](enrich-category-page.md)

