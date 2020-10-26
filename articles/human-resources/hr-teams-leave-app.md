---
title: จัดการคำขอลาหยุดใน Teams
description: หัวข้อนี้จะแสดงวิธีการขอลาหยุดในแอป Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
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
ms.openlocfilehash: c6856e417ee47f8f582f797c5bcedcff23a1432f
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930004"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="8a52f-103">จัดการคำขอลาหยุดใน Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="8a52f-104">แอปพลิเคชัน Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้คุณสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดของคุณได้ใน Microsoft Teams ในทันที</span><span class="sxs-lookup"><span data-stu-id="8a52f-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="8a52f-105">คุณสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูลและเริ่มต้นการร้องขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="8a52f-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="8a52f-106">แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="8a52f-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="8a52f-107">นอกจากนี้คุณยังสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะเกิดขึ้นในทีมและการสนทนาภายนอกแอปพลิเคชันทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="8a52f-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="8a52f-108">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="8a52f-108">Install the app</span></span>

<span data-ttu-id="8a52f-109">คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="8a52f-110">ใน Microsoft Teams ให้เลือกจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="8a52f-110">In Microsoft Teams, select the ellipses.</span></span>

   ![จุดไข่ปลาของแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="8a52f-112">ค้นหา Dynamics 365 Human Resources และเลือกไทล์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="8a52f-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![ไทล์ HR แอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="8a52f-114">เลือก **เพิ่ม** เพื่อติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="8a52f-114">Select the **Add** button to install the app.</span></span>

   ![ติดตั้งแอปการลาหยุดใน Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="8a52f-116">ถ้าแอปนั้นไม่ได้ลงชื่อเข้าใช้คุณโดยอัตโนมัติ ให้เลือกแท็บ **การตั้งค่า** เพื่อลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8a52f-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![แท็บการตั้งค่าแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="8a52f-118">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="8a52f-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="8a52f-119">ถ้าคุณมีสิทธิ์เข้าถึงอินสแตนซ์ของทรัพยากรบุคคลมากกว่าหนึ่งอินสแตนซ์ คุณสามารถเลือกสภาพแวดล้อมที่คุณต้องการเชื่อมต่อในแท็บ **การตั้งค่า** ได้</span><span class="sxs-lookup"><span data-stu-id="8a52f-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="8a52f-120">ขณะนี้แอปพลิเคชันสนับสนุนบทบาทความปลอดภัยของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="8a52f-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="8a52f-121">ใช้บอท</span><span class="sxs-lookup"><span data-stu-id="8a52f-121">Use the bot</span></span>

<span data-ttu-id="8a52f-122">หลังจากที่ติดตั้งแอปแล้ว ข้อความต้อนรับจะปรากฏขึ้นให้คุณทราบชนิดของการดำเนินการที่บอทสามารถใช้ในนามของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8a52f-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![ข้อความต้อนรับของบอทในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="8a52f-124">เมื่อมีการโต้ตอบกับบอทครั้งแรก คุณอาจจำเป็นต้องลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8a52f-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="8a52f-125">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="8a52f-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="8a52f-126">คุณสามารถขอให้บอทไปที่:</span><span class="sxs-lookup"><span data-stu-id="8a52f-126">You can ask the bot to:</span></span>

- <span data-ttu-id="8a52f-127">แสดงข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้</span><span class="sxs-lookup"><span data-stu-id="8a52f-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![แสดงยอดดุลในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="8a52f-129">แสดงรายละเอียดเพิ่มเติมเกี่ยวกับชนิดการลางานที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="8a52f-129">Show additional details about a specific leave type.</span></span>

   ![แสดงรายละเอียดแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="8a52f-131">เริ่มต้นการร้องขอการลาหยุดสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="8a52f-131">Start a leave request for you.</span></span>

   ![การขอลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="8a52f-133">หลังจากที่คุณเริ่มต้นคำขอการลางาน คุณสามารถปรับวันที่ืที่ถูกต้องภายในบัตรได้</span><span class="sxs-lookup"><span data-stu-id="8a52f-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![แก้ไขคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="8a52f-135">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้เลือก **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8a52f-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="8a52f-136">นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="8a52f-136">You can also select **Save as draft** to come back to it later.</span></span>

![ส่งคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="8a52f-138">จัดการคำขอลางานของคุณใน Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-138">Manage your leave in Teams</span></span>

<span data-ttu-id="8a52f-139">แท็บ **การลาหยุด** จะช่วยให้คุณสามารถดูสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8a52f-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="8a52f-140">ข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้</span><span class="sxs-lookup"><span data-stu-id="8a52f-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="8a52f-141">คำขอการลางานที่กำลังจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="8a52f-141">Upcoming leave requests</span></span>

- <span data-ttu-id="8a52f-142">คำขอลาหยุด</span><span class="sxs-lookup"><span data-stu-id="8a52f-142">Time-off requests</span></span>

- <span data-ttu-id="8a52f-143">ร่างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="8a52f-143">Draft leave requests</span></span>

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="8a52f-145">สร้างคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="8a52f-145">Create a new request</span></span>

1. <span data-ttu-id="8a52f-146">หากต้องการสร้างคำขอลางานใหม่ ให้เลือก **สร้างคำขอ**</span><span class="sxs-lookup"><span data-stu-id="8a52f-146">To create a new leave request, select **New request**.</span></span>

   ![สร้างคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="8a52f-148">ป้อนวันหรือวันที่ที่คุณต้องการลางาน แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8a52f-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![เพิ่มการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="8a52f-150">ถ้าใช้ได้ ให้ป้อนรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="8a52f-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="8a52f-151">ป้อนข้อคิดเห็นและเพิ่มไฟล์แนบใดๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="8a52f-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="8a52f-152">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8a52f-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="8a52f-153">นอกจากนี้คุณยังสามารถพิมพ์ **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="8a52f-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="8a52f-154">จัดการคำขอที่ร่าง</span><span class="sxs-lookup"><span data-stu-id="8a52f-154">Manage draft requests</span></span>

1. <span data-ttu-id="8a52f-155">เลือกแท็บ **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="8a52f-155">Select the **Drafts** tab.</span></span>

   ![แท็บแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="8a52f-157">เลือกดินสอเพื่อแก้ไขคำขอ หรือเลือกถังขยะเพื่อลบคำขอ</span><span class="sxs-lookup"><span data-stu-id="8a52f-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="8a52f-158">ทำการเปลี่ยนแปลงที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8a52f-158">Make any necessary changes.</span></span> <span data-ttu-id="8a52f-159">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8a52f-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="8a52f-160">นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="8a52f-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![แก้ไขแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="8a52f-162">การตอบสนองต่อการแจ้งเตือนของ Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-162">Respond to Teams notifications</span></span>

<span data-ttu-id="8a52f-163">เมื่อคุณหรือผู้ปฏิบัติงานที่คุณเป็นผู้อนุมัติสำหรับส่งกาคำขอการลางาน คุณจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="8a52f-164">คุณสามารถเลือกการแจ้งเตือนที่จะดูได้</span><span class="sxs-lookup"><span data-stu-id="8a52f-164">You can select the notification to view it.</span></span> <span data-ttu-id="8a52f-165">การแจ้งเตือนจะปรากฏในพื้นที่ **การแชท** ด้วย</span><span class="sxs-lookup"><span data-stu-id="8a52f-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="8a52f-166">ถ้าคุณเป็นผู้อนุมัติ คุณสามารถเลือก **อนุมัติ** หรือ **ปฏิเสธ** ในการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="8a52f-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="8a52f-167">นอกจากนี้ คุณยังสามารถระบุข้อความที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="8a52f-167">You can also provide an optional message.</span></span>

![การแจ้งเตือนคำขอการลางานในแอป Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="8a52f-169">ส่งข้อมูลการลางานที่กำลังจะมาถึงให้กับเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8a52f-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="8a52f-170">หลังจากที่คุณติดตั้งแอปพลิเคชันทรัพยากรบุคคลสำหรับ Teams แล้วคุณสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะมาถึงของคุณในทีมหรือการสนทนาได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="8a52f-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="8a52f-171">ในทีมงานหรือการสนทนาใน Teams ให้เลือกปุ่มทรัพยากรบุคคลที่อยู่ด้านล่างของหน้าต่างการสนทนา</span><span class="sxs-lookup"><span data-stu-id="8a52f-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![ปุ่มทรัพยากรบุคคลด้านล่างของหน้าต่างการสนทนา](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="8a52f-173">เลือกคำขอลางานคุณต้องการแชร์</span><span class="sxs-lookup"><span data-stu-id="8a52f-173">Select the leave request you want to share.</span></span> <span data-ttu-id="8a52f-174">ถ้าคุณต้องการใช้การร้องขอการลางานแบบร่างร่วมกัน ให้เลือก **แบบร่าง** ก่อน</span><span class="sxs-lookup"><span data-stu-id="8a52f-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![เลือกการร้องขอการลางานที่กำลังจะเกิดขึ้นที่จะใช้ร่วมกัน](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="8a52f-176">การร้องขอการลางานของคุณจะปรากฏในการสนทนา</span><span class="sxs-lookup"><span data-stu-id="8a52f-176">Your leave request will display in the chat.</span></span>

![ใบร้องขอการลางานของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="8a52f-178">ถ้าคุณใช้การร้องขอแบบร่างร่วมกัน เอกสารจะแสดงเป็นแบบร่าง:</span><span class="sxs-lookup"><span data-stu-id="8a52f-178">If you shared a draft request, it will display as a draft:</span></span>

![ใบร้องขอการลางานแบบร่างของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="8a52f-180">ดูปฏิทินการงานของทีมของคุณ</span><span class="sxs-lookup"><span data-stu-id="8a52f-180">View your team's leave calendar</span></span>

<span data-ttu-id="8a52f-181">ถ้าคุณเป็นผู้จัดการที่มีผู้ใต้บังคับบัญชาโดยตรง คุณสามารถดูการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของทีมของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8a52f-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="8a52f-182">ในแอป Human Resources ใน Teams ให้เลือก **การลาหยุด**</span><span class="sxs-lookup"><span data-stu-id="8a52f-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="8a52f-183">เลือก **ปฏิทินของทีม**</span><span class="sxs-lookup"><span data-stu-id="8a52f-183">Select **Team calendar**.</span></span>

   ![ดูปฏิทินในแอป Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="8a52f-185">ปฏิทินแสดงการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของผู้บังคับบัญชาโดยตรงของคุณ</span><span class="sxs-lookup"><span data-stu-id="8a52f-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![ปฏิทินการลาหยุดในแอป Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="8a52f-187">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="8a52f-187">Troubleshooting</span></span>

<span data-ttu-id="8a52f-188">ถ้าคุณกำลังมีปัญหาในการเข้าสู่ระบบ หรือใช้แอป Human Resources Teams ให้ลองปฏิบัติตามคำแนะนำในการแก้ไขปัญหาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8a52f-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="8a52f-189">ถ้าคุณยังคงมีปัญหาหลังการแก้ไขปัญหา โปรดติดต่อฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="8a52f-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="8a52f-190">สำหรับข้อมูลเพิ่มเติม ดู [รับการสนับสนุน](hr-admin-troubleshooting-support.md)</span><span class="sxs-lookup"><span data-stu-id="8a52f-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="8a52f-191">ไม่สามารถเข้าสู่ระบบแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="8a52f-192">หากคุณไม่สามารถเข้าสู่ระบบแอปได้ อาจเป็นไปได้ว่าบัญชีที่คุณใช้ในการเข้าสู่ระบบ Microsoft Teams ไม่เชื่อมโยงกับเรกคอร์ดพนักงานใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="8a52f-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8a52f-193">โปรดติดต่อผู้ดูแลระบบของคุณ เพื่อให้แน่ใจว่าเรกคอร์ดพนักงานของคุณเชื่อมโยงอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8a52f-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="8a52f-194">เกิดข้อผิดพลาดขณะอนุมัติคำขอการลางานในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="8a52f-195">ถ้าคุณได้รับข้อผิดพลาดขณะที่คุณพยายามอนุมัติคำขอการลางานในแอป Teams ให้ทำตามขั้นตอนการแก้ไขปัญหาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8a52f-195">If you receive an error when you're trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="8a52f-196">ตรวจสอบว่าบัญชีที่คุณใช้ในการเข้าสู่ระบบ Microsoft Teams เป็นเดียวกันกับที่คุณใช้สำหรับการเข้าถึง Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="8a52f-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="8a52f-197">ตรวจสอบว่าคุณเป็นผู้อนุมัติที่ถูกต้องสำหรับคำขอดังกล่าว โดยตรวจสอบการตั้งค่าลำดับงานสำหรับการอนุมัติการลางาน</span><span class="sxs-lookup"><span data-stu-id="8a52f-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="8a52f-198">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลำดับงานคำขอลางาน ดูที่ [สร้างลำดับงานคำขอลางาน](hr-leave-and-absence-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="8a52f-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="8a52f-199">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="8a52f-199">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="8a52f-200">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="8a52f-200">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="8a52f-201">ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="8a52f-201">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="8a52f-202">ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="8a52f-202">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="8a52f-203">อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/)</span><span class="sxs-lookup"><span data-stu-id="8a52f-203">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="8a52f-204">บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง</span><span class="sxs-lookup"><span data-stu-id="8a52f-204">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="8a52f-205">ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8a52f-205">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="8a52f-206">โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="8a52f-206">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="8a52f-207">บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="8a52f-207">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8a52f-208">ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure</span><span class="sxs-lookup"><span data-stu-id="8a52f-208">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="8a52f-209">เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="8a52f-209">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="8a52f-210">อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)</span><span class="sxs-lookup"><span data-stu-id="8a52f-210">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="8a52f-211">เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="8a52f-211">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="8a52f-212">Microsoft Teams, กริดเหตุการณ์ Azure และ Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8a52f-212">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="8a52f-213">เมื่อใช้แอป Dynamics 365 Human Resources ใน Microsoft Teams ข้อมูลลูกค้าบางรายอาจส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่มีการใช้บริการ Human Resources ของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="8a52f-213">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="8a52f-214">Dynamics 365 Human Resources ส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยังกริดเหตุการณ์ Microsoft Azure และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-214">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="8a52f-215">ข้อมูลนี้อาจจัดเก็บไว้ในกริดเหตุการณ์ Microsoft Azure นานถึง 24 ชั่วโมงและจะประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="8a52f-215">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="8a52f-216">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="8a52f-216">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="8a52f-217">ในขณะที่สนทนากับบอทแชทในแอปทรัพยากรบุคคล เนื้อหาการสนทนาอาจจัดเก็บไว้ใน Azure Cosmos DB และส่งผ่านไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-217">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="8a52f-218">ข้อมูลนี้อาจจัดเก็บไว้ใน Azure Cosmos DB ได้สูงสุด24ชั่วโมงและอาจได้รับการประมวลผลภายนอกภูมิภาคทางภูมิศาสตร์ที่มีการปรับใช้บริการทรัพยากรบุคคลของผู้เช่าของคุณจะถูกเข้ารหัสในการส่งต่อและในส่วนที่เหลือและไม่ได้ใช้โดย Microsoft หรือผู้ประมวลผลย่อยสำหรับการฝึกอบรมหรือการให้ปรับปรุงการบริการ</span><span class="sxs-lookup"><span data-stu-id="8a52f-218">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="8a52f-219">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="8a52f-219">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="8a52f-220">เมื่อต้องการจำกัดการเข้าถึงแอปพลิเคชันทรัพยากรบุคคลใน Microsoft Teams สำหรับองค์กรหรือผู้ใช้ภายในองค์กรของคุณ ให้ดูที่ [จัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="8a52f-220">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="8a52f-221">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="8a52f-221">See also</span></span>

[<span data-ttu-id="8a52f-222">ดาวน์โหลดและติดตั้ง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-222">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="8a52f-223">ศูนย์ความช่วยเหลือ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-223">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="8a52f-224">แอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="8a52f-224">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
