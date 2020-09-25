---
title: จัดการคำขอลาหยุดใน Teams
description: หัวข้อนี้จะแสดงวิธีการขอลาหยุดในแอป Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766771"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="6eac5-103">จัดการคำขอลาหยุดใน Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="6eac5-104">แอปพลิเคชัน Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้คุณสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดของคุณได้ใน Microsoft Teams ในทันที</span><span class="sxs-lookup"><span data-stu-id="6eac5-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="6eac5-105">คุณสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6eac5-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="6eac5-106">แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="6eac5-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="6eac5-107">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="6eac5-107">Install the app</span></span>

<span data-ttu-id="6eac5-108">คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="6eac5-109">ใน Microsoft Teams ให้เลือกจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="6eac5-109">In Microsoft Teams, select the ellipses.</span></span>

   ![จุดไข่ปลาของแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="6eac5-111">ค้นหา Dynamics 365 Human Resources และเลือกไทล์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="6eac5-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![ไทล์ HR แอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="6eac5-113">เลือก **เพิ่ม** เพื่อติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="6eac5-113">Select the **Add** button to install the app.</span></span>

   ![ติดตั้งแอปการลาหยุดใน Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="6eac5-115">ถ้าแอปนั้นไม่ได้ลงชื่อเข้าใช้คุณโดยอัตโนมัติ ให้เลือกแท็บ **การตั้งค่า** เพื่อลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="6eac5-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![แท็บการตั้งค่าแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="6eac5-117">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="6eac5-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="6eac5-118">ถ้าคุณมีสิทธิ์เข้าถึงอินสแตนซ์ของทรัพยากรบุคคลมากกว่าหนึ่งอินสแตนซ์ คุณสามารถเลือกสภาพแวดล้อมที่คุณต้องการเชื่อมต่อในแท็บ **การตั้งค่า** ได้</span><span class="sxs-lookup"><span data-stu-id="6eac5-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="6eac5-119">ขณะนี้แอปพลิเคชันไม่สนับสนุนบทบาทความปลอดภัยของผู้ดูแลระบบ และจะแสดงข้อความแสดงข้อผิดพลาดถ้าคุณลงชื่อเข้าใช้ด้วยบัญชีผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="6eac5-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="6eac5-120">เมื่อต้องการลงชื่อเข้าใช้ด้วยบัญชีอื่น บนแท็บ **การตั้งค่า** ให้เลือกปุ่ม **สลับบัญชี** แล้วลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้ที่ไม่มีสิทธิ์ของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="6eac5-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="6eac5-121">ใช้บอท</span><span class="sxs-lookup"><span data-stu-id="6eac5-121">Use the bot</span></span>

<span data-ttu-id="6eac5-122">หลังจากที่ติดตั้งแอปแล้ว ข้อความต้อนรับจะปรากฏขึ้นให้คุณทราบชนิดของการดำเนินการที่บอทสามารถใช้ในนามของคุณได้</span><span class="sxs-lookup"><span data-stu-id="6eac5-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![ข้อความต้อนรับของบอทในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="6eac5-124">เมื่อมีการโต้ตอบกับบอทครั้งแรก คุณอาจจำเป็นต้องลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="6eac5-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="6eac5-125">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="6eac5-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="6eac5-126">คุณสามารถขอให้บอทไปที่:</span><span class="sxs-lookup"><span data-stu-id="6eac5-126">You can ask the bot to:</span></span>

- <span data-ttu-id="6eac5-127">แสดงข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้</span><span class="sxs-lookup"><span data-stu-id="6eac5-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![แสดงยอดดุลในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="6eac5-129">แสดงรายละเอียดเพิ่มเติมเกี่ยวกับชนิดการลางานที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="6eac5-129">Show additional details about a specific leave type.</span></span>

   ![แสดงรายละเอียดแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="6eac5-131">เริ่มต้นการร้องขอการลาหยุดสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="6eac5-131">Start a leave request for you.</span></span>

   ![การขอลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="6eac5-133">หลังจากที่คุณเริ่มต้นคำขอการลางาน คุณสามารถปรับวันที่ืที่ถูกต้องภายในบัตรได้</span><span class="sxs-lookup"><span data-stu-id="6eac5-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![แก้ไขคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="6eac5-135">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้เลือก **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6eac5-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="6eac5-136">นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="6eac5-136">You can also select **Save as draft** to come back to it later.</span></span>

![ส่งคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="6eac5-138">จัดการคำขอลางานของคุณใน Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-138">Manage your leave in Teams</span></span>

<span data-ttu-id="6eac5-139">แท็บ **การลาหยุด** จะช่วยให้คุณสามารถดูสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6eac5-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="6eac5-140">ข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้</span><span class="sxs-lookup"><span data-stu-id="6eac5-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="6eac5-141">คำขอการลางานที่กำลังจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="6eac5-141">Upcoming leave requests</span></span>

- <span data-ttu-id="6eac5-142">คำขอลาหยุด</span><span class="sxs-lookup"><span data-stu-id="6eac5-142">Time-off requests</span></span>

- <span data-ttu-id="6eac5-143">ร่างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="6eac5-143">Draft leave requests</span></span>

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="6eac5-145">สร้างคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="6eac5-145">Create a new request</span></span>

1. <span data-ttu-id="6eac5-146">หากต้องการสร้างคำขอลางานใหม่ ให้เลือก **สร้างคำขอ**</span><span class="sxs-lookup"><span data-stu-id="6eac5-146">To create a new leave request, select **New request**.</span></span>

   ![สร้างคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="6eac5-148">ป้อนวันหรือวันที่ที่คุณต้องการลางาน แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6eac5-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![เพิ่มการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="6eac5-150">ถ้าใช้ได้ ให้ป้อนรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="6eac5-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="6eac5-151">ป้อนข้อคิดเห็นและเพิ่มไฟล์แนบใดๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="6eac5-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="6eac5-152">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6eac5-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="6eac5-153">นอกจากนี้คุณยังสามารถพิมพ์ **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="6eac5-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="6eac5-154">จัดการคำขอที่ร่าง</span><span class="sxs-lookup"><span data-stu-id="6eac5-154">Manage draft requests</span></span>

1. <span data-ttu-id="6eac5-155">เลือกแท็บ **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="6eac5-155">Select the **Drafts** tab.</span></span>

   ![แท็บแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="6eac5-157">เลือกดินสอเพื่อแก้ไขคำขอ หรือเลือกถังขยะเพื่อลบคำขอ</span><span class="sxs-lookup"><span data-stu-id="6eac5-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="6eac5-158">ทำการเปลี่ยนแปลงที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="6eac5-158">Make any necessary changes.</span></span> <span data-ttu-id="6eac5-159">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6eac5-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="6eac5-160">นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="6eac5-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![แก้ไขแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="6eac5-162">การแจ้งเตือนของ Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-162">Teams notifications</span></span>

<span data-ttu-id="6eac5-163">เมื่อคุณหรือผู้ปฏิบัติงานที่คุณเป็นผู้อนุมัติสำหรับส่งกาคำขอการลางาน คุณจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="6eac5-164">คุณสามารถเลือกการแจ้งเตือนที่จะดูได้</span><span class="sxs-lookup"><span data-stu-id="6eac5-164">You can select the notification to view it.</span></span> <span data-ttu-id="6eac5-165">การแจ้งเตือนจะปรากฏในพื้นที่ **การแชท** ด้วย</span><span class="sxs-lookup"><span data-stu-id="6eac5-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="6eac5-166">ถ้าคุณเป็นผู้อนุมัติ คุณสามารถเลือก **อนุมัติ** หรือ **ปฏิเสธ** ในการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="6eac5-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="6eac5-167">นอกจากนี้ คุณยังสามารถระบุข้อความที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="6eac5-167">You can also provide an optional message.</span></span>

![การแจ้งเตือนคำขอการลางานในแอป Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="6eac5-169">ดูปฏิทินการงานของทีมของคุณ</span><span class="sxs-lookup"><span data-stu-id="6eac5-169">View your team's leave calendar</span></span>

<span data-ttu-id="6eac5-170">ถ้าคุณเป็นผู้จัดการที่มีผู้ใต้บังคับบัญชาโดยตรง คุณสามารถดูการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของทีมของคุณได้</span><span class="sxs-lookup"><span data-stu-id="6eac5-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="6eac5-171">ในแอป Human Resources ใน Teams ให้เลือก **การลาหยุด**</span><span class="sxs-lookup"><span data-stu-id="6eac5-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="6eac5-172">เลือก **ปฏิทินของทีม**</span><span class="sxs-lookup"><span data-stu-id="6eac5-172">Select **Team calendar**.</span></span>

   ![ดูปฏิทินในแอป Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="6eac5-174">ปฏิทินแสดงการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของผู้บังคับบัญชาโดยตรงของคุณ</span><span class="sxs-lookup"><span data-stu-id="6eac5-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![ปฏิทินการลาหยุดในแอป Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="6eac5-176">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="6eac5-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="6eac5-177">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="6eac5-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="6eac5-178">ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="6eac5-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="6eac5-179">ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="6eac5-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="6eac5-180">อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/)</span><span class="sxs-lookup"><span data-stu-id="6eac5-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="6eac5-181">บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง</span><span class="sxs-lookup"><span data-stu-id="6eac5-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="6eac5-182">ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6eac5-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="6eac5-183">โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="6eac5-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="6eac5-184">บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="6eac5-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6eac5-185">ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure</span><span class="sxs-lookup"><span data-stu-id="6eac5-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="6eac5-186">เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="6eac5-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="6eac5-187">อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)</span><span class="sxs-lookup"><span data-stu-id="6eac5-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="6eac5-188">เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="6eac5-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="6eac5-189">กริดเหตุการณ์ Microsoft Azure และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="6eac5-190">เมื่อใช้คุณลักษณะการแจ้งเตือนสำหรับแอป Dynamics 365 Human Resources ใน Teams ข้อมูลลูกค้าบางรายจะมีการส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่มีการใช้บริการ Human Resources ของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="6eac5-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="6eac5-191">Dynamics 365 Human Resources ส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยังกริดเหตุการณ์ Microsoft Azure และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="6eac5-192">ข้อมูลนี้อาจจัดเก็บไว้นานถึง 24 ชั่วโมงและประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="6eac5-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="6eac5-193">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="6eac5-193">See also</span></span>

[<span data-ttu-id="6eac5-194">ดาวน์โหลดและติดตั้ง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="6eac5-195">ศูนย์ความช่วยเหลือ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="6eac5-196">แอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="6eac5-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
