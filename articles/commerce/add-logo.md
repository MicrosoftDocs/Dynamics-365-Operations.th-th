---
title: เพิ่มโลโก้
description: หัวข้อนี้อธิบายวิธีการเพิ่มโลโก้ไปยังไซต์ของคุณใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
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
ms.openlocfilehash: 62b8237fa0c30fa9d901d670de38416cf8615c8d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686657"
---
# <a name="add-a-logo"></a><span data-ttu-id="a4445-103">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="a4445-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4445-104">หัวข้อนี้อธิบายวิธีการเพิ่มโลโก้ไปยังไซต์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a4445-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a4445-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="a4445-105">Overview</span></span>

<span data-ttu-id="a4445-106">เมื่อคุณสร้างเว็บไซต์หนึ่ง สิ่งแรกที่คุณอาจจะทำคือการเพิ่มบริษัทหรือโลโก้แบรนด์ของคุณลงในส่วนหัวของเว็บไซต์</span><span class="sxs-lookup"><span data-stu-id="a4445-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="a4445-107">ชุดโปรแกรมเริ่มต้นออนไลน์ Dynamics 365 Commerce มีโมดูลที่ทำให้งานนี้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4445-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="a4445-108">คุณสามารถเพิ่มโลโก้ลงในเท็มเพลต เค้าโครง หรือหน้าได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="a4445-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="a4445-109">ด้วยวิธีนี้คุณสามารถเปลี่ยนโลโก้ที่ปรากฏบนหน้าเว็บหรือกลุ่มของหน้าเว็บที่เฉพาะเจาะจงได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="a4445-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="a4445-110">อย่างไรก็ตามหัวข้อนี้ครอบคลุมสถานการณ์ที่พบบ่อยที่สุดที่คุณเพิ่มโลโก้ของคุณไปยังส่วนหัวที่สามารถนำมาใช้ในทุกหน้าของเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4445-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a4445-111">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a4445-111">Prerequisites</span></span>

<span data-ttu-id="a4445-112">ก่อนที่คุณจะสามารถเพิ่มโลโก้ลงในหน้าเว็บทั้งหมดของไซต์ คุณจะต้องทำงานเหล่านี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a4445-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="a4445-113">อัพโหลดโลโก้ของคุณไปยังไลบรารีสื่อ</span><span class="sxs-lookup"><span data-stu-id="a4445-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="a4445-114">สร้างส่วนหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="a4445-114">Create a header fragment.</span></span> <span data-ttu-id="a4445-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างกลุ่มดังกล่าวและใช้หัวข้อ โปรดดู [ทำงานกับส่วน](work-with-fragments.md)</span><span class="sxs-lookup"><span data-stu-id="a4445-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="a4445-116">รวมส่วนหัวในเท็มเพลตที่หน้าของไซต์ของคุณใช้สำหรับเค้าโครงและตัวเลือกโมดูล</span><span class="sxs-lookup"><span data-stu-id="a4445-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="a4445-117">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับเท็มเพลต โปรดดูที่ [ทำงานกับเท็มเพลต](work-with-templates.md)</span><span class="sxs-lookup"><span data-stu-id="a4445-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="a4445-118">เพิ่มโลโก้ให้กับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="a4445-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="a4445-119">หากต้องการเพิ่มโลโก้ให้กับส่วนหัวของเว็บไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a4445-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="a4445-120">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วนต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="a4445-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="a4445-121">เลือกส่วนของส่วนหัวที่คุณสร้างไว้ก่อนหน้านี้ แล้วเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a4445-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="a4445-122">ขยายโมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="a4445-122">Expand the header module.</span></span>
1. <span data-ttu-id="a4445-123">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลส่วนหัว ให้ระบุรูปภาพและลิงก์สำหรับโลโก้</span><span class="sxs-lookup"><span data-stu-id="a4445-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="a4445-124">บันทึกส่วนของส่วนหัว แก้ไขให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="a4445-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="a4445-125">หลังจากที่คุณเผยแพร่ส่วนหัวที่อัปเดต หน้าไซต์ทั้งหมดที่ใช้เท็มเพลตที่ประกอบด้วยส่วนหัวจะแสดงโลโก้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4445-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4445-126">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a4445-126">Additional resources</span></span>

[<span data-ttu-id="a4445-127">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="a4445-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="a4445-128">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="a4445-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="a4445-129">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="a4445-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="a4445-130">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="a4445-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="a4445-131">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a4445-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="a4445-132">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4445-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="a4445-133">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="a4445-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

