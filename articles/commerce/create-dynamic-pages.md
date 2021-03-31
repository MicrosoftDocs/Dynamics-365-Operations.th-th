---
title: สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์ URL
description: หัวข้อนี้จะอธิบายวิธีตั้งค่าหน้า e-commerce ของ Microsoft Dynamics 365 Commerce ที่สามารถให้บริการเนื้อหาแบบไดนามิก บนพื้นฐานของพารามิเตอร์ URL
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d6b4756fc81dc99786da251d5d9a575a71ccc49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208026"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="625c7-103">สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์ URL</span><span class="sxs-lookup"><span data-stu-id="625c7-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="625c7-104">หัวข้อนี้จะอธิบายวิธีตั้งค่าหน้า e-commerce ของ Microsoft Dynamics 365 Commerce ที่สามารถให้บริการเนื้อหาแบบไดนามิก บนพื้นฐานของพารามิเตอร์ URL</span><span class="sxs-lookup"><span data-stu-id="625c7-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="625c7-105">หน้า e-commerce สามารถตั้งค่าคอนฟิกให้แสดงเนื้อหาที่แตกต่างกันตามเซ็กเมนต์ในพาธ URL ได้</span><span class="sxs-lookup"><span data-stu-id="625c7-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="625c7-106">ดังนั้น จึงสามารถเรียกหน้านี้ได้อีกอย่างหนึ่งว่าหน้าแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="625c7-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="625c7-107">เซ็กเมนต์นี้จะใช้เป็นพารามิเตอร์เพื่อดึงข้อมูลเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="625c7-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="625c7-108">ตัวอย่างเช่น หน้าที่มีชื่อว่า **blog\_viewer** จะถูกสร้างและเชื่อมโยงกับ URL `https://fabrikam.com/blog`</span><span class="sxs-lookup"><span data-stu-id="625c7-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="625c7-109">จากนั้นสามารถใช้หน้านี้เพื่อแสดงเนื้อหาที่แตกต่างกันตามเซ็กเมนต์สุดท้ายในพาธ URL</span><span class="sxs-lookup"><span data-stu-id="625c7-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="625c7-110">ตัวอย่างเช่น เซ็กเมนต์สุดท้ายใน URL `https://fabrikam.com/blog/article-1` คือ **article-1**</span><span class="sxs-lookup"><span data-stu-id="625c7-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="625c7-111">คุณสามารถเชื่อมโยงหน้าที่สร้างขึ้นเองแยกต่างหากซึ่งแทนที่หน้าแบบไดนามิกเข้ากับเซ็กเมนต์ในพาธ URL ได้</span><span class="sxs-lookup"><span data-stu-id="625c7-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="625c7-112">ตัวอย่างเช่น หน้าที่มีชื่อว่า **blog\_summary** จะถูกสร้างและเชื่อมโยงกับ URL `https://fabrikam.com/blog/about-this-blog`</span><span class="sxs-lookup"><span data-stu-id="625c7-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="625c7-113">เมื่อมีการร้องขอ URL นี้ หน้า **blog\_summary** ที่เชื่อมโยงกับพารามิเตอร์ **/about-this-blog** จะถูกส่งคืนแทนหน้า **blog\_viewer**</span><span class="sxs-lookup"><span data-stu-id="625c7-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="625c7-114">ฟังก์ชันการโฮสต์ การดึงข้อมูล และการแสดงเนื้อหาของหน้าแบบไดนามิกจะใช้งานโดยใช้โมดูลที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="625c7-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="625c7-115">สำหรับข้อมูลเพิ่มเติม ดู [ความสามารถในการขยายช่องทางออนไลน์](e-commerce-extensibility/overview.md)</span><span class="sxs-lookup"><span data-stu-id="625c7-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="625c7-116">ตั้งค่าหน้า e-commerce แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="625c7-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="625c7-117">หากต้องการตั้งค่าหน้า e-commerce แบบไดนามิก คุณต้องสร้างหน้าแบบไดนามิก สร้าง URL พื้นฐาน และตั้งค่าคอนฟิกเส้นทางไปยังหน้าแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="625c7-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="625c7-118">สร้างหน้าที่จะตอบสนองเนื้อหาแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="625c7-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="625c7-119">ในการสร้างหน้าที่จะตอบสนองเนื้อหาแบบไดนามิก ให้ปฏิบัติตามขั้นตอนใน [เพิ่มหน้าไซต์ใหม่](add-new-page.md)</span><span class="sxs-lookup"><span data-stu-id="625c7-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="625c7-120">หน้าที่คุณสร้างขึ้นจะต้องมีการใช้งานโมดูลที่ใช้เซ็กเมนต์สุดท้ายในพาธ URL เพื่อดึงข้อมูลเนื้อหาจากแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="625c7-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="625c7-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการพัฒนาโมดูลแบบกำหนดเอง ดู [ความสามารถในการขยายช่องทางออนไลน์](e-commerce-extensibility/overview.md)</span><span class="sxs-lookup"><span data-stu-id="625c7-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="625c7-122">สร้าง URL พื้นฐานของหน้าแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="625c7-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="625c7-123">หากต้องการสร้าง URL พื้นฐานให้กับหน้าแบบไดนามิกของโปรแกรมสร้างไซต์ Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="625c7-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="625c7-124">ไปยัง **URL** และเลือก **ใหม่ \> URL ใหม่**</span><span class="sxs-lookup"><span data-stu-id="625c7-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="625c7-125">ในกล่องโต้ตอบ **สร้าง URL ใหม่** เลือก **หน้าภายใน**</span><span class="sxs-lookup"><span data-stu-id="625c7-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="625c7-126">ภายใต้ **พาธ URL** ให้ป้อนพาธที่จะใช้เป็นฐานของหน้าแบบไดนามิก (ในตัวอย่างนี้ **/blog**)</span><span class="sxs-lookup"><span data-stu-id="625c7-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="625c7-127">จากนั้นเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="625c7-127">Then select **Next**.</span></span>
1. <span data-ttu-id="625c7-128">ในกล่องโต้ตอบ **เลือกหน้า** เลือกหน้าที่คุณสร้างมาเพื่อใช้เป็นหน้าแบบไดนามิก จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="625c7-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="625c7-129">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="625c7-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="625c7-130">ตั้งค่าคอนฟิกเส้นทางไปยังหน้าแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="625c7-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="625c7-131">หากต้องการตั้งค่าคอนฟิกของเส้นทางไปยังหน้าแบบไดนามิกของโปรแกรมสร้างไซต์ Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="625c7-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="625c7-132">ไปที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="625c7-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="625c7-133">ภายใต้ **พาธ URL ที่มีระบุพารามิเตอร์** เลือก **เพิ่ม** แล้วใส่ข้อมูลพาธ URL ที่คุณใส่เข้าไปตอนสร้าง URL (ในตัวอย่างนี้ **/blog**)</span><span class="sxs-lookup"><span data-stu-id="625c7-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="625c7-134">เลือก **Save and publish**</span><span class="sxs-lookup"><span data-stu-id="625c7-134">Select **Save and publish**.</span></span>

<span data-ttu-id="625c7-135">หลังจากตั้งค่าคอนฟิกเส้นทางแล้ว ทุกคำร้องที่ส่งไปยังพาธ URL ที่ตั้งค่าพารามิเตอร์จะถูกส่งกลับไปที่หน้าที่เชื่อมโยงกับ URL นั้น</span><span class="sxs-lookup"><span data-stu-id="625c7-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="625c7-136">หากการร้องขอใดๆ มีเซ็กเมนต์เพิ่มเติม หน้าที่ถูกเชื่อมโยงจะถูกส่งกลับและเนื้อหาของหน้าจะถูกดึงข้อมูลโดยใช้เซ็กเมนต์เป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="625c7-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="625c7-137">ตัวอย่างเช่น `https://fabrikam.com/blog/article-1` จะกลับไปที่หน้า **blog\_summary** และหน้าเนื้อหาจะถูกดึงข้อมูลโดยใช้พารามิเตอร์ **/article-1**</span><span class="sxs-lookup"><span data-stu-id="625c7-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="625c7-138">แทนที่ URL ที่ตั้งค่าพารามิเตอร์ด้วยหน้าที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="625c7-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="625c7-139">การแทนที่ URL ที่ตั้งค่าพารามิเตอร์ด้วยหน้าแบบกำหนดเองของโปรแกรมสร้างไซต์ Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="625c7-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="625c7-140">ไปยัง **URL** และเลือก **ใหม่ \> URL ใหม่**</span><span class="sxs-lookup"><span data-stu-id="625c7-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="625c7-141">ในกล่องโต้ตอบ **สร้าง URL ใหม่** เลือก **หน้าภายใน**</span><span class="sxs-lookup"><span data-stu-id="625c7-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="625c7-142">ภายใต้ **พาธ URL** ใส่ข้อมูลพาธที่มีเซ็กเมนต์ที่จะแทนที่ (ในตัวอย่างนี้ **/blog/about-this-blog**)</span><span class="sxs-lookup"><span data-stu-id="625c7-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="625c7-143">จากนั้นเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="625c7-143">Then select **Next**.</span></span>
1. <span data-ttu-id="625c7-144">ในกล่องโต้ตอบ **เลือกหน้า** เลือกหน้าที่กำหนดเอง แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="625c7-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="625c7-145">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="625c7-145">Select **Publish**.</span></span>
1. <span data-ttu-id="625c7-146">หากหน้าแบบกำหนดเองยังไม่ได้รับการเผยแพร่ ไปที่หน้า **หน้า** แล้วเลือกหน้าที่กำหนดเอง จากนั้นเลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="625c7-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="625c7-147">หลังจากที่เผยแพร่หน้าที่กำหนดเองแล้ว หน้านั้นจะทำหน้าที่แทนหน้าแบบไดนามิกที่มีเนื้อหาเป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="625c7-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="625c7-148">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="625c7-148">Additional resources</span></span>

[<span data-ttu-id="625c7-149">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="625c7-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="625c7-150">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="625c7-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="625c7-151">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="625c7-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="625c7-152">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="625c7-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="625c7-153">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="625c7-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="625c7-154">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="625c7-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="625c7-155">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="625c7-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="625c7-156">ตรวจสอบการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="625c7-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="625c7-157">ความสามารถในการเพิ่มฟังก์ชันช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="625c7-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]