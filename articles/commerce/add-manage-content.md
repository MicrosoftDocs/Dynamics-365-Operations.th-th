---
title: วิธีการเพิ่มเนื้อหา
description: หัวข้อนี้แสดงภาพรวม และเลือกลิงก์สำหรับสถานที่และวิธีการเริ่มต้นการจัดการเนื้อหา โดยใช้โปรแกรมสร้างไซต์ชุดเครื่องมือการเขียนแก้ไซต์ Microsoft Dynamics 365 Commerce
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 802a41b8c55e65eee58d26137c2f160b69847010
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973991"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="618d0-103">วิธีการเพิ่มเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="618d0-103">Ways to add content</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="618d0-104">หัวข้อนี้แสดงภาพรวม และเลือกลิงก์ไปยังเอกสารที่แสดงวิธีการจัดการเนื้อหา โดยใช้โปรแกรมสร้างไซต์ชุดเครื่องมือการเขียนแก้ไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="618d0-104">This topic provides an overview and links to documentation about how to manage content using the Microsoft Dynamics 365 Commerce site builder web authoring toolset.</span></span>

## <a name="overview"></a><span data-ttu-id="618d0-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="618d0-105">Overview</span></span>

<span data-ttu-id="618d0-106">มีหลายวิธีในการเปลี่ยนรูปลักษณ์ ความรู้สึก และเนื้อหาของเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="618d0-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="618d0-107">ทั้งนี้ขึ้นอยู่กับระดับที่กำหนดของการเลือกกำหนด การเปลี่ยนแปลงเหล่านี้อาจดำเนินการได้โดยผู้ที่ไม่ใช่นักพัฒนาโดยใช้โปรแกรมสร้างไซต์ ซึ่งคือชุดเครื่องมือการเขียนแก้ไซต์ที่รวมอยู่ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="618d0-107">Depending on the required level of customization, many of these changes can be implemented by non-developers within site builder, the web authoring toolset included with Dynamics 365 Commerce.</span></span> <span data-ttu-id="618d0-108">โปรแกรมสร้างไซต์ช่วยให้คุณสามารถสร้างแม่แบบ ได้เลือกชุดรูปแบบ และเลือกและตั้งค่าคอนฟิกโมดูลโดยที่ไม่ต้องมีการเขียนโค้ดใด ๆ</span><span class="sxs-lookup"><span data-stu-id="618d0-108">Site builder enables you to build templates, select themes, and select and configure modules without writing any code.</span></span> <span data-ttu-id="618d0-109">ในทางกลับกัน ทักษะการพัฒนาต้องใช้ในการสร้างชุดรูปแบบหรือโมดูลใหม่ เนื่องจากชุดพัฒนาซอฟต์แวร์อีคอมเมิร์ซ (SDK) และ Microsoft Dynamics Lifecycle Services (LCS) ต้องใช้ลำดับงานการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="618d0-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="618d0-110">หัวข้อต่อไปนี้เป็นจุดเริ่มต้นดีในการเริ่มต้นการทำความเข้าใจวิธีการเพิ่มและจัดการเนื้อหาของไซต์</span><span class="sxs-lookup"><span data-stu-id="618d0-110">The following topics are good jumping off points to start understanding how to add and manage site content.</span></span> <span data-ttu-id="618d0-111">หัวข้อส่วนใหญ่โฟกัสที่ขอบเขตของไซต์ที่ไม่จำเป็นต้องมีนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="618d0-111">Most of the topics listed focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="618d0-112">การแก้ไขเนื้อหาพื้นฐานบางอย่าง ในขณะที่ผู้อื่นเน้นในงานของผู้ดูแลไซต์</span><span class="sxs-lookup"><span data-stu-id="618d0-112">Some address basic content editing, while others focus on site administrator tasks.</span></span> <span data-ttu-id="618d0-113">แต่ละหัวข้อเหล่านี้จะแสดงถึงงานที่เฉพาะเจาะจงอาจต้องใช้งาน SDK</span><span class="sxs-lookup"><span data-stu-id="618d0-113">Each of these topics will denote specific tasks might require SDK work.</span></span> <span data-ttu-id="618d0-114">แต่ละหัวข้อคิดว่าคุณได้เตรียมไซต์แล้ว และได้รับอนุญาตให้เข้าถึงโปรแกรมสร้างไซต์สำหรับไซต์ของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="618d0-114">Each topic assumes that you have already provisioned a site and been granted access to the site builder toolset for your site.</span></span>

<span data-ttu-id="618d0-115">เลือกหัวข้ออย่างใดอย่างหนึ่งต่อไปนี้เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="618d0-115">Select one of the following topics to get started.</span></span>

- <span data-ttu-id="618d0-116">เมื่อต้องการทำความคุ้นเคยกับคำศัพท์ของการจัดการเนื้อหาที่ใช้ในโปรแกรมสร้างไซต์ และภายในเอกสารนี้ โปรดดูที่ [อภิธานศัพท์แบบจำลองหน้า](page-elements-overview.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-116">To familiarize yourself with the content management terminology used in site builder and within this documentation, see [Page model glossary](page-elements-overview.md).</span></span>
- <span data-ttu-id="618d0-117">เมื่อต้องการเข้าใจวิธีการทำงานของโมดูลในลำดับงานการจัดการเนื้อหา ให้ดูที่ [การทำงานกับโมดูล](work-with-modules.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-117">To understand how modules work within content management workflows, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="618d0-118">เมื่อต้องการเปลี่ยนแปลงข้อความ รูปภาพ หรือวิดีโอบนหน้าไซต์ที่มีอยู่ ดูที่ [การทำงานกับโมดูล](work-with-modules.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-118">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="618d0-119">เมื่อต้องการดูว่าส่วนจะทำให้การจัดการเนื้อหามีประสิทธิภาพและยืดหยุ่นมากขึ้นได้อย่างไร ให้ดูที่ [การทำงานกับส่วน](work-with-fragments.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-119">To see how fragments can make content management more efficient and flexible, see [Work with fragments](work-with-fragments.md).</span></span>
- <span data-ttu-id="618d0-120">เพื่อช่วยให้มั่นใจว่าประสบความสำเร็จใน ประสบการณ์การสร้างรูปแบบแบรนด์สำหรับผู้เขียนเนื้อหาเว็บ โปรดดูที่ [แม่แบบและโครงร่าง](templates-layouts-overview.md) และ [การทำงานกับแม่แบบ](work-with-templates.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-120">To help ensure a successful on-brand authoring experience for web content authors, see [Templates and layouts overview](templates-layouts-overview.md) and [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="618d0-121">เมื่อต้องการจัดเรียงส่วนบนเพจของไซต์ ดูที่ [การทำงานกับโครงร่าง](work-with-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-121">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="618d0-122">เมื่อต้องการเปลี่ยนแบบอักษร สี และลักษณะทั่วไปของเพจของไซต์ ดูที่ [การเลือกชุดรูปแบบไซต์](select-site-theme.md) หรือ [ทำงานกับไฟล์แทนที่ CSS](css-override-files.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-122">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md) or [Work with CSS over-ride files](css-override-files.md).</span></span>
- <span data-ttu-id="618d0-123">เมื่อต้องการจัดเรียงใหม่หรือเพิ่มตัวเลือกการนำทางใหม่ ให้ดูที่ [การเลือกกำหนดการนำทางของไซต์](customize-site-navigation.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-123">To rearrange or add new navigation options, see [Customize site navigation](customize-site-navigation.md).</span></span>
- <span data-ttu-id="618d0-124">เมื่อต้องการเรียนรู้เกี่ยวกับการเตรียมการ การแสดงตัวอย่าง และเผยแพร่การเปลี่ยนแปลงเนื้อหาเว็บที่เกิดขึ้นพร้อมกัน ดู [การทำงานกับกลุ่มการเผยแพร่](publish-groups.md)</span><span class="sxs-lookup"><span data-stu-id="618d0-124">To learn how to stage, preview, and publish a broad set of concurrent web content changes, see [Work with publish groups](publish-groups.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="618d0-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="618d0-125">Additional resources</span></span>

[<span data-ttu-id="618d0-126">ภาพรวมของการสร้างหน้า</span><span class="sxs-lookup"><span data-stu-id="618d0-126">Authoring page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="618d0-127">อภิธานศัพท์ของรูปแบบหน้า</span><span class="sxs-lookup"><span data-stu-id="618d0-127">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="618d0-128">สถานะและระยะเวลาใช้งานของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="618d0-128">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="618d0-129">เปิดใช้งานและใช้การใช้ร่วมกันข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="618d0-129">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)
