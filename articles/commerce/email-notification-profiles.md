---
title: ตั้งค่าโปรไฟล์การแจ้งเตือนทางอีเมล
description: หัวข้อนี้อธิบายวิธีสร้างโปรไฟล์การแจ้งเตือนทางอีเมลใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113816"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="d2d85-103">ตั้งค่าโปรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d2d85-104">หัวข้อนี้อธิบายวิธีสร้างโปรไฟล์การแจ้งเตือนทางอีเมลใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d2d85-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d2d85-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="d2d85-105">Overview</span></span>

<span data-ttu-id="d2d85-106">ก่อนที่จะสร้างช่องทาง คุณจะต้องตั้งค่าโปรไฟล์เพื่อให้แน่ใจว่าสามารถส่งการแจ้งเตือนทางอีเมลสำหรับกิจกรรมต่างๆได้ เช่น การสร้างใบสั่ง สถานะการจัดส่งใบสั่ง และการชำระเงินล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="d2d85-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="d2d85-107">สำหรับข้อมูลการกำหนดค่าอีเมลเพิ่มเติม ดู [การกำหนดค่าและส่งอีเมล](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)</span><span class="sxs-lookup"><span data-stu-id="d2d85-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="d2d85-108">สร้างโปรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-108">Create an email notification profile</span></span>

<span data-ttu-id="d2d85-109">สร้างโปรไฟล์การแจ้งเตือนทางอีเมล ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="d2d85-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="d2d85-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> Retail และ commerce \> การตั้งค่าศูนย์ควบคุม \> โปรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**</span><span class="sxs-lookup"><span data-stu-id="d2d85-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="d2d85-111">บนหน้าต่างการดำเนินการ คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d2d85-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="d2d85-112">ในฟิลด์ **โปรไฟล์การแจ้งเตือนทางอีเมล** ให้ป้อนชื่อเพื่อระบุโปรไฟล์</span><span class="sxs-lookup"><span data-stu-id="d2d85-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="d2d85-113">ป้อนคำอธิบายที่เกี่ยวข้องลงในฟิลด์ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="d2d85-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="d2d85-114">สลับการตั้งค่า **เปิดใช้งาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="d2d85-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="d2d85-115">สร้างเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-115">Create an email template</span></span>

<span data-ttu-id="d2d85-116">ก่อนที่จะสามารถสร้างการแจ้งเตือนทางอีเมลได้ คุณจะต้องสร้างแม่แบบอีเมลขององค์กรที่มีข้อมูลอีเมลของผู้ส่งและแม่แบบอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="d2d85-117">ทำตามขั้นตอนเหล่านี้เพื่อสร้างแม่แบบอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="d2d85-118">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งสำนักงานใหญ่ \> พารามิเตอร์ \> แม่แบบอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="d2d85-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="d2d85-119">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d2d85-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d2d85-120">ในฟิลด์ **รหัสอีเมล** ให้ป้อนรหัสเพื่อช่วยระบุแม่แบบนี้</span><span class="sxs-lookup"><span data-stu-id="d2d85-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="d2d85-121">ในฟิลด์ **ชื่อผู้ส่ง** ให้ใส่ชื่อผู้ส่ง</span><span class="sxs-lookup"><span data-stu-id="d2d85-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="d2d85-122">ป้อนคำอธิบายที่มีความหมาย ลงใน **คำอธิบายอีเมล**</span><span class="sxs-lookup"><span data-stu-id="d2d85-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="d2d85-123">ใน **อีเมลผู้ส่ง** ป้อนที่อยู่อีเมลผู้ส่ง</span><span class="sxs-lookup"><span data-stu-id="d2d85-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="d2d85-124">ในส่วน **ทั่วไป** กรอกข้อมูลเพิ่มเติมอื่นๆตามความจำเป็น (เช่น ลำดับความสำคัญของอีเมล)</span><span class="sxs-lookup"><span data-stu-id="d2d85-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="d2d85-125">ขยายส่วน **เนื้อหาข้อความอีเมล** และเลือก **สร้าง** เพื่อสร้างเนื้อหาของแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="d2d85-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="d2d85-126">สำหรับรายการเนื้อหาแต่ละรายการ ให้เลือกภาษาและระบุบรรทัดหัวเรื่องอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="d2d85-127">หากอีเมลจะมีเนื้อความให้ ตรวจสอบให้แน่ใจว่าได้ทำเครื่องหมายในช่อง **มีเนื้อความ** แล้ว</span><span class="sxs-lookup"><span data-stu-id="d2d85-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="d2d85-128">ในบานหน้าต่างการดำเนินการ เลือก **ข้อความอีเมล** เพื่อจัดทำแม่แบบเนื้อความของอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="d2d85-129">ภาพต่อไปนี้แสดงตัวอย่างส่วนหนึ่งของการตั้งค่าแม่แบบอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-129">The following image shows some example email template settings.</span></span>

![การตั้งค่าเท็มเพลตอีเมล](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="d2d85-131">สร้างเหตุการณ์ทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-131">Create an email event</span></span>

<span data-ttu-id="d2d85-132">ทำตามขั้นตอนเหล่านี้เพื่อสร้างเหตุการณ์ทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="d2d85-133">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> Retail และ commerce \> การตั้งค่าศูนย์ควบคุม \> โปรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**</span><span class="sxs-lookup"><span data-stu-id="d2d85-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="d2d85-134">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2d85-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="d2d85-135">เลือกแม่แบบอีเมลจากรายการแบบหล่นลง **รหัสอีเมล**</span><span class="sxs-lookup"><span data-stu-id="d2d85-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="d2d85-136">เลือก **ชนิดการแจ้งเตือนอีเมล** ที่เหมาะสมจากรายการแบบหล่นลง </span><span class="sxs-lookup"><span data-stu-id="d2d85-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="d2d85-137">เลือกกล่องกาเครื่องหมาย **ใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d2d85-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="d2d85-138">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d2d85-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d2d85-139">ภาพต่อไปนี้แสดงตัวอย่างส่วนหนึ่งของการตั้งค่าการแจ้งเตือนเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="d2d85-139">The following image shows some example event notification settings.</span></span>

![การตั้งค่าการแจ้งเตือนเหตุการณ์](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="d2d85-141">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d2d85-141">Additional resources</span></span>

[<span data-ttu-id="d2d85-142">ตั้งค่าคอนฟิกและส่งอีเมล</span><span class="sxs-lookup"><span data-stu-id="d2d85-142">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d2d85-143">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="d2d85-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d2d85-144">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="d2d85-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d2d85-145">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="d2d85-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
