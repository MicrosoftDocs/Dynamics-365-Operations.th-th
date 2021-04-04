---
title: ตั้งค่าโปรไฟล์การแจ้งเตือนทางอีเมล
description: หัวข้อนี้อธิบายวิธีสร้างโปรไฟล์การแจ้งเตือนทางอีเมลใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555318"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="815f1-103">ตั้งค่าโพรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="815f1-104">หัวข้อนี้อธิบายวิธีสร้างโปรไฟล์การแจ้งเตือนทางอีเมลใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="815f1-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="815f1-105">เมื่อคุณสร้างช่องทางการขาย คุณจะสามารถตั้งค่าโปรไฟล์การแจ้งเตือนอีเมลได้ </span><span class="sxs-lookup"><span data-stu-id="815f1-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="815f1-106">ด้วยวิธีนี้ อีเมลจะถูกส่งไปยังลูกค้าสำหรับเหตุการณ์ทางธุรกรรมต่างๆ เช่น การสร้างใบสั่ง สถานะการจัดส่งคำสั่งซื้อ และการำชำระเงินล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="815f1-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="815f1-107">สำหรับข้อมูลการกำหนดค่าอีเมลเพิ่มเติม ดู [การกำหนดค่าและส่งอีเมล](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)</span><span class="sxs-lookup"><span data-stu-id="815f1-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="815f1-108">สร้างโปรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-108">Create an email notification profile</span></span>

<span data-ttu-id="815f1-109">สร้างโปรไฟล์การแจ้งเตือนทางอีเมล ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="815f1-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="815f1-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> Retail และ commerce \> การตั้งค่าศูนย์ควบคุม \> โปรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**</span><span class="sxs-lookup"><span data-stu-id="815f1-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="815f1-111">บนหน้าต่างการดำเนินการ คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="815f1-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="815f1-112">ในฟิลด์ **โปรไฟล์การแจ้งเตือนทางอีเมล** ให้ป้อนชื่อเพื่อระบุโปรไฟล์</span><span class="sxs-lookup"><span data-stu-id="815f1-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="815f1-113">ป้อนคำอธิบายที่เกี่ยวข้องลงในฟิลด์ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="815f1-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="815f1-114">สลับการตั้งค่า **เปิดใช้งาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="815f1-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="815f1-115">สร้างเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-115">Create an email template</span></span>

<span data-ttu-id="815f1-116">ก่อนเปิดใช้งานชนิดการแจ้งเตือนทางอีเมล คุณต้องสร้างเท็มเพลตอีเมลขององค์กรในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="815f1-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="815f1-117">เท็มเพลตนี้จะระบุชื่อเรื่องอีเมล ผู้ส่ง ภาษาเริ่มต้น และเนื้อหาอีเมลในแต่ละภาษาที่คุณต้องการรองรับ</span><span class="sxs-lookup"><span data-stu-id="815f1-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="815f1-118">ทำตามขั้นตอนเหล่านี้เพื่อสร้างแม่แบบอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="815f1-119">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งสำนักงานใหญ่ \> พารามิเตอร์ \> แม่แบบอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="815f1-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="815f1-120">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="815f1-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="815f1-121">ในฟิลด์ **รหัสอีเมล** ให้ป้อนรหัสเพื่อช่วยระบุแม่แบบนี้</span><span class="sxs-lookup"><span data-stu-id="815f1-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="815f1-122">ในฟิลด์ **ชื่อผู้ส่ง** ให้ใส่ชื่อผู้ส่ง</span><span class="sxs-lookup"><span data-stu-id="815f1-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="815f1-123">ป้อนคำอธิบายที่มีความหมาย ลงใน **คำอธิบายอีเมล**</span><span class="sxs-lookup"><span data-stu-id="815f1-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="815f1-124">ใน **อีเมลผู้ส่ง** ป้อนที่อยู่อีเมลผู้ส่ง</span><span class="sxs-lookup"><span data-stu-id="815f1-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="815f1-125">ในส่วน **ทั่วไป** เลือกภาษาเริ่มต้นสำหรับเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="815f1-126">ภาษาเริ่มต้นจะถูกนำไปใช้เมื่อไม่มีเทมเพลตที่แปลเป็นภาษาท้องถิ่นสำหรับภาษาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="815f1-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="815f1-127">ขยายส่วน **เนื้อหาข้อความอีเมล** และเลือก **สร้าง** เพื่อสร้างเนื้อหาของแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="815f1-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="815f1-128">สำหรับรายการเนื้อหาแต่ละรายการ ให้เลือกภาษาและระบุบรรทัดหัวเรื่องอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="815f1-129">หากอีเมลจะมีเนื้อความให้ ตรวจสอบให้แน่ใจว่าได้ทำเครื่องหมายในช่อง **มีเนื้อความ** แล้ว</span><span class="sxs-lookup"><span data-stu-id="815f1-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="815f1-130">ในบานหน้าต่างการดำเนินการ เลือก **ข้อความอีเมล** เพื่อจัดทำแม่แบบเนื้อความของอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="815f1-131">ภาพต่อไปนี้แสดงตัวอย่างส่วนหนึ่งของการตั้งค่าแม่แบบอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-131">The following image shows some example email template settings.</span></span>

![การตั้งค่าเท็มเพลตอีเมล](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="815f1-133">สร้างเหตุการณ์ทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-133">Create an email event</span></span>

<span data-ttu-id="815f1-134">ทำตามขั้นตอนเหล่านี้เพื่อสร้างเหตุการณ์ทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="815f1-135">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> Retail และ commerce \> การตั้งค่าศูนย์ควบคุม \> โปรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**</span><span class="sxs-lookup"><span data-stu-id="815f1-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="815f1-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="815f1-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="815f1-137">เลือกแม่แบบอีเมลจากรายการแบบหล่นลง **รหัสอีเมล**</span><span class="sxs-lookup"><span data-stu-id="815f1-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="815f1-138">เลือก **ชนิดการแจ้งเตือนอีเมล** ที่เหมาะสมจากรายการแบบหล่นลง </span><span class="sxs-lookup"><span data-stu-id="815f1-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="815f1-139">เลือกกล่องกาเครื่องหมาย **ใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="815f1-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="815f1-140">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="815f1-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="815f1-141">ภาพต่อไปนี้แสดงตัวอย่างส่วนหนึ่งของการตั้งค่าการแจ้งเตือนเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="815f1-141">The following image shows some example event notification settings.</span></span>

![การตั้งค่าการแจ้งเตือนเหตุการณ์](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="815f1-143">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="815f1-143">Next steps</span></span>

<span data-ttu-id="815f1-144">ก่อนที่คุณจะสามารถส่งจดหมาย คุณต้องตั้งค่าคอนฟิกบริการจดหมายขาออกและตั้งค่าชุดงาน</span><span class="sxs-lookup"><span data-stu-id="815f1-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="815f1-145">สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าคอนฟิกและส่งอีเมล](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)</span><span class="sxs-lookup"><span data-stu-id="815f1-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="815f1-146">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="815f1-146">Additional resources</span></span>

[<span data-ttu-id="815f1-147">ตั้งค่าคอนฟิกและส่งอีเมล</span><span class="sxs-lookup"><span data-stu-id="815f1-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="815f1-148">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="815f1-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="815f1-149">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="815f1-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="815f1-150">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="815f1-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
