---
title: เรียกใช้แอป Dynamics 365 for Talent - Onboard
description: หัวข้อนี้จะอธิบายถึงวิธีการเรียกใช้รุ่นสแตนด์อะโลนของแอป Microsoft Dynamics 365 for Talent - Onboard หรือรุ่นที่มี Comprehensive Hiring Add-On
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e83bbd71089b145c6c99780ea9516793c5238b33
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731666"
---
# <a name="get-the-dynamics-365-for-talent-onboard-app"></a><span data-ttu-id="d5b01-103">เรียกใช้แอป Dynamics 365 for Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="d5b01-103">Get the Dynamics 365 for Talent: Onboard app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5b01-104">คุณสามารถดูการสาธิตและลองใช้แอป Microsoft Dynamics 365 for Talent: Onboard ได้ฟรีจาก [หน้าผลิตภัณฑ์ Onboard](https://dynamics.microsoft.com/talent/onboard/)</span><span class="sxs-lookup"><span data-stu-id="d5b01-104">You can view a demo and try the Microsoft Dynamics 365 for Talent: Onboard app for free from the [Onboard product page](https://dynamics.microsoft.com/talent/onboard/).</span></span>

> [!NOTE]
> <span data-ttu-id="d5b01-105">การทดลองใช้ฟรีต้องใช้บัญชีอีเมลสำหรับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="d5b01-105">The free trial requires a business email account.</span></span>

<span data-ttu-id="d5b01-106">คุณสามารถซื้อการบอกรับเป็นสมาชิก Onboard เป็นแอปแบบสแตนด์อโลน หรือเป็นส่วนหนึ่งของ Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="d5b01-106">You can purchase a subscription to Onboard as either a stand-alone app or part of Dynamics 365 for Talent.</span></span> <span data-ttu-id="d5b01-107">Talent เป็นระบบการจัดการทุนมนุษย์ที่ครอบคลุม (HCM) ซึ่งรวมถึง Dynamics 365 for Talent: Attract, Onboard, and Core HR</span><span class="sxs-lookup"><span data-stu-id="d5b01-107">Talent is a comprehensive human capital management (HCM) system that includes Dynamics 365 for Talent: Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="d5b01-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการซื้อ Onboard โปรดดูที่ [หน้าผลิตภัณฑ์ Onboard](https://dynamics.microsoft.com/talent/onboard/)</span><span class="sxs-lookup"><span data-stu-id="d5b01-108">For more information about how to purchase Onboard, see the [Onboard product page](https://dynamics.microsoft.com/talent/onboard/).</span></span>

<span data-ttu-id="d5b01-109">ในระหว่างกระบวนการทดลองหรือการซื้อ คุณจะตั้งค่าที่อยู่อีเมลและรหัสผ่านของ Microsoft 365 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5b01-109">During the trial or purchase process, you will set up your Microsoft 365 email address and password.</span></span> <span data-ttu-id="d5b01-110">ตรวจสอบให้แน่ใจว่าได้บันทึกค่าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="d5b01-110">Be sure to make a note of these values.</span></span>

> [!WARNING]
> <span data-ttu-id="d5b01-111">คุณไม่สามารถย้ายข้อมูลจากการทดลองของคุณไปยังสภาพแวดล้อมการบอกรับเป็นสมาชิกที่ชำระเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5b01-111">You can't migrate data from your trial to your paid subscription environment.</span></span> <!--Reviewers: please verify.-->

<span data-ttu-id="d5b01-112">เพื่อค้นหาเกี่ยวกับคุณลักษณะใหม่ๆ ใน Talent ดู [มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent](./whats-new.md) และ [บันทึกย่อประจำรุ่นของ Dynamics 365 และ Power Platform](https://docs.microsoft.com/business-applications-release-notes/index)</span><span class="sxs-lookup"><span data-stu-id="d5b01-112">To find out about new features in Talent, see [What's new or changed in Dynamics 365 for Talent](./whats-new.md) and [Dynamics 365 and Power Platform release notes](https://docs.microsoft.com/business-applications-release-notes/index).</span></span> <span data-ttu-id="d5b01-113">ถ้าคุณต้องการแสดงตัวอย่างคุณลักษณะใหม่ๆ ใน Onboard โปรดดูที่ [เข้าถึงคุณลักษณะการแสดงตัวอย่างใน Talent](./access-preview-feature.md)</span><span class="sxs-lookup"><span data-stu-id="d5b01-113">If you want to preview new features in Onboard, see [Access preview features in Talent](./access-preview-feature.md).</span></span>

<span data-ttu-id="d5b01-114">ถ้าคุณเป็นผู้เชี่ยวชาญด้าน IT และต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเตรียมใช้งานแอป Onboard สองรุ่น โปรดดู [การเตรียมใช้งานสำหรับแอป Onboard](./modular-app-tech-faq.md)ดูที่การจัดเตรียมสำหรับแอป onboard</span><span class="sxs-lookup"><span data-stu-id="d5b01-114">If you're an IT professional and want to learn more about how the two versions of the Onboard app are provisioned, see [Provisioning for the Onboard app](./modular-app-tech-faq.md).</span></span>

## <a name="get-started-with-onboard"></a><span data-ttu-id="d5b01-115">เริ่มต้นใช้งาน Onboard</span><span class="sxs-lookup"><span data-stu-id="d5b01-115">Get started with Onboard</span></span>

<span data-ttu-id="d5b01-116">เมื่อคุณเปิด Onboard เป็นครั้งแรก คุณจะได้รับเชิญให้เริ่มต้นการแนะนำการใช้งานของศูนย์การจัดการ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d5b01-116">When you open Onboard for the first time, you're invited to start a tour of the Microsoft 365 admin center.</span></span> <span data-ttu-id="d5b01-117">ศูนย์การจัดการคือ สถานที่ที่คุณตั้งค่าองค์กรของคุณ จัดการผู้ใช้ และจัดการการบอกรับเป็นสมาชิกของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5b01-117">The admin center is where you set up your organization, manage users, and manage your subscriptions.</span></span> <span data-ttu-id="d5b01-118">(หนึ่งในการบอกรับเป็นสมาชิกดังกล่าวคือการบอกรับเป็นสมาชิก Onboard ของคุณ) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับศูนย์การจัดการ Microsoft 365 โปรดดู [เกี่ยวกับศูนย์การจัดการ Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="d5b01-118">(One of those subscriptions is your Onboard subscription.) For more information about the Microsoft 365 admin center, see [About the Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

<span data-ttu-id="d5b01-119">เมื่อต้องการเข้าถึงแอป Onboard ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d5b01-119">To get to the Onboard app, follow these steps.</span></span>

1. <span data-ttu-id="d5b01-120">เปิด [หน้าการลงชื่อเข้าใช้ Microsoft](https://portal.office.com/)</span><span class="sxs-lookup"><span data-stu-id="d5b01-120">Open the [Microsoft sign-in page](https://portal.office.com/).</span></span>
2. <span data-ttu-id="d5b01-121">เมื่อคุณได้รับข้อความแจ้ง ให้ป้อนที่อยู่อีเมลและรหัสผ่านของ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d5b01-121">When you're prompted, enter your Microsoft 365 email address and password.</span></span>
3. <span data-ttu-id="d5b01-122">เลือกตัวเรียกใช้แอปในมุมบนซ้าย แล้วจากนั้น เลือก **Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="d5b01-122">Select the app launcher in the upper left, and then select **Dynamics 365**.</span></span>

    <span data-ttu-id="d5b01-123">[![กำลังเข้าถึง Dynamics 365](./media/onboard-start-dynamics365.png)](./media/onboard-start-dynamics365.png)</span><span class="sxs-lookup"><span data-stu-id="d5b01-123">[![Accessing Dynamics 365](./media/onboard-start-dynamics365.png)](./media/onboard-start-dynamics365.png)</span></span>

4. <span data-ttu-id="d5b01-124">เลือกไทล์ **Talent: Onboard**</span><span class="sxs-lookup"><span data-stu-id="d5b01-124">Select the **Talent: Onboard** tile.</span></span>

    <span data-ttu-id="d5b01-125">[![กำลังเปิด Onboard](./media/onboard-start-onboard.png)](./media/onboard-start-onboard.png)</span><span class="sxs-lookup"><span data-stu-id="d5b01-125">[![Opening Onboard](./media/onboard-start-onboard.png)](./media/onboard-start-onboard.png)</span></span>

<span data-ttu-id="d5b01-126">การลงชื่อเข้าใช้ครั้งแรกของคุณอาจใช้เวลาสักครู่ เนื่องจากต้องมีการเริ่มต้นสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="d5b01-126">Your first sign-in might take a few minutes, because the environment must be initialized.</span></span>

## <a name="try-the-walkthrough"></a><span data-ttu-id="d5b01-127">ลองใช้การฝึกปฏิบัติ</span><span class="sxs-lookup"><span data-stu-id="d5b01-127">Try the walkthrough</span></span>

<span data-ttu-id="d5b01-128">เมื่อคุณเปิด Onboard ครั้งแรก คุณสามารถเลือก **เริ่มต้นการฝึกปฏิบัติ** เพื่อเริ่มต้นใช้งานเท็มเพลตการทำงานได้</span><span class="sxs-lookup"><span data-stu-id="d5b01-128">When you first open Onboard, you can select **Start the walkthrough** to get started with a working template.</span></span>

<span data-ttu-id="d5b01-129">ถ้าคุณข้ามการฝึกปฏิบัติ คุณสามารถเข้าถึงได้ในภายหลังโดยการเลือกปุ่ม **วิธีใช้** (**?**) และจากนั้น เลือก **เริ่มต้นใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="d5b01-129">If you skip the walkthrough, you can access it later by selecting the **Help** button (**?**) and then selecting **Get started**.</span></span>

![[<span data-ttu-id="d5b01-130">เริ่มต้นการฝึกปฏิบัติ Onboard</span><span class="sxs-lookup"><span data-stu-id="d5b01-130">Starting the Onboard walkthrough</span></span>](./media/onboard-start-walkthrough.png)](./media/onboard-start-walkthrough.png)

## <a name="change-the-domain-name"></a><span data-ttu-id="d5b01-131">เปลี่ยนชื่อโดเมน</span><span class="sxs-lookup"><span data-stu-id="d5b01-131">Change the domain name</span></span>

<span data-ttu-id="d5b01-132">ถ้าคุณยอมรับชื่อโดเมนเริ่มต้นเมื่อคุณลงชื่อสมัครใช้งานด้วย Onboard คุณสามารถเปลี่ยนเป็นโดเมนอื่นในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="d5b01-132">If you accepted the default domain name when you signed up with Onboard, you can change it to another domain later.</span></span> <span data-ttu-id="d5b01-133">(ชื่อโดเมนเริ่มต้นสิ้นสุดใน **onmicrosoft.com**)</span><span class="sxs-lookup"><span data-stu-id="d5b01-133">(The default domain name ends in **onmicrosoft.com**.)</span></span>

1. <span data-ttu-id="d5b01-134">เปิด [หน้าการลงชื่อเข้าใช้ Microsoft](https://portal.office.com/)</span><span class="sxs-lookup"><span data-stu-id="d5b01-134">Open the [Microsoft sign-in page](https://portal.office.com/).</span></span>
2. <span data-ttu-id="d5b01-135">เมื่อคุณได้รับข้อความแจ้ง ให้ป้อนที่อยู่อีเมลและรหัสผ่านของ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d5b01-135">When you're prompted, enter your Microsoft 365 email address and password.</span></span>
3. <span data-ttu-id="d5b01-136">ถ้าคุณเห็นคำแนะนำในการเพิ่มโดเมนของคุณเองภายใต้ **แนะนำสำหรับคุณ** ให้เลือก **ดูคำแนะนำ** และทำตามพร้อมท์</span><span class="sxs-lookup"><span data-stu-id="d5b01-136">If you see a recommendation to add your own domain under **Recommended for you**, select **View recommendation**, and follow the prompts.</span></span> <span data-ttu-id="d5b01-137">ถ้าคุณไม่เห็นคำแนะนำ ให้เลือก **แสดงทั้งหมด** บนเมนูด้านซ้าย เลือก **การตั้งค่า** เลือก **โดเมน** แล้วจากนั้น เลือก **เพิ่มโดเมน** หรือ **ซื้อโดเมน** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d5b01-137">If you don't see the recommendation, select **Show all** on the menu on the left, select **Setup**, select **Domains**, and then select either **Add domain** or **Buy domain**.</span></span> <span data-ttu-id="d5b01-138">จากนั้น ให้ทำตามพร้อมท์</span><span class="sxs-lookup"><span data-stu-id="d5b01-138">Then follow the prompts.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d5b01-139">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d5b01-139">Next steps</span></span>

- [<span data-ttu-id="d5b01-140">สร้างคู่มือการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="d5b01-140">Create an onboarding guide</span></span>](./onboard-create-guide.md)
- [<span data-ttu-id="d5b01-141">สร้างเท็มเพลตการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="d5b01-141">Create an onboarding template</span></span>](./onboard-create-template.md)
- [<span data-ttu-id="d5b01-142">แก้ไขคู่มือและเท็มเพลตการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="d5b01-142">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="d5b01-143">แบ่งปันเนื้อหากับผู้สนับสนุนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="d5b01-143">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="d5b01-144">ดูสถานะของงานและพนักงานการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="d5b01-144">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="d5b01-145">สร้างทีมการจ้างงานใน Onboard</span><span class="sxs-lookup"><span data-stu-id="d5b01-145">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="d5b01-146">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d5b01-146">See also</span></span>

- [<span data-ttu-id="d5b01-147">ลองหรือซื้อแอป Onboard</span><span class="sxs-lookup"><span data-stu-id="d5b01-147">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="d5b01-148">มีอะไรใหม่</span><span class="sxs-lookup"><span data-stu-id="d5b01-148">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="d5b01-149">บันทึกย่อประจำรุ่น</span><span class="sxs-lookup"><span data-stu-id="d5b01-149">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="d5b01-150">รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d5b01-150">Get support</span></span>](./talent-support.md)
