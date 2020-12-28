---
title: จัดการคำขอลาหยุดใน Teams
description: หัวข้อนี้จะแสดงวิธีการขอลาหยุดในแอป Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: AnnBe
ms.date: 10/28/2020
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
ms.openlocfilehash: d24c257054578282f1a2eafa050094194a358aa0
ms.sourcegitcommit: 369639cd92e03fe792ed9d61a329d842aafa052f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4420850"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="77e7e-103">จัดการคำขอลาหยุดใน Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="77e7e-104">แอปพลิเคชัน Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้คุณสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดของคุณได้ใน Microsoft Teams ในทันที</span><span class="sxs-lookup"><span data-stu-id="77e7e-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="77e7e-105">คุณสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูลและเริ่มต้นการร้องขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="77e7e-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="77e7e-106">แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="77e7e-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="77e7e-107">นอกจากนี้ คุณยังสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะเกิดขึ้นในทีมและแชทภายนอกแอปพลิเคชันทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-107">You can also send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="77e7e-108">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="77e7e-108">Install the app</span></span>

<span data-ttu-id="77e7e-109">คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="77e7e-110">ใน Microsoft Teams ให้เลือกจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="77e7e-110">In Microsoft Teams, select the ellipses.</span></span>

   ![จุดไข่ปลาของแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="77e7e-112">ค้นหา Dynamics 365 Human Resources และเลือกไทล์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="77e7e-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![ไทล์ HR แอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="77e7e-114">เลือก **เพิ่ม** เพื่อติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="77e7e-114">Select the **Add** button to install the app.</span></span>

   ![ติดตั้งแอปการลาหยุดใน Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="77e7e-116">ถ้าแอปนั้นไม่ได้ลงชื่อเข้าใช้คุณโดยอัตโนมัติ ให้เลือกแท็บ **การตั้งค่า** เพื่อลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="77e7e-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![แท็บการตั้งค่าแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="77e7e-118">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="77e7e-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="77e7e-119">ถ้าคุณมีสิทธิ์เข้าถึงอินสแตนซ์ของทรัพยากรบุคคลมากกว่าหนึ่งอินสแตนซ์ คุณสามารถเลือกสภาพแวดล้อมที่คุณต้องการเชื่อมต่อในแท็บ **การตั้งค่า** ได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="77e7e-120">ขณะนี้แอปพลิเคชันสนับสนุนบทบาทความปลอดภัยของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="77e7e-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="77e7e-121">ใช้บอท</span><span class="sxs-lookup"><span data-stu-id="77e7e-121">Use the bot</span></span>

<span data-ttu-id="77e7e-122">หลังจากที่ติดตั้งแอปแล้ว ข้อความต้อนรับจะปรากฏขึ้นให้คุณทราบชนิดของการดำเนินการที่บอทสามารถใช้ในนามของคุณได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![ข้อความต้อนรับของบอทในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="77e7e-124">เมื่อมีการโต้ตอบกับบอทครั้งแรก คุณอาจจำเป็นต้องลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="77e7e-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="77e7e-125">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="77e7e-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="77e7e-126">คุณสามารถขอให้บอทไปที่:</span><span class="sxs-lookup"><span data-stu-id="77e7e-126">You can ask the bot to:</span></span>

- <span data-ttu-id="77e7e-127">แสดงข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้</span><span class="sxs-lookup"><span data-stu-id="77e7e-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![แสดงยอดดุลในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="77e7e-129">แสดงรายละเอียดเพิ่มเติมเกี่ยวกับชนิดการลางานที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="77e7e-129">Show additional details about a specific leave type.</span></span>

   ![แสดงรายละเอียดแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="77e7e-131">เริ่มต้นการร้องขอการลาหยุดสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="77e7e-131">Start a leave request for you.</span></span>

   ![การขอลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="77e7e-133">หลังจากที่คุณเริ่มต้นคำขอการลางาน คุณสามารถปรับวันที่ืที่ถูกต้องภายในบัตรได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![แก้ไขคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="77e7e-135">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้เลือก **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="77e7e-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="77e7e-136">นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="77e7e-136">You can also select **Save as draft** to come back to it later.</span></span>

![ส่งคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="77e7e-138">จัดการคำขอลางานของคุณใน Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-138">Manage your leave in Teams</span></span>

<span data-ttu-id="77e7e-139">แท็บ **การลาหยุด** จะช่วยให้คุณสามารถดูสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="77e7e-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="77e7e-140">ข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้</span><span class="sxs-lookup"><span data-stu-id="77e7e-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="77e7e-141">คำขอการลางานที่กำลังจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="77e7e-141">Upcoming leave requests</span></span>

- <span data-ttu-id="77e7e-142">คำขอลาหยุด</span><span class="sxs-lookup"><span data-stu-id="77e7e-142">Time-off requests</span></span>

- <span data-ttu-id="77e7e-143">ร่างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="77e7e-143">Draft leave requests</span></span>

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="77e7e-145">สร้างคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="77e7e-145">Create a new request</span></span>

1. <span data-ttu-id="77e7e-146">หากต้องการสร้างคำขอลางานใหม่ ให้เลือก **สร้างคำขอ**</span><span class="sxs-lookup"><span data-stu-id="77e7e-146">To create a new leave request, select **New request**.</span></span>

   ![สร้างคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="77e7e-148">ป้อนวันหรือวันที่ที่คุณต้องการลางาน แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="77e7e-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![เพิ่มการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="77e7e-150">ถ้าใช้ได้ ให้ป้อนรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="77e7e-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="77e7e-151">ป้อนข้อคิดเห็นและเพิ่มไฟล์แนบใดๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="77e7e-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="77e7e-152">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="77e7e-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="77e7e-153">นอกจากนี้คุณยังสามารถพิมพ์ **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="77e7e-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="77e7e-154">จัดการคำขอที่ร่าง</span><span class="sxs-lookup"><span data-stu-id="77e7e-154">Manage draft requests</span></span>

1. <span data-ttu-id="77e7e-155">เลือกแท็บ **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="77e7e-155">Select the **Drafts** tab.</span></span>

   ![แท็บแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="77e7e-157">เลือกดินสอเพื่อแก้ไขคำขอ หรือเลือกถังขยะเพื่อลบคำขอ</span><span class="sxs-lookup"><span data-stu-id="77e7e-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="77e7e-158">ทำการเปลี่ยนแปลงที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="77e7e-158">Make any necessary changes.</span></span> <span data-ttu-id="77e7e-159">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="77e7e-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="77e7e-160">นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="77e7e-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![แก้ไขแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="77e7e-162">การตอบสนองต่อการแจ้งเตือนของ Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-162">Respond to Teams notifications</span></span>

<span data-ttu-id="77e7e-163">เมื่อคุณหรือผู้ปฏิบัติงานที่คุณเป็นผู้อนุมัติสำหรับส่งกาคำขอการลางาน คุณจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="77e7e-164">คุณสามารถเลือกการแจ้งเตือนที่จะดูได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-164">You can select the notification to view it.</span></span> <span data-ttu-id="77e7e-165">การแจ้งเตือนจะปรากฏในพื้นที่ **การแชท** ด้วย</span><span class="sxs-lookup"><span data-stu-id="77e7e-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="77e7e-166">ถ้าคุณเป็นผู้อนุมัติ คุณสามารถเลือก **อนุมัติ** หรือ **ปฏิเสธ** ในการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="77e7e-167">นอกจากนี้ คุณยังสามารถระบุข้อความที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-167">You can also provide an optional message.</span></span>

![การแจ้งเตือนคำขอการลางานในแอป Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="77e7e-169">ส่งข้อมูลการลางานที่กำลังจะมาถึงให้กับเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="77e7e-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="77e7e-170">หลังจากที่คุณติดตั้งแอปพลิเคชันทรัพยากรบุคคลสำหรับ Teams แล้วคุณสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะมาถึงของคุณในทีมหรือการสนทนาได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="77e7e-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="77e7e-171">ในทีมงานหรือการสนทนาใน Teams ให้เลือกปุ่มทรัพยากรบุคคลที่อยู่ด้านล่างของหน้าต่างการสนทนา</span><span class="sxs-lookup"><span data-stu-id="77e7e-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![ปุ่มทรัพยากรบุคคลด้านล่างของหน้าต่างการสนทนา](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="77e7e-173">เลือกคำขอลางานคุณต้องการแชร์</span><span class="sxs-lookup"><span data-stu-id="77e7e-173">Select the leave request you want to share.</span></span> <span data-ttu-id="77e7e-174">ถ้าคุณต้องการใช้การร้องขอการลางานแบบร่างร่วมกัน ให้เลือก **แบบร่าง** ก่อน</span><span class="sxs-lookup"><span data-stu-id="77e7e-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![เลือกการร้องขอการลางานที่กำลังจะเกิดขึ้นที่จะใช้ร่วมกัน](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="77e7e-176">การร้องขอการลางานของคุณจะปรากฏในการสนทนา</span><span class="sxs-lookup"><span data-stu-id="77e7e-176">Your leave request will display in the chat.</span></span>

![ใบร้องขอการลางานของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="77e7e-178">ถ้าคุณใช้การร้องขอแบบร่างร่วมกัน เอกสารจะแสดงเป็นแบบร่าง:</span><span class="sxs-lookup"><span data-stu-id="77e7e-178">If you shared a draft request, it will display as a draft:</span></span>

![ใบร้องขอการลางานแบบร่างของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="77e7e-180">ดูปฏิทินการงานของทีมของคุณ</span><span class="sxs-lookup"><span data-stu-id="77e7e-180">View your team's leave calendar</span></span>

<span data-ttu-id="77e7e-181">ถ้าคุณเป็นผู้จัดการที่มีผู้ใต้บังคับบัญชาโดยตรง คุณสามารถดูการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของทีมของคุณได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="77e7e-182">ในแอป Human Resources ใน Teams ให้เลือก **การลาหยุด**</span><span class="sxs-lookup"><span data-stu-id="77e7e-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="77e7e-183">เลือก **ปฏิทินของทีม**</span><span class="sxs-lookup"><span data-stu-id="77e7e-183">Select **Team calendar**.</span></span>

   ![ดูปฏิทินในแอป Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="77e7e-185">ปฏิทินแสดงการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของผู้บังคับบัญชาโดยตรงของคุณ</span><span class="sxs-lookup"><span data-stu-id="77e7e-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![ปฏิทินการลาหยุดในแอป Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="77e7e-187">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="77e7e-187">Troubleshooting</span></span>

<span data-ttu-id="77e7e-188">ถ้าคุณกำลังมีปัญหาในการเข้าสู่ระบบ หรือใช้แอป Human Resources Teams ให้ลองปฏิบัติตามคำแนะนำในการแก้ไขปัญหาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="77e7e-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="77e7e-189">ถ้าคุณยังคงมีปัญหาหลังการแก้ไขปัญหา โปรดติดต่อฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="77e7e-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="77e7e-190">สำหรับข้อมูลเพิ่มเติม ดู [รับการสนับสนุน](hr-admin-troubleshooting-support.md)</span><span class="sxs-lookup"><span data-stu-id="77e7e-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="77e7e-191">ไม่สามารถเข้าสู่ระบบแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="77e7e-192">หากคุณไม่สามารถเข้าสู่ระบบแอปได้ อาจเป็นไปได้ว่าบัญชีที่คุณใช้ในการเข้าสู่ระบบ Microsoft Teams ไม่เชื่อมโยงกับเรกคอร์ดพนักงานใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="77e7e-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="77e7e-193">โปรดติดต่อผู้ดูแลระบบของคุณ เพื่อให้แน่ใจว่าเรกคอร์ดพนักงานของคุณเชื่อมโยงอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="77e7e-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="77e7e-194">เกิดข้อผิดพลาดขณะอนุมัติคำขอการลางานในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="77e7e-195">ถ้าคุณได้รับข้อผิดพลาดขณะที่คุณพยายามอนุมัติคำขอการลางานในแอป Teams ให้ลองทำตามขั้นตอนการแก้ไขปัญหาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="77e7e-195">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="77e7e-196">ตรวจสอบว่าบัญชีที่คุณใช้ในการเข้าสู่ระบบ Microsoft Teams เป็นเดียวกันกับที่คุณใช้สำหรับการเข้าถึง Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="77e7e-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="77e7e-197">ตรวจสอบว่าคุณเป็นผู้อนุมัติที่ถูกต้องสำหรับคำขอดังกล่าว โดยตรวจสอบการตั้งค่าลำดับงานสำหรับการอนุมัติการลางาน</span><span class="sxs-lookup"><span data-stu-id="77e7e-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="77e7e-198">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลำดับงานคำขอลางาน ดูที่ [สร้างลำดับงานคำขอลางาน](hr-leave-and-absence-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="77e7e-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="77e7e-199">ปัญหาเกี่ยวกับความสามารถในการเข้าถึงที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="77e7e-199">Known accessibility issues</span></span>

<span data-ttu-id="77e7e-200">แอปพลิเคชันทรัพยากรบุคคลใน Teams มีปัญหาความสามารถในการเข้าถึงต่อไปนี้ซึ่งเรากำลังทำการแก้ไขในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="77e7e-200">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="77e7e-201">ออก</span><span class="sxs-lookup"><span data-stu-id="77e7e-201">Issue</span></span> | <span data-ttu-id="77e7e-202">วิธีการแก้ปัญหาหรือคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="77e7e-202">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="77e7e-203">การซูมภาพเป็น 400% บนเดสก์ท็อปจะซ่อนปุ่มการดำเนินการบางปุ่มจากมุมมอง</span><span class="sxs-lookup"><span data-stu-id="77e7e-203">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="77e7e-204">เราขอแนะนำให้ใช้แว่นขยายแทน จนกว่าเราจะสามารถสนับสนุนระดับการย่อ/ขยายนี้ได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-204">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="77e7e-205">บนแท็บ **เวลาหยุดพัก** voiceover ประกาศการดำเนินการปุ่ม ในขณะที่อ่านส่วนหัวสำหรับกริดเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="77e7e-205">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="77e7e-206">ส่วนหัวและองค์ประกอบภายในกริดมีการจัดกลุ่มตามปี และจะสามารถยุบได้</span><span class="sxs-lookup"><span data-stu-id="77e7e-206">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="77e7e-207">Voiceover จะแปลเป็นสินค้าที่สามารถดำเนินการได้ แต่ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="77e7e-207">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="77e7e-208">ถ้าคุณปัดนิ้วในขณะที่ป็อปอัพหรือเมนูเปิดอยู่ voiceover จะข้ามการอ่านเนื้อหาของป็อปอัพหรือเมนู</span><span class="sxs-lookup"><span data-stu-id="77e7e-208">If you swipe while a popup or menu is open, voiceover skips reading the popup or menu contents.</span></span> | <span data-ttu-id="77e7e-209">สำรวจเนื้อหาโดยใช้การสแกนนิ้ว</span><span class="sxs-lookup"><span data-stu-id="77e7e-209">Explore the content using finger scanning.</span></span> |
| <span data-ttu-id="77e7e-210">บนแท็บ **เวลาหยุดพัก** มีท่าทางการรูดพิเศษเมื่อนำทางไปยัง **รหัสเหตุผล** ในคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="77e7e-210">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="77e7e-211">ไม่มีตัวควบคุมที่ซ่อนอยู่ซึ่งการนำทางการรูดกำลังพยายามเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="77e7e-211">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="77e7e-212">บนแท็บ **เวลาหยุดพัก** ถ้าคุณปัดนิ้วในขณะที่ปฏิทินเปิดอยู่ คุณจะไปอยู่ที่ภายนอกตัวควบคุม แทนที่จะอยู่ด้านบนในคำขอใหม่ หรือในขณะที่แก้ไขคำขอ</span><span class="sxs-lookup"><span data-stu-id="77e7e-212">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="77e7e-213">เมื่อคุณเข้าถึง **ไปยังวันนี้** ให้พิจารณาว่าจะเป็นจุดสิ้นสุดของการควบคุมและปัดนิ้วในทิศทางย้อนกลับเพื่อกลับไปด้านบน</span><span class="sxs-lookup"><span data-stu-id="77e7e-213">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="77e7e-214">Voiceover ไม่ได้อ่านป้ายชื่อสำหรับวันที่</span><span class="sxs-lookup"><span data-stu-id="77e7e-214">Voiceover doesn't read the labels for dates.</span></span> | <span data-ttu-id="77e7e-215">วันที่ที่พบเป็นคู่จะเป็น **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** เสมอ</span><span class="sxs-lookup"><span data-stu-id="77e7e-215">The dates encountered in pairs are always **Start date** and **End date**.</span></span> |
| <span data-ttu-id="77e7e-216">บนแท็บ **แชท** โฟกัสจะข้ามไปที่ด้านบนสุด เมื่อคุณป้อนวันที่ในขณะที่ใช้เครื่องมือช่วยเหลือหรือการนำทางของคีย์บอร์ด</span><span class="sxs-lookup"><span data-stu-id="77e7e-216">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="77e7e-217">แตะจนกว่าคุณจะไปถึงพื้นที่อินพุตของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="77e7e-217">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="77e7e-218">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="77e7e-218">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="77e7e-219">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="77e7e-219">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="77e7e-220">ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="77e7e-220">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="77e7e-221">ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="77e7e-221">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="77e7e-222">อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/)</span><span class="sxs-lookup"><span data-stu-id="77e7e-222">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="77e7e-223">บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง</span><span class="sxs-lookup"><span data-stu-id="77e7e-223">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="77e7e-224">ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="77e7e-224">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="77e7e-225">โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="77e7e-225">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="77e7e-226">บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="77e7e-226">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="77e7e-227">ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure</span><span class="sxs-lookup"><span data-stu-id="77e7e-227">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="77e7e-228">เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="77e7e-228">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="77e7e-229">อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)</span><span class="sxs-lookup"><span data-stu-id="77e7e-229">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="77e7e-230">เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="77e7e-230">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="77e7e-231">Microsoft Teams, กริดเหตุการณ์ Azure และ Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="77e7e-231">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="77e7e-232">เมื่อใช้แอป Dynamics 365 Human Resources ใน Microsoft Teams ข้อมูลลูกค้าบางรายอาจส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่มีการใช้บริการ Human Resources ของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="77e7e-232">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="77e7e-233">Dynamics 365 Human Resources ส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยังกริดเหตุการณ์ Microsoft Azure และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-233">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="77e7e-234">ข้อมูลนี้อาจจัดเก็บไว้ในกริดเหตุการณ์ Microsoft Azure นานถึง 24 ชั่วโมงและจะประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="77e7e-234">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="77e7e-235">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="77e7e-235">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="77e7e-236">ในขณะที่สนทนากับบอทแชทในแอปทรัพยากรบุคคล เนื้อหาการสนทนาอาจจัดเก็บไว้ใน Azure Cosmos DB และส่งผ่านไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-236">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="77e7e-237">ข้อมูลนี้อาจจัดเก็บไว้ใน Azure Cosmos DB ได้สูงสุด24ชั่วโมงและอาจได้รับการประมวลผลภายนอกภูมิภาคทางภูมิศาสตร์ที่มีการปรับใช้บริการทรัพยากรบุคคลของผู้เช่าของคุณจะถูกเข้ารหัสในการส่งต่อและในส่วนที่เหลือและไม่ได้ใช้โดย Microsoft หรือผู้ประมวลผลย่อยสำหรับการฝึกอบรมหรือการให้ปรับปรุงการบริการ</span><span class="sxs-lookup"><span data-stu-id="77e7e-237">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="77e7e-238">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="77e7e-238">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="77e7e-239">เมื่อต้องการจำกัดการเข้าถึงแอปพลิเคชันทรัพยากรบุคคลใน Microsoft Teams สำหรับองค์กรหรือผู้ใช้ภายในองค์กรของคุณ ให้ดูที่ [จัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="77e7e-239">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="77e7e-240">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="77e7e-240">See also</span></span>

[<span data-ttu-id="77e7e-241">ดาวน์โหลดและติดตั้ง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-241">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="77e7e-242">ศูนย์ความช่วยเหลือ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-242">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="77e7e-243">แอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="77e7e-243">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
