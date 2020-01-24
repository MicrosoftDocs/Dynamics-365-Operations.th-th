---
title: ทำงานกับไฟล์การแทนที่ CSS
description: หัวข้อนี้อธิบายว่าทำไม เมื่อใด และวิธีการใช้ไฟล์การแทนที่ Cascading Style Sheet (CSS) ใน Microsoft Dynamics 365 Commerce
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b5a50fc0c9060117cdddc0875446afc2edc12a11
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915450"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="002ed-103">ทำงานกับไฟล์การแทนที่ CSS</span><span class="sxs-lookup"><span data-stu-id="002ed-103">Work with CSS override files</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="002ed-104">หัวข้อนี้อธิบายว่าทำไม เมื่อใด และวิธีการใช้ไฟล์การแทนที่ Cascading Style Sheet (CSS) ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="002ed-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="002ed-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="002ed-105">Overview</span></span>

<span data-ttu-id="002ed-106">รูปแบบเว็บไซต์ถาวรควรจะจัดการผ่านชุดรูปแบบของเว็บไซต์.</span><span class="sxs-lookup"><span data-stu-id="002ed-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="002ed-107">ชุดรูปแบบจะให้การตั้งค่าและลักษณะ CSS ที่เป็นพื้นฐานสำหรับโมดูลที่อยู่บนหน้าเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="002ed-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="002ed-108">ชุดรูปแบบถูกสร้างขึ้นโดยใช้ชุดพัฒนาซอฟต์แวร์ออนไลน์ (SDK) Dynamics 365 Commerce และจะถูกปรับใช้กับเว็บไซต์ของคุณผ่าน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="002ed-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="002ed-109">ความสามารถในการดีบักของชุดรูปแบบและการกำหนดค่าส่วนติดต่อโมดูลใน SDK ช่วยให้นักพัฒนาเว็บไซต์สร้างแพคเกจการออกแบบที่ปรับแต่งเองได้และสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="002ed-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="002ed-110">เมื่อมีการปรับใช้แพ็กเกจการออกแบบเหล่านี้ไปยังไซต์ ผู้เขียนไซต์สามารถมุ่งเน้นไปที่การสร้าง การแก้ไข และการเผยแพร่เนื้อหาแทนการพัฒนาไซต์</span><span class="sxs-lookup"><span data-stu-id="002ed-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="002ed-111">กำหนดวงจรชีวิตปกติของชุดรูปแบบ การพึ่งพานักพัฒนาเพื่อทำการเปลี่ยนแปลงลักษณะผ่าน SDK และการปรับใช้ของไปป์ไลน์ LCS สามารถจำกัดได้ในบางสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="002ed-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="002ed-112">ต้นแบบของไซต์หรือโปรแกรมแก้ไขด่วนสามารถดูยุ่งยาก ถ้า SDK ไม่ได้รับการกำหนดค่า หรือถ้าคุณไม่มีเวลาที่จะรอการปรับใช้ LCS</span><span class="sxs-lookup"><span data-stu-id="002ed-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="002ed-113">ในสถานการณ์เหล่านี้ การแทนที่ CSS สามารถช่วยได้</span><span class="sxs-lookup"><span data-stu-id="002ed-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="002ed-114">ในเครื่องมือการเขียน Commerce ผู้ใช้ที่รับรองความถูกต้องสามารถอัปโหลดไฟล์ CSS ดูตัวอย่าง แล้วเปิดใช้งานเพื่อแทนที่ชุดรูปแบบของไซต์</span><span class="sxs-lookup"><span data-stu-id="002ed-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="002ed-115">ค่าโสหุ้ยของการปรับใช้ SDK หรือ LCS ไม่จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="002ed-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="002ed-116">การแทนที่ที่ระบุไว้ในไฟล์การแทนที่ CSS อาจมีขนาดเล็กเท่าการเปลี่ยนแปลงรูปแบบข้อความเดียวหรือที่หลากหลายเป็นยกเลิกแบรนด์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="002ed-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="002ed-117">ก่อนที่คุณจะใช้การแทนที่ไฟล์ CSS โปรดทราบข้อจำกัดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="002ed-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="002ed-118">ไฟล์แทนที่ CSS หนึ่งไฟล์เท่านั้นที่สามารถใช้งานได้บนไซต์ในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="002ed-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="002ed-119">ดังนั้น การแทนที่ที่ใช้งานอยู่ทั้งหมดต้องอยู่ในไฟล์แทนที่เดียว</span><span class="sxs-lookup"><span data-stu-id="002ed-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="002ed-120">ถึงแม้ว่าคุณสามารถแสดงตัวอย่างการแทนที่ในเครื่องมือการเขียน Commerce ไม่มีคุณลักษณะการดีบักโดยเฉพาะเพื่อช่วยระบุข้อบกพร่องใดๆ ที่การแทนที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="002ed-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="002ed-121">อีกนัยหนึ่ง เมื่อคุณใช้ไฟล์การแทนที่ CSS คุณไม่มีเครื่องมือชุดเดียวกันที่ SDK ให้สำหรับโมดูลและการตรวจสอบการเขียนแก้</span><span class="sxs-lookup"><span data-stu-id="002ed-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="002ed-122">อย่างไรก็ตาม ไฟล์แทนที่ CSS ให้วิธีที่รวดเร็วในการสร้างต้นแบบการออกแบบหรือใช้โปรแกรมแก้ไขด่วนก่อนที่จะมีการพัฒนารูปแบบเต็มรูปแบบและปรับใช้</span><span class="sxs-lookup"><span data-stu-id="002ed-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="002ed-123">สร้างไฟล์การแทนที่ CSS</span><span class="sxs-lookup"><span data-stu-id="002ed-123">Create a CSS override file</span></span>

<span data-ttu-id="002ed-124">เมื่อต้องการสร้างไฟล์แทนที่ CSS คุณสามารถใช้สภาพแวดล้อมการพัฒนาแบบรวม (IDE) โปรแกรมแก้ไขข้อความ หรือตัวแก้ไขรหัสต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="002ed-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="002ed-125">วิธีการทั่วไปคือการใช้ดีบักเกอร์เว็บไซต์มาตรฐานในเบราว์เซอร์ของคุณเพื่อระบุตัวเลือกลักษณะ คุณสมบัติ และค่าบนไซต์ที่มีอยู่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="002ed-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="002ed-126">เบราว์เซอร์ส่วนใหญ่ช่วยให้คุณสามารถเปลี่ยนค่าและแสดงตัวอย่างในดีบักเกอร์ได้</span><span class="sxs-lookup"><span data-stu-id="002ed-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="002ed-127">หลังจากที่คุณได้ระบุการเปลี่ยนแปลงที่คุณต้องการทำแล้ว คุณสามารถบันทึกไปยังไฟล์ CSS ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="002ed-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="002ed-128">อัปโหลดไฟล์แทนที่ CSS</span><span class="sxs-lookup"><span data-stu-id="002ed-128">Upload a CSS override file</span></span>

<span data-ttu-id="002ed-129">หากต้องการอัปโหลดไฟล์ CSS ไปยังไซต์ของคุณใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="002ed-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="002ed-130">ในเครื่องมือการสร้าง ให้ไปที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="002ed-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="002ed-131">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="002ed-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="002ed-132">ขึ้นอยู่กับเวอร์ชันของเครื่องการแก้ไข Commerce ที่คุณใช้ คุณอาจต้องขยาย **การตั้งค่า** ในบานหน้าต่างนำทางก่อนจึงจะสามารถเลือก **การออกแบบ** ได้</span><span class="sxs-lookup"><span data-stu-id="002ed-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="002ed-133">ที่ด้านบนของบานหน้าต่างการออกแบบหลัก ให้เลือกแท็บ **การแทนที่ CSS** ถ้ายังไม่ได้เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="002ed-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="002ed-134">ภายใต้ **การแทนที่ CSS ที่ใช้ได้** เลือก **อัปโหลดไฟล์ CSS**</span><span class="sxs-lookup"><span data-stu-id="002ed-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="002ed-135">หน้าต่างตัวสำรวจไฟล์จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="002ed-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="002ed-136">ใน File Explorer เรียกดูและเลือกไฟล์ CSS แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="002ed-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="002ed-137">ไฟล์ CSS ที่อัปโหลดจะปรากฏภายใต้ **การแทนที่ CSS ที่พร้อมใช้**</span><span class="sxs-lookup"><span data-stu-id="002ed-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="002ed-138">แสดงตัวอย่างไฟล์แทนที่ CSS</span><span class="sxs-lookup"><span data-stu-id="002ed-138">Preview a CSS override file</span></span>

<span data-ttu-id="002ed-139">เมื่อต้องการแสดงตัวอย่างไฟล์แทนที่ CSS ก่อนที่คุณจะทำให้เปิดใช้งานบนเว็บไซต์ของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="002ed-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="002ed-140">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ออกแบบ** จากนั้นบนแท็บ **การแทนที่ CSS** ภายใต้ **การแทนที่ CSS ที่พร้อมใช้งาน** ค้นหาไฟล์ CSS ที่คุณต้องการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="002ed-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="002ed-141">ถัดจากชื่อไฟล์ CSS เลือก **ไซต์แสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="002ed-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="002ed-142">ในกล่องโต้ตอบ **เลือก URL** เลือก URL ของไซต์ที่คุณต้องการดูการแทนที่ที่นำไปใช้ จากนั้นให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="002ed-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="002ed-143">ถ้ามีหลายตัวแปรสำหรับ URL ที่เลือก ให้เลือกตัวแปรที่ต้องการในกล่องโต้ตอบ **ดูตัวอย่างตัวแปร** ที่ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="002ed-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="002ed-144">แท็บหรือหน้าต่างใหม่ของเบราว์เซอร์ใหม่จะเปิดขึ้น ซึ่งคุณสามารถตรวจสอบการแทนที่ลักษณะของคุณกับไซต์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="002ed-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="002ed-145">จากนั้นคุณสามารถแชร์ URL กับผู้ใช้ Commerce ที่รับรองความถูกต้องอื่นๆ สำหรับการตรวจทานและข้อเสนอแนะ</span><span class="sxs-lookup"><span data-stu-id="002ed-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="002ed-146">เปิดใช้ไฟล์แทนที่ CSS บนไซต์ที่ถ่ายทอดสดของคุณ</span><span class="sxs-lookup"><span data-stu-id="002ed-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="002ed-147">หลังจากที่คุณได้แสดงตัวอย่างและอนุมัติไฟล์แทนที่ CSS แล้ว คุณจะสามารถเปิดใช้งานได้บนเว็บไซต์ที่ถ่ายทอดสดของคุณ</span><span class="sxs-lookup"><span data-stu-id="002ed-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="002ed-148">ไฟล์แทนที่ CSS หนึ่งไฟล์เท่านั้นที่สามารถใช้งานได้บนไซต์ของคุณในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="002ed-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="002ed-149">ถ้าคุณเปิดใช้งานไฟล์แทนที่ใหม่ ไฟล์แทนที่ก่อนหน้าจะถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="002ed-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="002ed-150">ดังนั้นโปรดตรวจสอบให้แน่ใจว่าการแทนที่ CSS ที่จำเป็นทั้งหมดมีอยู่ในไฟล์แทนที่เดียว</span><span class="sxs-lookup"><span data-stu-id="002ed-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="002ed-151">เมื่อต้องการเปิดใช้ไฟล์แทนที่ CSS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="002ed-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="002ed-152">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ออกแบบ** จากนั้นบนแท็บ **การแทนที่ CSS** ภายใต้ **การแทนที่ CSS ที่พร้อมใช้งาน** ค้นหาไฟล์ CSS ที่คุณต้องการเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="002ed-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="002ed-153">ภายใต้ชื่อไฟล์ CSS ให้เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="002ed-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="002ed-154">ไฟล์แทนที่จะเปิดใช้งานในเว็บไซต์ที่ถ่ายทอดสดของคุณทันที</span><span class="sxs-lookup"><span data-stu-id="002ed-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="002ed-155">ปิดใช้ไฟล์แทนที่ CSS บนไซต์ที่ถ่ายทอดสดของคุณ</span><span class="sxs-lookup"><span data-stu-id="002ed-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="002ed-156">เมื่อต้องการปิดใช้งานไฟล์แทนที่ CSS บนไซต์ของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="002ed-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="002ed-157">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ออกแบบ** จากนั้นบนแท็บ **การแทนที่ CSS** ภายใต้ **การแทนที่ CSS ที่พร้อมใช้งาน** ค้นหาไฟล์ CSS ที่คุณต้องการปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="002ed-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="002ed-158">ภายใต้ชื่อไฟล์ CSS ให้เลือก **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="002ed-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="002ed-159">ไฟล์แทนที่จะปิดใช้งานในเว็บไซต์ที่ถ่ายทอดสดของคุณทันที</span><span class="sxs-lookup"><span data-stu-id="002ed-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="002ed-160">หากต้องการเข้าถึงตัวเลือกเพิ่มเติมสำหรับการแทนที่ไฟล์ CSS ให้เลือกจุดไข่ปลา (**...**) ที่อยู่ติดกับชื่อไฟล์ CSS</span><span class="sxs-lookup"><span data-stu-id="002ed-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="002ed-161">ตัวเลือก **ดาวน์โหลด** **เปลี่ยนชื่อ** และ **แทนที่** มีประโยชน์สำหรับการเปลี่ยนแปลงอย่างรวดเร็วไปยังไฟล์การแทนที่ CSS ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="002ed-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="002ed-162">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="002ed-162">Additional resources</span></span>

[<span data-ttu-id="002ed-163">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="002ed-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="002ed-164">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="002ed-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="002ed-165">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="002ed-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="002ed-166">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="002ed-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="002ed-167">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="002ed-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="002ed-168">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="002ed-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="002ed-169">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="002ed-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
