---
title: เพิ่มหน้านโยบายความเป็นส่วนตัว
description: หัวข้อนี้อธิบายวิธีการเพิ่มหน้านโญบายความปลอดภัยไปยังไซต์ของคุณใน Microsoft Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001334"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="c0e45-103">เพิ่มหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c0e45-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c0e45-104">หัวข้อนี้อธิบายวิธีการเพิ่มหน้านโญบายความปลอดภัยไปยังไซต์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0e45-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c0e45-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="c0e45-105">Overview</span></span>

<span data-ttu-id="c0e45-106">การปฏิบัติตามข้อกำหนดด้านความเป็นส่วนตัวรวมถึงมาตรการขององค์กรที่แจ้งให้ผู้ใช้ไซต์ทราบถึงวิธีการรวบรวมและจัดการข้อมูลของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="c0e45-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="c0e45-107">ผู้ใช้สามารถตัดสินใจได้ว่าต้องการจัดการข้อมูลส่วนบุคคลของตนอย่างไรและสามารถดำเนินการที่เหมาะสมได้</span><span class="sxs-lookup"><span data-stu-id="c0e45-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="c0e45-108">ตรวจทานคำชี้แจงความเป็นส่วนตัวของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0e45-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="c0e45-109">เมื่อต้องการตรวจสอบคำชี้แจงความเป็นส่วนตัวของขณะที่คุณเข้าสู่เครื่องมือการสร้างและแก้ไข Microsoft Dynamics 365 Commerce เลือกปุ่ม **ช่วยเหลือ** (**?**) ที่มุมขวาบน และเลือก **ความเป็นส่วนตัวและคุกกี้**</span><span class="sxs-lookup"><span data-stu-id="c0e45-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="c0e45-110">แท็บใหม่ที่ถูกเปิดที่มีการเชื่อมโยงไปยัง [คำชี้แจงความเป็นส่วนตัว Microsoft](https://privacy.microsoft.com/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="c0e45-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="c0e45-111">สร้างหน้านโยบายความเป็นส่วนตัวสำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0e45-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="c0e45-112">ใน Dynamics 365 Commerce มีหลายวิธีที่จะให้ผู้ใช้เว็บไซต์ของคุณเข้าถึงนโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c0e45-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="c0e45-113">ส่วนนี้แสดงวิธีการสร้างหน้านโยบายความเป็นส่วนตัวและจากนั้นอ้างอิงหน้าโดยใช้แฟรกเมนต์ส่วนท้ายหน้า</span><span class="sxs-lookup"><span data-stu-id="c0e45-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="c0e45-114">คำแนะนำที่ต่อไปนี้เป็นตัวอย่างที่แสดงให้เห็นถึงวิธีการสร้างหน้านโยบายความเป็นส่วนตัวทั่วไปสำหรับไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="c0e45-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="c0e45-115">คุณต้องรับผิดชอบในการออกแบบและใช้โซลูชันหน้านโยบายความเป็นส่วนตัวที่ตรงกับข้อกำหนดทางกฎหมายของบริษัทของคุณมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="c0e45-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="c0e45-116">ในการเริ่มต้น ในเครื่องมือการสร้างและแก้ไข ให้ไปที่ไซต์ที่คุณต้องการสร้างหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c0e45-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="c0e45-117">สร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="c0e45-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="c0e45-118">ถ้าเท็มเพลตที่สามารถใช้สำหรับหน้านโยบายความเป็นส่วนตัวได้ถูกสร้างขึ้นแล้วให้ข้ามไปยังส่วนของ [หน้านโยบายการสร้างความเป็นส่วนตัว](#build-a-privacy-policy-page)</span><span class="sxs-lookup"><span data-stu-id="c0e45-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="c0e45-119">เมื่อต้องการสร้างเท็มเพลต ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c0e45-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="c0e45-120">ไปที่ **เท็มเพลต \> เท็มเพลตใหม่**</span><span class="sxs-lookup"><span data-stu-id="c0e45-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="c0e45-121">ป้อนชื่อเท็มเพลต และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0e45-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="c0e45-122">ในเทมเพลต ให้เพิ่มโมดูลที่จำเป็นลงในช่องใส่หน้าเว็บที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c0e45-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="c0e45-123">สำหรับคำแนะนำ ให้วางเมาส์เหนือเครื่องหมายอัศเจรีย์สีแดง</span><span class="sxs-lookup"><span data-stu-id="c0e45-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="c0e45-124">ตัวอย่างเช่น ช่อง**หัว HTML** อาจต้องการโมดูล **สคริปต์ภายนอกเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="c0e45-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="c0e45-125">ในช่อง **Body** ให้เพิ่มโมดูล **หน้าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="c0e45-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="c0e45-126">ในช่อง **หน้าเริ่มต้น** ในช่อง **หลัก** ให้เพิ่มโมดูล **บล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="c0e45-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="c0e45-127">ในโมดูล **บล็อกเนื้อหา** ให้เพิ่มโมดูล **รายการบล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="c0e45-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="c0e45-128">เช็คอินเท็มเพลต และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="c0e45-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="c0e45-129">สร้างหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c0e45-129">Build a privacy policy page</span></span>

<span data-ttu-id="c0e45-130">หากต้องการสร้างหน้านโยบายความเป็นส่วนตัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c0e45-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="c0e45-131">ไปที่ **หน้า \> หน้าใหม่**</span><span class="sxs-lookup"><span data-stu-id="c0e45-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="c0e45-132">เลือกเท็มเพลตสำหรับหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c0e45-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="c0e45-133">ป้อนชื่อหน้าและ URL และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0e45-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="c0e45-134">ในช่อง **หลัก** ของหน้า ให้เพิ่มโมดูล **บล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="c0e45-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="c0e45-135">ในโมดูล **บล็อกเนื้อหา** ให้เพิ่มโมดูล **รายการบล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="c0e45-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="c0e45-136">ในบานหน้าต่างคุณสมบัติสำหรับโมดูล **บล็อกเนื้อหา** ให้เลือก **เพิ่มแหล่งข้อมูล** จากนั้นเลือก **Rich Text Content**</span><span class="sxs-lookup"><span data-stu-id="c0e45-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="c0e45-137">ในตัวแก้ไข Rich Text ให้ป้อนเนื้อหาสำหรับหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c0e45-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="c0e45-138">ขยายตัวแก้ไข Rich Text ไปยังโหมดเต็มหน้าจอตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="c0e45-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="c0e45-139">เมื่อคุณป้อนเนื้อหาเสร็จแล้วให้เลือก **แสดงตัวอย่าง** เพื่อดูตัวอย่างหน้าในเว็บเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="c0e45-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="c0e45-140">ทำการเพิ่มเติมที่เหลือให้กับคุณสมบัติหน้าและโมดูลให้เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="c0e45-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="c0e45-141">เช็คอินเท็มเพลตหน้านโยบายความเป็นส่วนตัว และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="c0e45-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="c0e45-142">เมื่อต้องการเผยแพร่ URL สำหรับหน้านโยบายความเป็นส่วนตัว ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c0e45-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="c0e45-143">ไปที่ **URLs** และเลือก URL สำหรับหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c0e45-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="c0e45-144">เผยแพร่ URL ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c0e45-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="c0e45-145">สร้างลิงก์ไปยังหน้านโยบายความเป็นส่วนตัวในส่วนท้ายหน้า</span><span class="sxs-lookup"><span data-stu-id="c0e45-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="c0e45-146">คุณสามารถเพิ่มการเชื่อมโยงไปยังหน้านโยบายความเป็นส่วนตัวไปยังส่วน</span><span class="sxs-lookup"><span data-stu-id="c0e45-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="c0e45-147">ด้วยวิธีนี้คุณสามารถแชร์ลิงก์และอัปเดตในหน้าเว็บไซต์ต่างๆ โดยอ้างอิงส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c0e45-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="c0e45-148">ตัวอย่างนี้แสดงวิธีการเพิ่มการเชื่อมโยงไปยังหน้าของนโยบายความเป็นส่วนตัวไปยังส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="c0e45-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="c0e45-149">เมื่อต้องการเพิ่มลิงก์ไปยังส่วนท้ายหน้า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c0e45-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="c0e45-150">ไปที่ **ส่วนของหน้า \> ส่วนของหน้าใหม่**</span><span class="sxs-lookup"><span data-stu-id="c0e45-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="c0e45-151">เลือกโมดูล **ท้ายหน้า** แล้วป้อนชื่อในฟิลด์ชื่อ **ส่วนของหน้า**</span><span class="sxs-lookup"><span data-stu-id="c0e45-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="c0e45-152">ในช่อง **ประเภทส่วนท้าย** ให้เพิ่มโมดูล **รายการส่วนท้าย**</span><span class="sxs-lookup"><span data-stu-id="c0e45-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="c0e45-153">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **ข้อความลิงก์**</span><span class="sxs-lookup"><span data-stu-id="c0e45-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="c0e45-154">ในกล่องโต้ตอบ **ข้อความลิงก์** ป้อนข้อความลิงก์และเป้าหมายการเชื่อมโยงของหน้านโยบายความเป็นส่วนตัว จากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0e45-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="c0e45-155">หากต้องการรับ URL ของหน้านโยบายความเป็นส่วนตัว ไปที่ **หน้า** ไปที่หน้านโยบายความเป็นส่วนตัวและคัดลอก URL จากบานหน้าต่างคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="c0e45-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="c0e45-156">บันทึกส่วน เช็คอิน และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="c0e45-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="c0e45-157">แสดงตัวอย่างส่วนและทดสอบลิงก์ไปยังหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c0e45-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="c0e45-158">ตอนนี้ส่วนสามารถถูกอ้างอิงในแม่แบบสำหรับหน้าไซต์อื่น</span><span class="sxs-lookup"><span data-stu-id="c0e45-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="c0e45-159">เมื่อส่วนนี้ถูกอ้างอิงในโมดูล **ท้ายหน้า** ของเท็มเพลต การอ้างอิงการเชื่อมโยงจะปรากฏบนหน้าใดก็ได้ที่สร้างขึ้นโดยใช้เท็มเพลตนั้น</span><span class="sxs-lookup"><span data-stu-id="c0e45-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0e45-160">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c0e45-160">Additional resources</span></span>

[<span data-ttu-id="c0e45-161">ภาพรวมเกี่ยวกับการปฏิบัติตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="c0e45-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="c0e45-162">คุณลักษณะและความสามารถของการช่วยการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="c0e45-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="c0e45-163">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="c0e45-163">Cookie compliance</span></span>](cookie-compliance.md)
