---
title: เพิ่มหน้านโยบายความเป็นส่วนตัว
description: หัวข้อนี้อธิบายวิธีการเพิ่มหน้านโยบายความเป็นส่วนตัวลงในไซต์ของคุณใน Microsoft Dynamics 365 Commerce
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797538"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="f1a33-103">เพิ่มหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f1a33-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1a33-104">หัวข้อนี้อธิบายวิธีการเพิ่มหน้านโยบายความเป็นส่วนตัวลงในไซต์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f1a33-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f1a33-105">การปฏิบัติตามข้อกำหนดด้านความเป็นส่วนตัวรวมถึงมาตรการขององค์กรที่แจ้งให้ผู้ใช้ไซต์ทราบถึงวิธีการรวบรวมและจัดการข้อมูลของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="f1a33-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="f1a33-106">ผู้ใช้สามารถตัดสินใจได้ว่าต้องการจัดการข้อมูลส่วนบุคคลของตนอย่างไรและสามารถดำเนินการที่เหมาะสมได้</span><span class="sxs-lookup"><span data-stu-id="f1a33-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="f1a33-107">ตรวจทานคำชี้แจงความเป็นส่วนตัวของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f1a33-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="f1a33-108">เมื่อต้องการตรวจสอบคำชี้แจงความเป็นส่วนตัวของขณะที่คุณเข้าสู่เครื่องมือการสร้างและแก้ไข Microsoft Dynamics 365 Commerce เลือกปุ่ม **ช่วยเหลือ** (**?**) ที่มุมขวาบน และเลือก **ความเป็นส่วนตัวและคุกกี้**</span><span class="sxs-lookup"><span data-stu-id="f1a33-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="f1a33-109">แท็บใหม่ที่ถูกเปิดที่มีการเชื่อมโยงไปยัง [คำชี้แจงความเป็นส่วนตัว Microsoft](https://privacy.microsoft.com/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="f1a33-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="f1a33-110">สร้างหน้านโยบายความเป็นส่วนตัวสำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f1a33-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="f1a33-111">ใน Dynamics 365 Commerce มีหลายวิธีที่จะให้ผู้ใช้เว็บไซต์ของคุณเข้าถึงนโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f1a33-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="f1a33-112">ส่วนนี้แสดงวิธีการสร้างหน้านโยบายความเป็นส่วนตัวและจากนั้นอ้างอิงหน้าโดยใช้แฟรกเมนต์ส่วนท้ายหน้า</span><span class="sxs-lookup"><span data-stu-id="f1a33-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="f1a33-113">คำแนะนำที่ต่อไปนี้เป็นตัวอย่างที่แสดงให้เห็นถึงวิธีการสร้างหน้านโยบายความเป็นส่วนตัวทั่วไปสำหรับไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="f1a33-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="f1a33-114">คุณต้องรับผิดชอบในการออกแบบและใช้โซลูชันหน้านโยบายความเป็นส่วนตัวที่ตรงกับข้อกำหนดทางกฎหมายของบริษัทของคุณมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="f1a33-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="f1a33-115">ในการเริ่มต้น ในเครื่องมือการสร้างและแก้ไข ให้ไปที่ไซต์ที่คุณต้องการสร้างหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f1a33-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="f1a33-116">สร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f1a33-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="f1a33-117">ถ้าเท็มเพลตที่สามารถใช้สำหรับหน้านโยบายความเป็นส่วนตัวได้ถูกสร้างขึ้นแล้วให้ข้ามไปยังส่วนของ [หน้านโยบายการสร้างความเป็นส่วนตัว](#build-a-privacy-policy-page)</span><span class="sxs-lookup"><span data-stu-id="f1a33-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="f1a33-118">เมื่อต้องการสร้างเท็มเพลต ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f1a33-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="f1a33-119">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตของหน้า</span><span class="sxs-lookup"><span data-stu-id="f1a33-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="f1a33-120">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตแบนเนอร์โปรโมชั่น** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f1a33-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f1a33-121">ในเทมเพลต ให้เพิ่มโมดูลที่จำเป็นลงในช่องใส่หน้าเว็บที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f1a33-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="f1a33-122">สำหรับคำแนะนำ ให้วางเมาส์เหนือเครื่องหมายอัศเจรีย์สีแดง</span><span class="sxs-lookup"><span data-stu-id="f1a33-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="f1a33-123">(ตัวอย่างเช่น ช่อง **ส่วนหัวของ HTML** อาจต้องการโมดูล **สคริปต์ภายนอกเริ่มต้น**)</span><span class="sxs-lookup"><span data-stu-id="f1a33-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="f1a33-124">ในช่อง **Body** ให้เพิ่มโมดูล **หน้าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f1a33-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="f1a33-125">ในช่อง **หน้าเริ่มต้น** ในช่อง **หลัก** ให้เพิ่มโมดูล **บล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="f1a33-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="f1a33-126">ในโมดูล **บล็อกเนื้อหา** ให้เพิ่มโมดูล **รายการบล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="f1a33-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="f1a33-127">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f1a33-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="f1a33-128">สร้างหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f1a33-128">Build a privacy policy page</span></span>

<span data-ttu-id="f1a33-129">หากต้องการสร้างหน้านโยบายความเป็นส่วนตัว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f1a33-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="f1a33-130">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้า</span><span class="sxs-lookup"><span data-stu-id="f1a33-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="f1a33-131">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือกเท็มเพลตสำหรับหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f1a33-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="f1a33-132">ป้อนชื่อหน้าและ URL ของหน้า และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f1a33-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="f1a33-133">ในช่อง **หลัก** ของหน้า ให้เพิ่มโมดูล **บล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="f1a33-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="f1a33-134">ในโมดูล **บล็อกเนื้อหา** ให้เพิ่มโมดูล **รายการบล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="f1a33-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="f1a33-135">ในบานหน้าต่างคุณสมบัติสำหรับโมดูล **บล็อกเนื้อหา** ให้เลือก **เพิ่มแหล่งข้อมูล** จากนั้นเลือก **Rich Text Content**</span><span class="sxs-lookup"><span data-stu-id="f1a33-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="f1a33-136">ในตัวแก้ไข Rich Text ให้ป้อนเนื้อหาสำหรับหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f1a33-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="f1a33-137">ขยายตัวแก้ไข Rich Text ไปยังโหมดเต็มหน้าจอตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f1a33-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="f1a33-138">เมื่อคุณป้อนเนื้อหาเสร็จแล้วให้เลือก **แสดงตัวอย่าง** เพื่อดูตัวอย่างหน้าในเว็บเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="f1a33-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="f1a33-139">ทำการเพิ่มเติมที่เหลือให้กับคุณสมบัติหน้าและโมดูลให้เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="f1a33-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="f1a33-140">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f1a33-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f1a33-141">เมื่อต้องการเผยแพร่ URL สำหรับหน้านโยบายความเป็นส่วนตัว ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f1a33-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="f1a33-142">ไปที่ **URLs** และเลือก URL สำหรับหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f1a33-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="f1a33-143">เลือก **เผยแพร่** เพื่อเผยแพร่ URL ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f1a33-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="f1a33-144">สร้างลิงก์ไปยังหน้านโยบายความเป็นส่วนตัวในส่วนท้ายหน้า</span><span class="sxs-lookup"><span data-stu-id="f1a33-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="f1a33-145">คุณสามารถเพิ่มการเชื่อมโยงไปยังหน้านโยบายความเป็นส่วนตัวไปยังส่วน</span><span class="sxs-lookup"><span data-stu-id="f1a33-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="f1a33-146">ด้วยวิธีนี้คุณสามารถแชร์ลิงก์และอัปเดตในหน้าเว็บไซต์ต่างๆ โดยอ้างอิงส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="f1a33-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="f1a33-147">ตัวอย่างนี้แสดงวิธีการเพิ่มการเชื่อมโยงไปยังหน้าของนโยบายความเป็นส่วนตัวไปยังส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="f1a33-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="f1a33-148">เมื่อต้องการเพิ่มลิงก์ไปยังส่วนท้ายหน้า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f1a33-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="f1a33-149">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนของเพจใหม่</span><span class="sxs-lookup"><span data-stu-id="f1a33-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="f1a33-150">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **ส่วนท้าย**</span><span class="sxs-lookup"><span data-stu-id="f1a33-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="f1a33-151">ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f1a33-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f1a33-152">ในช่อง **ประเภทส่วนท้าย** ให้เพิ่มโมดูล **รายการส่วนท้าย**</span><span class="sxs-lookup"><span data-stu-id="f1a33-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="f1a33-153">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **ข้อความลิงก์**</span><span class="sxs-lookup"><span data-stu-id="f1a33-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="f1a33-154">ในกล่องโต้ตอบ **ข้อความลิงก์** ป้อนข้อความลิงก์และเป้าหมายการเชื่อมโยงของหน้านโยบายความเป็นส่วนตัว จากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f1a33-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="f1a33-155">หากต้องการรับ URL ของหน้านโยบายความเป็นส่วนตัว ไปที่ **หน้า** ไปที่หน้านโยบายความเป็นส่วนตัวและคัดลอก URL จากบานหน้าต่างคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="f1a33-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="f1a33-156">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f1a33-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f1a33-157">แสดงตัวอย่างส่วนและทดสอบลิงก์ไปยังหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f1a33-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="f1a33-158">ตอนนี้ส่วนสามารถถูกอ้างอิงในแม่แบบสำหรับหน้าไซต์อื่น</span><span class="sxs-lookup"><span data-stu-id="f1a33-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="f1a33-159">เมื่อส่วนนี้ถูกอ้างอิงในโมดูล **ท้ายหน้า** ของเท็มเพลต การอ้างอิงการเชื่อมโยงจะปรากฏบนหน้าใดก็ได้ที่สร้างขึ้นโดยใช้เท็มเพลตนั้น</span><span class="sxs-lookup"><span data-stu-id="f1a33-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1a33-160">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f1a33-160">Additional resources</span></span>

[<span data-ttu-id="f1a33-161">ภาพรวมเกี่ยวกับการปฏิบัติตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="f1a33-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="f1a33-162">คุณลักษณะและความสามารถของการช่วยการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="f1a33-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="f1a33-163">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="f1a33-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="f1a33-164">แทนที่รหัสผู้ใช้ที่เชื่อมโยงกับการเปลี่ยนแปลงเนื้อหาที่ติดตาม</span><span class="sxs-lookup"><span data-stu-id="f1a33-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
