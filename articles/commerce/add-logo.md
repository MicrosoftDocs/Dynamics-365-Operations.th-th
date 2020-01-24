---
title: เพิ่มโลโก้
description: หัวข้อนี้อธิบายวิธีการเพิ่มโลโก้ไปยังไซต์ของคุณใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914637"
---
# <a name="add-a-logo"></a><span data-ttu-id="83f49-103">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="83f49-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="83f49-104">หัวข้อนี้อธิบายวิธีการเพิ่มโลโก้ไปยังไซต์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="83f49-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="83f49-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="83f49-105">Overview</span></span>

<span data-ttu-id="83f49-106">เมื่อคุณสร้างเว็บไซต์หนึ่ง สิ่งแรกที่คุณอาจจะทำคือการเพิ่มบริษัทหรือโลโก้แบรนด์ของคุณลงในส่วนหัวของเว็บไซต์</span><span class="sxs-lookup"><span data-stu-id="83f49-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="83f49-107">ชุดโปรแกรมเริ่มต้นออนไลน์ Dynamics 365 Commerce มีโมดูลที่ทำให้งานนี้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="83f49-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="83f49-108">คุณสามารถเพิ่มโลโก้ลงในเท็มเพลต เค้าโครง หรือหน้าได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="83f49-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="83f49-109">ด้วยวิธีนี้คุณสามารถเปลี่ยนโลโก้ที่ปรากฏบนหน้าเว็บหรือกลุ่มของหน้าเว็บที่เฉพาะเจาะจงได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="83f49-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="83f49-110">อย่างไรก็ตามหัวข้อนี้ครอบคลุมสถานการณ์ที่พบบ่อยที่สุดที่คุณเพิ่มโลโก้ของคุณไปยังส่วนหัวที่สามารถนำมาใช้ในทุกหน้าของเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="83f49-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="83f49-111">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="83f49-111">Prerequisites</span></span>

<span data-ttu-id="83f49-112">ก่อนที่คุณจะสามารถเพิ่มโลโก้ลงในหน้าเว็บทั้งหมดของไซต์ คุณจะต้องทำงานเหล่านี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="83f49-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="83f49-113">อัปโหลดโลโก้ของคุณไปยังตัวจัดการสินทรัพย์ดิจิทัล ซึ่งคุณสามารถเข้าถึงได้จากหน้า **สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="83f49-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="83f49-114">สร้างส่วนหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="83f49-114">Create a header fragment.</span></span> <span data-ttu-id="83f49-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างกลุ่มดังกล่าวและใช้หัวข้อ โปรดดู [ทำงานกับส่วน](work-with-fragments.md)</span><span class="sxs-lookup"><span data-stu-id="83f49-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="83f49-116">รวมส่วนหัวในเท็มเพลตที่หน้าของไซต์ของคุณใช้สำหรับเค้าโครงและตัวเลือกโมดูล</span><span class="sxs-lookup"><span data-stu-id="83f49-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="83f49-117">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับเท็มเพลต โปรดดูที่ [ทำงานกับเท็มเพลต](work-with-templates.md)</span><span class="sxs-lookup"><span data-stu-id="83f49-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="83f49-118">เพิ่มโลโก้ให้กับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="83f49-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="83f49-119">หากต้องการเพิ่มโลโก้ให้กับส่วนหัวของเว็บไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="83f49-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="83f49-120">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วน** แล้วเลือกส่วนหัวที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="83f49-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="83f49-121">เลือก **เช็คเอาท์**</span><span class="sxs-lookup"><span data-stu-id="83f49-121">Select **Check out**.</span></span>
3. <span data-ttu-id="83f49-122">ขยายช่อง **ส่วนหัว** และช่อง **โลโก้**</span><span class="sxs-lookup"><span data-stu-id="83f49-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="83f49-123">เลือกปุ่มจุดไข่ปลา (**...**) สำหรับช่อง **โลโก้** แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="83f49-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="83f49-124">เลือกโมดูลโลโก้</span><span class="sxs-lookup"><span data-stu-id="83f49-124">Select the logo module.</span></span>
6. <span data-ttu-id="83f49-125">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ตั้งค่าโมดูลโลโก้กลับไปที่ด้านบนเพื่อแสดงโลโก้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="83f49-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="83f49-126">บันทึกส่วนที่เป็นส่วนหัว เช็คอิน และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="83f49-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="83f49-127">หลังจากที่คุณเผยแพร่ส่วนหัวที่อัปเดต หน้าไซต์ทั้งหมดที่ใช้เท็มเพลตที่ประกอบด้วยส่วนหัวจะแสดงโลโก้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="83f49-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83f49-128">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="83f49-128">Additional resources</span></span>

[<span data-ttu-id="83f49-129">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="83f49-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="83f49-130">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="83f49-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="83f49-131">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="83f49-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="83f49-132">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="83f49-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="83f49-133">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="83f49-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="83f49-134">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="83f49-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="83f49-135">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="83f49-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

