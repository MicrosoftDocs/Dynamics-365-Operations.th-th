---
title: แก้ไขคู่มือและเท็มเพลตการเตรียมความพร้อมใน Dynamics 365 Talent - Onboard
description: หัวข้อนี้จะอธิบายถึงวิธีการเพิ่มกิจกรรมและข้อมูลอื่นๆ ไปยังคำแนะนำและเท็มเพลตการเตรียมความพร้อมใน Microsoft Dynamics 365 Talent - Onboard
author: andreabichsel
manager: ''
ms.date: 06/19/2019
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
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0f4c68acfe021e736c259e91a40ce7d43d401246
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552013"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-talent---onboard"></a><span data-ttu-id="7dd97-103">แก้ไขคู่มือและเท็มเพลตการเตรียมความพร้อมใน Dynamics 365 Talent - Onboard</span><span class="sxs-lookup"><span data-stu-id="7dd97-103">Edit onboarding guides and templates in Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7dd97-104">หลังจากที่คุณสร้างคู่มือหรือเท็มเพลตการเตรียมความพร้อมใน Microsoft Dynamics 365 Talent: Onboard คุณต้องเพิ่มคำแนะนำ กิจกรรม ผู้ติดต่อ และทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7dd97-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="7dd97-105">Onboard ช่วยให้คุณสามารถรวมเนื้อหาที่สมบูรณ์ใคู่มือการเตรียมความพร้อมของคุณ ซึ่งรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="7dd97-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="7dd97-106">วิดีโอ YouTube</span><span class="sxs-lookup"><span data-stu-id="7dd97-106">YouTube videos</span></span>
- <span data-ttu-id="7dd97-107">งานนำเสนอ Microsoft Sway</span><span class="sxs-lookup"><span data-stu-id="7dd97-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="7dd97-108">แอป Microsoft PowerApps</span><span class="sxs-lookup"><span data-stu-id="7dd97-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="7dd97-109">วิดีโอ Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="7dd97-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="7dd97-110">ฟอร์ม Microsoft Forms</span><span class="sxs-lookup"><span data-stu-id="7dd97-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="7dd97-111">Iframes ที่มีเนื้อหาเว็บ</span><span class="sxs-lookup"><span data-stu-id="7dd97-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="7dd97-112">แก้ไขบทนำหรือกิจกรรมที่นำเข้าจากเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7dd97-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="7dd97-113">ถ้าคุณสร้างคู่มือการเตรียมความพร้อมจากเท็มเพลต หรือถ้าคุณนำเข้ากิจกรรมจากเท็มเพลตหนึ่งไปยังอีกเท็มเพลตหนึ่ง คุณจะสังเกตเห็นปุ่ม **ล็อค** ในกิจกรรมที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="7dd97-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="7dd97-114">ซึ่งเรียกว่า *กิจกรรมที่มีการจัดการ*</span><span class="sxs-lookup"><span data-stu-id="7dd97-114">These are called *managed activities*.</span></span>

<span data-ttu-id="7dd97-115">[![กิจกรรมที่มีการจัดการ](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="7dd97-116">เมื่อคุณเลือกกิจกรรมที่มีการจัดการ คุณจะเห็นเท็มเพลตต้นทางที่ด้านบนของกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="7dd97-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="7dd97-117">[![แหล่งที่มาของกิจกรรมที่มีการจัดการ](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="7dd97-118">ถ้าคุณแก้ไขกิจกรรมในเท็มเพลต Onboard จะผลักดันการเปลี่ยนแปลงไปยังเท็มเพลตและคู่มือที่ยังไม่ได้ส่งทั้งหมดที่ใช้เท็มเพลตนั้น</span><span class="sxs-lookup"><span data-stu-id="7dd97-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="7dd97-119">ถ้าคุณเลือกคู่มือที่ยังไม่ได้ส่งตามเท็มเพลตที่คุณแก้ไข แล้วจากนั้น เลือกแท็บ **กิจกรรม** ในคู่มือ คุณจะเห็นการแจ้งเตือนว่าคู่มือของคุณมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="7dd97-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="7dd97-120">เมื่อต้องการยกเลิกการแจ้งเตือน เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7dd97-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="7dd97-121">[![เปลี่ยนการแจ้งเตือน](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="7dd97-122">คุณจะเห็นจุดสีดำถัดจากกิจกรรมที่มีการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="7dd97-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="7dd97-123">[![กิจกรรมที่เปลี่ยน](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="7dd97-124">คุณไม่สามารถแก้ไขกิจกรรมที่มีการจัดการภายนอกเท็มเพลตต้นฉบับ ยกเว้นการเพิ่มผู้รับ วันที่ครบกำหนดชำระ หรือข้อมูลอื่นๆ ในส่วนทางด้านขวามือของกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="7dd97-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="7dd97-125">ถ้าคุณต้องการแก้ไขกิจกรรมที่มีการจัดการ หรือถ้าคุณไม่ต้องการให้กิจกรรมรับการปรับปรุงจากเท็มเพลตที่มา ให้เลือกปุ่ม **ล็อค** สำหรับกิจกรรมนั้น</span><span class="sxs-lookup"><span data-stu-id="7dd97-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="7dd97-126">ปุ่ม **ล็อค** จะหายไป</span><span class="sxs-lookup"><span data-stu-id="7dd97-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="7dd97-127">กิจกรรมจะไม่ได้รับการจัดการโดยเท็มเพลตเดิมอีกต่อไป และจะไม่ได้รับการปรับปรุงจากเท็มเพลตนั้นอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="7dd97-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="7dd97-128">การปรับปรุงที่คุณทำกับกิจกรรมจะไม่มีผลกระทบต่อเท็มเพลตเดิม</span><span class="sxs-lookup"><span data-stu-id="7dd97-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="7dd97-129">ถ้าคุณลบกิจกรรมออกจากคู่มือ และผลักดันการเปลี่ยนแปลงจากเท็มเพลตของคู่มือนั้น กิจกรรมจะยังคงถูกลบออกในคู่มือ</span><span class="sxs-lookup"><span data-stu-id="7dd97-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="7dd97-130">ผู้ติดต่อและทรัพยากรไม่ได้รับการจัดการโดยเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7dd97-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="7dd97-131">นอกจากนี้ ส่วนไม่ได้รับการจัดการ ดังนั้นถ้าคุณเพิ่มหรือแก้ไขส่วนในเท็มเพลต การเปลี่ยนแปลงจะไม่ถูกผลักไปที่คู่มือหรือเท็มเพลตที่ใช้เท็มเพลตนั้น</span><span class="sxs-lookup"><span data-stu-id="7dd97-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="7dd97-132">ถ้าคุณเพิ่มกิจกรรมใหม่ลงในเท็มเพลต กิจกรรมใหม่จะถูกผลักไปที่คู่มือและเท็มเพลตโดยยึดตามเท็มเพลตนี้ และกิจกรรมใหม่จะแสดงที่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="7dd97-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="7dd97-133">นำเข้ากิจกรรมจากเท็มเพลตอื่น</span><span class="sxs-lookup"><span data-stu-id="7dd97-133">Import activities from another template</span></span>

<span data-ttu-id="7dd97-134">คุณสามารถนำเข้ากิจกรรมจากเท็มเพลตหนึ่งรายการขึ้นไปลงในคู่มือหรือเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7dd97-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="7dd97-135">เลือกคู่มือหรือเท็มเพลตที่คุณต้องการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="7dd97-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="7dd97-136">เลือกแท็บ **กิจกรรม**</span><span class="sxs-lookup"><span data-stu-id="7dd97-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="7dd97-137">เลือกแท็บ **นำเข้า** ในส่วนทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="7dd97-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="7dd97-138">[![นำเข้ากิจกรรม](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="7dd97-139">เมื่อต้องการแสดงตัวอย่างงานในแท็บใหม่ในเบราว์เซอร์ของคุณ ให้เลือกปุ่ม **เปิดในแท็บใหม่** บนเท็มเพลตใดๆ</span><span class="sxs-lookup"><span data-stu-id="7dd97-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="7dd97-140">[![นำเข้ากิจกรรม](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="7dd97-141">ลากและวางเท็มเพลตที่ต้องการไปยังตำแหน่งในเท็มเพลตคู่มือของคุณที่ซึ่งคุณต้องการให้กิจกรรมปรากฏ</span><span class="sxs-lookup"><span data-stu-id="7dd97-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="7dd97-142">ดำเนินการแก้ไขคู่มือหรือเท็มเพลตของคุณต่อไป</span><span class="sxs-lookup"><span data-stu-id="7dd97-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="7dd97-143">กิจกรรมที่นำเข้าจะมีปุ่ม **ล็อค** ซึ่งบ่งชี้ว่ากิจกรรมเหล่านั้นได้รับการจัดการโดยเท็มเพลตที่คุณนำเข้า</span><span class="sxs-lookup"><span data-stu-id="7dd97-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="7dd97-144">เมื่อคุณทำการเปลี่ยนแปลงไปยังเท็มเพลตที่คุณนำเข้า กิจกรรมเหล่านั้นจะปรับปรุงในเท็มเพลตที่คุณนำเข้า</span><span class="sxs-lookup"><span data-stu-id="7dd97-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="7dd97-145">อย่างไรก็ตาม การเปลี่ยนแปลงจะไม่ถูกผลักดันโดยอัตโนมัติไปยังคู่มือใดๆ ที่สร้างขึ้นจากเท็มเพลตที่คุณนำเข้า</span><span class="sxs-lookup"><span data-stu-id="7dd97-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="7dd97-146">ส่งการเปลี่ยนแปลงจากเท็มเพลตหนึ่งไปยังเท็มเพลตหรือคู่มืออื่นๆ</span><span class="sxs-lookup"><span data-stu-id="7dd97-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="7dd97-147">ถ้าคุณแก้ไขเท็มเพลตที่มีกิจกรรมที่ใช้ในเท็มเพลตหรือคู่มืออื่นๆ คุณต้องผลักดันการเปลี่ยนแปลง ถ้าคุณต้องการให้ปรากฏในเท็มเพลตหรือคู่มืออื่นๆ</span><span class="sxs-lookup"><span data-stu-id="7dd97-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="7dd97-148">ถ้าคุณไม่แน่ใจว่ามีการใช้กิจกรรมของเท็มเพลตของคุณในเท็มเพลตหรือคู่มืออื่นๆ หรือไม่ เลือกแท็บ **ที่ใช้ใน** เพื่อดูตำแหน่งที่กิจกรรมเหล่านั้นปรากฏ</span><span class="sxs-lookup"><span data-stu-id="7dd97-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="7dd97-149">[![ดูคู่มือและกิจกรรมของเท็มเพลตที่ใช้ใน](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="7dd97-150">เมื่อต้องการผลักดันการเปลี่ยนแปลงของคุณ:</span><span class="sxs-lookup"><span data-stu-id="7dd97-150">To push your changes:</span></span>

1. <span data-ttu-id="7dd97-151">บันทึกการเปลี่ยนแปลงของคุณโดยเลือกปุ่ม **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7dd97-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="7dd97-152">ถ้าคุณไม่ได้ดำเนินการนี้ ระบบจะขอให้คุณบันทึกการเปลี่ยนแปลงของคุณในขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="7dd97-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="7dd97-153">เลือก **ส่งการเปลี่ยนแปลงเหล่านี้**</span><span class="sxs-lookup"><span data-stu-id="7dd97-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="7dd97-154">เพิ่มหรือแก้ไขบทนำ</span><span class="sxs-lookup"><span data-stu-id="7dd97-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="7dd97-155">บนแท็บ **บทนำ** ให้ป้อนชื่อสำหรับคู่มือของคุณและข้อความเปิด</span><span class="sxs-lookup"><span data-stu-id="7dd97-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="7dd97-156">เมื่อต้องการใช้ข้อความตัวอย่าง ให้เลือก **ใช้ข้อความนี้**</span><span class="sxs-lookup"><span data-stu-id="7dd97-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="7dd97-157">[![แท็บบทนำในเท็มเพลต Onboard](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="7dd97-158">ใช้ปุ่มการจัดรูปแบบเพื่อเรียกข้อความตามที่คุณต้องการ หรือเพื่อเพิ่มรูปหรือลิงค์</span><span class="sxs-lookup"><span data-stu-id="7dd97-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="7dd97-159">เลือก **บันทึก** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="7dd97-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="7dd97-160">เพิ่มหรือแก้ไขกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="7dd97-160">Add or edit activities</span></span>

1. <span data-ttu-id="7dd97-161">บนแท็บ **กิจกรรม** ให้ลากรายการจากทางขวาไปยังพื้นที่สำหรับแก้ไข</span><span class="sxs-lookup"><span data-stu-id="7dd97-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="7dd97-162">เมื่อต้องการจัดระเบียบคู่มือของคุณให้เป็นส่วนๆ ลากรายการ **ส่วนใหม่** ไปยังพื้นที่สำหรับแก้ไข และป้อนชื่อและคำอธิบายที่เลือกกำหนดได้สำหรับส่วน</span><span class="sxs-lookup"><span data-stu-id="7dd97-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="7dd97-163">การเพิ่มส่วนใหม่ลงในคู่มือหรือเท็มเพลตการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="7dd97-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="7dd97-164">เมื่อต้องการเพิ่มกิจกรรมสำหรับการจ้างงานใหม่ของคุณให้เสร็จสมบูรณ์ ให้ลากรายการ **กิจกรรมใหม่** ไปยังพื้นที่สำหรับแก้ไข และป้อนชื่อและคำอธิบายสำหรับกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="7dd97-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="7dd97-165">การเพิ่มกิจกรรมใหม่ลงในคู่มือหรือเท็มเพลตการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="7dd97-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="7dd97-166">เพิ่มเนื้อหาที่สมบูรณ์ให้กับคู่มือการเตรียมความพร้อมของคุณ:</span><span class="sxs-lookup"><span data-stu-id="7dd97-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="7dd97-167">เมื่อต้องการเพิ่มวิดีโอ YouTube ให้ลากรายการ **YouTube** ไปยังพื้นที่สำหรับแก้ไข ป้อนชื่อและคำอธิบายสำหรับกิจกรรมนั้น และป้อน URL สำหรับวิดีโอ YouTube</span><span class="sxs-lookup"><span data-stu-id="7dd97-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="7dd97-168">เมื่อต้องการเพิ่มงานนำเสนอหรือจดหมายข่าว Sway ให้ลากรายการ **Sway** ไปที่พื้นที่สำหรับแก้ไข ป้อนชื่อและคำอธิบายสำหรับกิจกรรม และป้อน URL ที่ฝังไว้สำหรับการนำเสนอหรือจดหมายข่าว Sway</span><span class="sxs-lookup"><span data-stu-id="7dd97-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="7dd97-169">เมื่อต้องการเพิ่มแอป PowerApps ให้ลากรายการ **PowerApps** ไปยังพื้นที่สำหรับแก้ไข ป้อนชื่อและคำอธิบายสำหรับกิจกรรม และเลือกแอป PowerApps หรือป้อนรหัสแอป PowerApps อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7dd97-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="7dd97-170">เมื่อต้องการเพิ่มวิดีโอ Microsoft Stream ให้ลากรายการ **Microsoft Stream** ไปยังพื้นที่สำหรับแก้ไข ป้อนชื่อและคำอธิบายสำหรับกิจกรรมนั้น และป้อน URL สำหรับวิดีโอ Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="7dd97-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="7dd97-171">เมื่อต้องการเพิ่มฟอร์ม Microsoft Forms ให้ลากรายการ **Microsoft Forms** ไปที่พื้นที่สำหรับแก้ไข ป้อนชื่อและคำอธิบายสำหรับกิจกรรม ป้อน URL สำหรับฟอร์ม Microsoft Forms และระบุขนาดของพื้นที่หน้าจอ</span><span class="sxs-lookup"><span data-stu-id="7dd97-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="7dd97-172">เมื่อต้องการเพิ่ม iframe ที่มีเนื้อหาเว็บ ให้ลากรายการ **เนื้อหาเว็บ (iframe)** ไปที่พื้นที่สำหรับแก้ไข ป้อนชื่อและคำอธิบายสำหรับกิจกรรม ป้อน URL สำหรับเนื้อหาเว็บ และระบุขนาดของพื้นที่หน้าจอ</span><span class="sxs-lookup"><span data-stu-id="7dd97-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="7dd97-173">การเพิ่มเนื้อหาที่สมบูรณ์ลงในคู่มือหรือเท็มเพลตการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="7dd97-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="7dd97-174">ไม่จำเป็นต้องระบุ: ในพื้นที่ทางด้านขวาของแต่ละกิจกรรม ให้กำหนดกิจกรรมให้กับบุคคลหรือบทบาทหนึ่งๆ เพิ่มวันที่ครบกำหนดและผู้ติดต่อ และกำหนดสีของประเภท</span><span class="sxs-lookup"><span data-stu-id="7dd97-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="7dd97-175">เมื่อคุณกำหนดกิจกรรมให้กับบุคคลหรือบทบาทหนึ่งๆ งานจะถูกสร้างขึ้นสำหรับแต่ละบุคคล</span><span class="sxs-lookup"><span data-stu-id="7dd97-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="7dd97-176">งานนี้จะปรากฏขึ้นบนเมนู **งาน** ใน Onboard</span><span class="sxs-lookup"><span data-stu-id="7dd97-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="7dd97-177">[![การกำหนดกิจกรรมในคู่มือหรือเท็มเพลตการเตรียมความพร้อม](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="7dd97-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="7dd97-178">เลือก **บันทึก** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="7dd97-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="7dd97-179">ถ้าต้องการลบกิจกรรมหรือส่วน ให้เลือกปุ่ม **ลบ** (สัญลักษณ์ถังขยะ) ในมุมบนขวาของกิจกรรมหรือส่วน</span><span class="sxs-lookup"><span data-stu-id="7dd97-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="7dd97-180">เมื่อต้องการจัดเรียงกิจกรรมและส่วนใหม่ ให้ลากไปยังสถานที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="7dd97-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="7dd97-181">เพิ่มหรือแก้ไขผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="7dd97-181">Add or edit contacts</span></span>

<span data-ttu-id="7dd97-182">คุณสามารถเพิ่มผู้ติดต่อที่สามารถช่วยให้การจ้างงานใหม่ของคุณประสบความสำเร็จตั้งแต่วันที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7dd97-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="7dd97-183">ผู้ติดต่อเหล่านี้อาจเป็นผู้สรรหา เพื่อนร่วมทีม คู่หูการเตรียมความพร้อม ผู้ให้คำปรึกษา ผู้ดูแลระบบ และเจ้าหน้าที่สนับสนุนด้าน IT</span><span class="sxs-lookup"><span data-stu-id="7dd97-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="7dd97-184">บนแท็บ **ผู้ติดต่อ** ให้เลือก **ผู้ติดต่อใหม่**</span><span class="sxs-lookup"><span data-stu-id="7dd97-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="7dd97-185">ในกล่องโต้ตอบ **เพิ่มสมาชิกทีมงาน** ให้ป้อนชื่อหรือที่อยู่อีเมลของผู้ติดต่อ ให้ป้อนคำอธิบายโดยย่อที่อธิบายวิธีการที่ผู้ติดต่อสามารถช่วยพนักงานใหม่ แล้วจากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="7dd97-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="7dd97-186">การเพิ่มผู้ติดต่อลงในคู่มือหรือเท็มเพลตการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="7dd97-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="7dd97-187">อีกทางหนึ่งคือ คุณสามารถเลือกผู้ติดต่อหนึ่งรายขึ้นไปภายใต้ **คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="7dd97-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="7dd97-188">เลือก **บันทึก** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="7dd97-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="7dd97-189">ถ้าต้องการลบผู้ติดต่อ ให้เลือกปุ่ม **ลบ** (สัญลักษณ์ถังขยะ) ที่อยู่ด้านขวาของผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="7dd97-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="7dd97-190">ถ้าต้องการแก้ไขผู้ติดต่อ ให้เลือกปุ่ม **แก้ไข** (สัญลักษณ์ดินสอ) ที่อยู่ด้านขวาของผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="7dd97-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="7dd97-191">เพิ่มหรือแก้ไขทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7dd97-191">Add or edit resources</span></span>

<span data-ttu-id="7dd97-192">คุณสามารถเพิ่มไฟล์ที่มีประโยชน์ แผนที่ และลิงค์ไปยังส่วน **ทรัพยากร** ของคู่มือการเตรียมความพร้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="7dd97-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="7dd97-193">บนแท็บ **ทรัพยากร** ให้เลือก **ทรัพยากรใหม่**</span><span class="sxs-lookup"><span data-stu-id="7dd97-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="7dd97-194">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7dd97-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="7dd97-195">เมื่อต้องการเพิ่มไฟล์ ให้เลือกแท็บ **ไฟล์** และลากไฟล์นั้นไปยังพื้นที่ที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="7dd97-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="7dd97-196">(หรือคลิกที่ใดก็ได้ในพื้นที่ดังกล่าวเพื่อเรียกดูไฟล์บนคอมพิวเตอร์ของคุณ หรือเลือก **เรียกดู OneDrive**) ป้อนชื่อสำหรับไฟล์ แล้วจากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="7dd97-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="7dd97-197">เมื่อต้องการเพิ่มลิงค์ ให้เลือกแท็บ **ลิงค์** ป้อนชื่อและที่อยู่สำหรับลิงค์ แล้วจากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="7dd97-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="7dd97-198">เมื่อต้องการเพิ่มแผนที่ ให้เลือกแท็บ **แผนที่** ป้อนชื่อและที่อยู่สำหรับแผนที่ แล้วจากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="7dd97-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="7dd97-199">Onboard จะรวมแผนที่ของที่อยู่ที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="7dd97-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="7dd97-200">การเพิ่มทรัพยากรลงในคู่มือหรือเท็มเพลตการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="7dd97-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="7dd97-201">เลือก **บันทึก** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="7dd97-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="7dd97-202">ถ้าต้องการลบทรัพยากร ให้เลือกปุ่ม **ลบ** (สัญลักษณ์ถังขยะ) ที่อยู่ด้านขวาของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7dd97-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="7dd97-203">ถ้าต้องการแก้ไขผู้ติดต่อ ให้เลือกปุ่ม **แก้ไข** (สัญลักษณ์ดินสอ) ที่อยู่ด้านขวาของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7dd97-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7dd97-204">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7dd97-204">Next steps</span></span>

- [<span data-ttu-id="7dd97-205">แบ่งปันเนื้อหากับผู้สนับสนุนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="7dd97-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="7dd97-206">ดูสถานะของงานและพนักงานการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="7dd97-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="7dd97-207">สร้างทีมการจ้างงานใน Onboard</span><span class="sxs-lookup"><span data-stu-id="7dd97-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="7dd97-208">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="7dd97-208">See also</span></span>

- [<span data-ttu-id="7dd97-209">ลองหรือซื้อแอป Onboard</span><span class="sxs-lookup"><span data-stu-id="7dd97-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="7dd97-210">มีอะไรใหม่</span><span class="sxs-lookup"><span data-stu-id="7dd97-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="7dd97-211">บันทึกย่อประจำรุ่น</span><span class="sxs-lookup"><span data-stu-id="7dd97-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="7dd97-212">รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="7dd97-212">Get support</span></span>](./talent-support.md)
