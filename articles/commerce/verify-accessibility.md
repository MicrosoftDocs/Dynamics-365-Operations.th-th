---
title: ตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้า
description: หัวข้อนี้จะอธิบายวิธีการตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้าใน Microsoft Dynamics 365 Commerce
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7690f3bb17a56b9a16b6e818b675064b1979948e
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097376"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="dd4c5-103">ตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="dd4c5-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dd4c5-104">หัวข้อนี้จะอธิบายวิธีการตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dd4c5-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dd4c5-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="dd4c5-105">Overview</span></span>

<span data-ttu-id="dd4c5-106">เมื่อคุณเปลี่ยนหน้าเสร็จแล้ว คุณควรตรวจสอบให้แน่ใจว่าเนื้อหานั้นสามารถเข้าถึงได้สำหรับทุกคนบนเว็บ</span><span class="sxs-lookup"><span data-stu-id="dd4c5-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="dd4c5-107">ในเครื่องมือการสร้าง Commerce คุณสามารถตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้าได้อย่างง่ายดายโดยใช้บริการ [Microsoft Accessibility Insights](https://accessibilityinsights.io/)</span><span class="sxs-lookup"><span data-stu-id="dd4c5-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="dd4c5-108">บริการนี้จะตรวจสอบเนื้อหาของเพจของคุณเทียบกับแนวทาง [ความสามารถในการเข้าถึง World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility) ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="dd4c5-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="dd4c5-109">การรวม [Microsoft Accessibility Insights](https://accessibilityinsights.io/) ต้องถูกเปิดอยู่ที่ระดับผู้เช่าหรือระดับไซต์ ก่อนที่คุณจะสามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="dd4c5-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="dd4c5-110">เปิดใช้งาน Microsoft Accessibility Insights สำหรับไซต์ทั้งหมดในผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="dd4c5-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="dd4c5-111">เมื่อต้องการเปิดใช้งานการรวม [Microsoft Accessibility Insights](https://accessibilityinsights.io/) สำหรับไซต์ Commerce ทั้งหมดในผู้เช่าของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dd4c5-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="dd4c5-112">เมื่อต้องการเข้าถึงการตั้งค่าผู้เช่า คุณต้องลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="dd4c5-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="dd4c5-113">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="dd4c5-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="dd4c5-114">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="dd4c5-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="dd4c5-115">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **คุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="dd4c5-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="dd4c5-116">ตั้งค่าตัวเลือก **ตรวจสอบความสามารถในการเข้าถึง** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="dd4c5-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="dd4c5-117">เปิดใช้งาน Microsoft Accessibility Insights สำหรับไซต์เดียว</span><span class="sxs-lookup"><span data-stu-id="dd4c5-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="dd4c5-118">เมื่อต้องการเปิดใช้งานการรวม [Microsoft Accessibility Insights](https://accessibilityinsights.io/) สำหรับไซต์ Commerce เดียว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dd4c5-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="dd4c5-119">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="dd4c5-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="dd4c5-120">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="dd4c5-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="dd4c5-121">ภายใต้ **การตั้งค่าไซต์** ให้เลือก **คุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="dd4c5-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="dd4c5-122">ตั้งค่าตัวเลือก **ตรวจสอบความสามารถในการเข้าถึง** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="dd4c5-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="dd4c5-123">ตรวจสอบความสามารถในการเข้าถึงเนื้อหาบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="dd4c5-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="dd4c5-124">หากต้องการใช้บริการ [Microsoft Accessibility Insights](https://accessibilityinsights.io/) แบบรวม เพื่อสแกนและตรวจสอบเนื้อหาของโฮมเพจของคุณใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dd4c5-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="dd4c5-125">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="dd4c5-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="dd4c5-126">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **หน้า**</span><span class="sxs-lookup"><span data-stu-id="dd4c5-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="dd4c5-127">ค้นหาและเลือกหน้าหลัก เพื่อเปิดในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="dd4c5-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="dd4c5-128">บนแถบคำสั่ง ให้เลือก **ตรวจสอบความสามารถในการเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="dd4c5-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="dd4c5-129">หน้า **ตรวจสอบความสามารถในการเข้าถึง** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="dd4c5-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="dd4c5-130">หลังจากการสแกนเสร็จสมบูรณ์ ให้ตรวจทานเนื้อหาของรายงาน</span><span class="sxs-lookup"><span data-stu-id="dd4c5-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="dd4c5-131">ถ้าการตรวจสอบใดๆ ล้มเหลว ให้เลือกรายการตรวจสอบที่ล้มเหลวแต่ละรายการเพื่อขยาย เพื่อให้คุณสามารถดูรายละเอียดเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="dd4c5-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="dd4c5-132">หากต้องการปิดรายงานหลังจากที่คุณตรวจทานเสร็จแล้ว ให้เลื่อนไปที่ด้านล่างของหน้า **ตรวจสอบความสามารถในการเข้าถึง** และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="dd4c5-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd4c5-133">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dd4c5-133">Additional resources</span></span>

[<span data-ttu-id="dd4c5-134">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="dd4c5-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="dd4c5-135">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="dd4c5-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="dd4c5-136">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="dd4c5-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="dd4c5-137">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="dd4c5-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="dd4c5-138">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="dd4c5-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="dd4c5-139">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="dd4c5-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="dd4c5-140">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="dd4c5-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="dd4c5-141">สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์บน URL</span><span class="sxs-lookup"><span data-stu-id="dd4c5-141">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
