---
title: จัดการคำขอลาหยุดใน Teams
description: หัวข้อนี้จะแสดงวิธีการขอลาหยุดในแอป Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: tfehr
ms.date: 02/23/2021
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
ms.openlocfilehash: 79bded5a241a8d5de1847adff3e663359ce1b26f
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571739"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="745e2-103">จัดการคำขอลางานใน Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="745e2-104">แอป Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้คุณสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดของคุณได้ใน Microsoft Teams ในทันที</span><span class="sxs-lookup"><span data-stu-id="745e2-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="745e2-105">คุณสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูลและเริ่มต้นการร้องขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="745e2-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="745e2-106">แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="745e2-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="745e2-107">นอกจากนี้ คุณยังสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะเกิดขึ้นใน Teams และแชทภายนอกแอปทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="745e2-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="745e2-108">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="745e2-108">Install the app</span></span>

<span data-ttu-id="745e2-109">คุณสามารถค้นหาแอป Dynamics 365 Human Resources ในร้านค้า Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="745e2-110">ใน Microsoft Teams ให้เลือกจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="745e2-110">In Microsoft Teams, select the ellipses.</span></span>

   ![จุดไข่ปลาของแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="745e2-112">ค้นหา Dynamics 365 Human Resources และเลือกไทล์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="745e2-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![ไทล์ HR แอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="745e2-114">เลือก **เพิ่ม** เพื่อติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="745e2-114">Select the **Add** button to install the app.</span></span>

   ![ติดตั้งแอปการลาหยุดใน Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="745e2-116">ถ้าแอปนั้นไม่ได้ลงชื่อเข้าใช้คุณโดยอัตโนมัติ ให้เลือกแท็บ **การตั้งค่า** เพื่อลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="745e2-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![แท็บการตั้งค่าแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="745e2-118">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="745e2-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="745e2-119">ถ้าคุณมีสิทธิ์เข้าถึงอินสแตนซ์ของทรัพยากรบุคคลมากกว่าหนึ่งอินสแตนซ์ คุณสามารถเลือกสภาพแวดล้อมที่คุณต้องการเชื่อมต่อในแท็บ **การตั้งค่า** ได้</span><span class="sxs-lookup"><span data-stu-id="745e2-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="745e2-120">ขณะนี้แอปพลิเคชันสนับสนุนบทบาทความปลอดภัยของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="745e2-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="745e2-121">ใช้บอท</span><span class="sxs-lookup"><span data-stu-id="745e2-121">Use the bot</span></span>

<span data-ttu-id="745e2-122">หลังจากที่ติดตั้งแอปแล้ว ข้อความต้อนรับจะปรากฏขึ้นให้คุณทราบชนิดของการดำเนินการที่บอทสามารถใช้ในนามของคุณได้</span><span class="sxs-lookup"><span data-stu-id="745e2-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![ข้อความต้อนรับของบอทในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="745e2-124">เมื่อมีการโต้ตอบกับบอทครั้งแรก คุณอาจจำเป็นต้องลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="745e2-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="745e2-125">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="745e2-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="745e2-126">คุณสามารถขอให้บอทไปที่:</span><span class="sxs-lookup"><span data-stu-id="745e2-126">You can ask the bot to:</span></span>

- <span data-ttu-id="745e2-127">เริ่มต้นการร้องขอการลาหยุดสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="745e2-127">Start a leave request for you.</span></span>

  ![เริ่มต้นการร้องขอการลางานในแชท Teams](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="745e2-129">แชทบอทจะเติมข้อมูลการขอลางานให้คุณ</span><span class="sxs-lookup"><span data-stu-id="745e2-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="745e2-130">เลือก **ส่งคำขอการลาหยุด** และแก้ไขรายละเอียดเกี่ยวกับคำขอของคุณ</span><span class="sxs-lookup"><span data-stu-id="745e2-130">Select **Request time off** and edit the details for your request.</span></span>

  ![แก้ไขรายละเอียดคำขอการลาหยุด](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="745e2-132">เมื่อคุณแก้ไขรายละเอียดการลาหยุดของคุณเสร็จแล้ว ให้เลือก **ส่ง** เพื่อส่งคำขอเพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="745e2-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![ส่งคำขอการลาหยุด](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="745e2-134">จัดการคำขอลางานของคุณใน Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-134">Manage your leave in Teams</span></span>

<span data-ttu-id="745e2-135">แท็บ **การลาหยุด** จะช่วยให้คุณสามารถดูสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="745e2-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="745e2-136">ข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้</span><span class="sxs-lookup"><span data-stu-id="745e2-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="745e2-137">คำขอการลางานที่กำลังจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="745e2-137">Upcoming leave requests</span></span>

- <span data-ttu-id="745e2-138">คำขอลาหยุด</span><span class="sxs-lookup"><span data-stu-id="745e2-138">Time-off requests</span></span>

- <span data-ttu-id="745e2-139">ร่างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="745e2-139">Draft leave requests</span></span>

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="745e2-141">สร้างคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="745e2-141">Create a new request</span></span>

1. <span data-ttu-id="745e2-142">หากต้องการสร้างคำขอลางานใหม่ ให้เลือก **สร้างคำขอ**</span><span class="sxs-lookup"><span data-stu-id="745e2-142">To create a new leave request, select **New request**.</span></span>

   ![สร้างคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="745e2-144">ป้อนวันหรือวันที่ที่คุณต้องการลางาน แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="745e2-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![เพิ่มการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="745e2-146">ถ้าใช้ได้ ให้ป้อนรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="745e2-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="745e2-147">ป้อนข้อคิดเห็นและเพิ่มไฟล์แนบใดๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="745e2-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="745e2-148">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="745e2-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="745e2-149">นอกจากนี้คุณยังสามารถพิมพ์ **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="745e2-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="745e2-150">จัดการคำขอที่ร่าง</span><span class="sxs-lookup"><span data-stu-id="745e2-150">Manage draft requests</span></span>

1. <span data-ttu-id="745e2-151">เลือกแท็บ **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="745e2-151">Select the **Drafts** tab.</span></span>

   ![แท็บแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="745e2-153">เลือกดินสอเพื่อแก้ไขคำขอ หรือเลือกถังขยะเพื่อลบคำขอ</span><span class="sxs-lookup"><span data-stu-id="745e2-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="745e2-154">ทำการเปลี่ยนแปลงที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="745e2-154">Make any necessary changes.</span></span> <span data-ttu-id="745e2-155">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="745e2-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="745e2-156">นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="745e2-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![แก้ไขแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="745e2-158">การตอบสนองต่อการแจ้งเตือนของ Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-158">Respond to Teams notifications</span></span>

<span data-ttu-id="745e2-159">เมื่อคุณหรือผู้ปฏิบัติงานที่คุณเป็นผู้อนุมัติสำหรับส่งกาคำขอการลางาน คุณจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="745e2-160">คุณสามารถเลือกการแจ้งเตือนที่จะดูได้</span><span class="sxs-lookup"><span data-stu-id="745e2-160">You can select the notification to view it.</span></span> <span data-ttu-id="745e2-161">การแจ้งเตือนจะปรากฏในพื้นที่ **การแชท** ด้วย</span><span class="sxs-lookup"><span data-stu-id="745e2-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="745e2-162">ถ้าคุณเป็นผู้อนุมัติ คุณสามารถเลือก **อนุมัติ** หรือ **ปฏิเสธ** ในการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="745e2-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="745e2-163">นอกจากนี้ คุณยังสามารถระบุข้อความที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="745e2-163">You can also provide an optional message.</span></span>

![การแจ้งเตือนคำขอการลางานในแอป Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="745e2-165">ส่งข้อมูลการลางานที่กำลังจะมาถึงให้กับเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="745e2-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="745e2-166">หลังจากที่คุณติดตั้งแอปพลิเคชันทรัพยากรบุคคลสำหรับ Teams แล้วคุณสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะมาถึงของคุณในทีมหรือการสนทนาได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="745e2-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="745e2-167">ในทีมงานหรือการสนทนาใน Teams ให้เลือกปุ่มทรัพยากรบุคคลที่อยู่ด้านล่างของหน้าต่างการสนทนา</span><span class="sxs-lookup"><span data-stu-id="745e2-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![ปุ่มทรัพยากรบุคคลด้านล่างของหน้าต่างการสนทนา](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="745e2-169">เลือกคำขอลางานคุณต้องการแชร์</span><span class="sxs-lookup"><span data-stu-id="745e2-169">Select the leave request you want to share.</span></span> <span data-ttu-id="745e2-170">ถ้าคุณต้องการใช้การร้องขอการลางานแบบร่างร่วมกัน ให้เลือก **แบบร่าง** ก่อน</span><span class="sxs-lookup"><span data-stu-id="745e2-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![เลือกการร้องขอการลางานที่กำลังจะเกิดขึ้นที่จะใช้ร่วมกัน](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="745e2-172">การร้องขอการลางานของคุณจะปรากฏในการสนทนา</span><span class="sxs-lookup"><span data-stu-id="745e2-172">Your leave request will display in the chat.</span></span>

![ใบร้องขอการลางานของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="745e2-174">ถ้าคุณใช้การร้องขอแบบร่างร่วมกัน เอกสารจะแสดงเป็นแบบร่าง:</span><span class="sxs-lookup"><span data-stu-id="745e2-174">If you shared a draft request, it will display as a draft:</span></span>

![ใบร้องขอการลางานแบบร่างของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="745e2-176">ดูปฏิทินการงานของทีมของคุณ</span><span class="sxs-lookup"><span data-stu-id="745e2-176">View your team's leave calendar</span></span>

<span data-ttu-id="745e2-177">ถ้าคุณเป็นผู้จัดการที่มีผู้ใต้บังคับบัญชาโดยตรง คุณสามารถดูการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของทีมของคุณได้</span><span class="sxs-lookup"><span data-stu-id="745e2-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="745e2-178">ในแอป Human Resources ใน Teams ให้เลือก **การลาหยุด**</span><span class="sxs-lookup"><span data-stu-id="745e2-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="745e2-179">เลือก **ปฏิทินของทีม**</span><span class="sxs-lookup"><span data-stu-id="745e2-179">Select **Team calendar**.</span></span> <span data-ttu-id="745e2-180">ปฏิทินแสดงการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของผู้บังคับบัญชาโดยตรงของคุณ</span><span class="sxs-lookup"><span data-stu-id="745e2-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![ดูปฏิทินในแอป Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="745e2-182">หากคุณไม่เห็นปฏิทินของ Teams โปรดขอให้ผู้ดูแลระบบของคุณเปิดใช้งานปฏิทินนั้น</span><span class="sxs-lookup"><span data-stu-id="745e2-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="745e2-183">สำหรับข้อมูลเพิ่มเติม ดูที่ [ติดตั้งและตั้งค่า](hr-admin-teams-leave-app.md#install-and-setup)</span><span class="sxs-lookup"><span data-stu-id="745e2-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="745e2-184">ภาษาที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="745e2-184">Supported languages</span></span>

<span data-ttu-id="745e2-185">แอป Dynamics 365 Human Resources ใน Teams สนับสนุนภาษาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="745e2-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="745e2-186">รหัสภาษา</span><span class="sxs-lookup"><span data-stu-id="745e2-186">Locale ID</span></span> | <span data-ttu-id="745e2-187">ภาษา</span><span class="sxs-lookup"><span data-stu-id="745e2-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="745e2-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="745e2-188">de-DE</span></span> | <span data-ttu-id="745e2-189">ภาษาเยอรมัน (เยอรมนี)</span><span class="sxs-lookup"><span data-stu-id="745e2-189">German (Germany)</span></span> |
| <span data-ttu-id="745e2-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="745e2-190">es-ES</span></span> | <span data-ttu-id="745e2-191">ภาษาสเปน (สเปน)</span><span class="sxs-lookup"><span data-stu-id="745e2-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="745e2-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="745e2-192">es-MX</span></span> | <span data-ttu-id="745e2-193">ภาษาสเปน (เม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="745e2-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="745e2-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="745e2-194">fr-CA</span></span> | <span data-ttu-id="745e2-195">ภาษาฝรั่งเศส (แคนาดา)</span><span class="sxs-lookup"><span data-stu-id="745e2-195">French (Canada)</span></span> |
| <span data-ttu-id="745e2-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="745e2-196">fr-FR</span></span> | <span data-ttu-id="745e2-197">ภาษาฝรั่งเศส (ฝรั่งเศส)</span><span class="sxs-lookup"><span data-stu-id="745e2-197">French (France)</span></span> |
| <span data-ttu-id="745e2-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="745e2-198">it-IT</span></span> | <span data-ttu-id="745e2-199">ภาษาอิตาลี (อิตาลี)</span><span class="sxs-lookup"><span data-stu-id="745e2-199">Italian (Italy)</span></span> |
| <span data-ttu-id="745e2-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="745e2-200">nl-NL</span></span> | <span data-ttu-id="745e2-201">ภาษาดัตช์ (เนเธอร์แลนด์)</span><span class="sxs-lookup"><span data-stu-id="745e2-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="745e2-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="745e2-202">pt-BR</span></span> | <span data-ttu-id="745e2-203">ภาษาโปรตุเกส (บราซิล)</span><span class="sxs-lookup"><span data-stu-id="745e2-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="745e2-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="745e2-204">tr-TR</span></span> | <span data-ttu-id="745e2-205">ภาษาตุรกี (ตุรกี)</span><span class="sxs-lookup"><span data-stu-id="745e2-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="745e2-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="745e2-206">zh-CN</span></span> | <span data-ttu-id="745e2-207">จีน (ประยุกต์)</span><span class="sxs-lookup"><span data-stu-id="745e2-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="745e2-208">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="745e2-208">Troubleshooting</span></span>

<span data-ttu-id="745e2-209">หากคุณกำลังมีปัญหาในการเข้าสู่ระบบ หรือการใช้แอป Dynamics 365 Human Resources Teams ให้ลองปฏิบัติตามคำแนะนำในการแก้ไขปัญหาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="745e2-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="745e2-210">ถ้าคุณยังคงมีปัญหาหลังการแก้ไขปัญหา โปรดติดต่อฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="745e2-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="745e2-211">สำหรับข้อมูลเพิ่มเติม ดู [รับการสนับสนุน](hr-admin-troubleshooting-support.md)</span><span class="sxs-lookup"><span data-stu-id="745e2-211">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="745e2-212">ไม่สามารถเข้าสู่ระบบแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="745e2-213">หากคุณไม่สามารถเข้าสู่ระบบแอปได้ อาจเป็นไปได้ว่าบัญชีที่คุณใช้ในการเข้าสู่ระบบ Microsoft Teams ไม่เชื่อมโยงกับเรกคอร์ดพนักงานใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="745e2-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="745e2-214">โปรดติดต่อผู้ดูแลระบบของคุณ เพื่อให้แน่ใจว่าเรกคอร์ดพนักงานของคุณเชื่อมโยงอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="745e2-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="745e2-215">การแปลแสดงไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="745e2-215">Translations don't display correctly</span></span>

<span data-ttu-id="745e2-216">หากการแปลไม่แสดงตามที่คาดไว้ ให้ตรวจสอบให้แน่ใจว่าภาษาที่คุณเลือกใน Teams ตรงกับภาษาที่เลือกไว้ใน ทรัพยากรบุคคล **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="745e2-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="745e2-217">ใน Teams ให้ดู **ภาษาของแอป** ใน **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="745e2-217">In Teams, look at **App language** in **Settings**.</span></span>

![การตั้งค่า Teams](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="745e2-219">ในทรัพยากรบุคคล ให้เลือก **การตั้งค่า** แล้วเลือก **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="745e2-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="745e2-220">ตรวจสอบว่าฟิลด์ **ภาษา** ตรงกับฟิลด์ **ภาษาของแอป** ใน Teams หรือไม่</span><span class="sxs-lookup"><span data-stu-id="745e2-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![ตัวเลือกผู้ใช้ทรัพยากรบุคคล](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="745e2-222">หากคุณยังคงพบปัญหาการแปล โปรดแจ้งให้เราทราบ</span><span class="sxs-lookup"><span data-stu-id="745e2-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="745e2-223">สำหรับข้อมูล ให้ดูที่ [การขอความช่วยเหลือสำหรับแอป Finance and Operations หรือ Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json)</span><span class="sxs-lookup"><span data-stu-id="745e2-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="745e2-224">เกิดข้อผิดพลาดขณะอนุมัติคำขอการลางานในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="745e2-225">ถ้าคุณได้รับข้อผิดพลาดขณะที่คุณพยายามอนุมัติคำขอการลางานในแอป Teams ให้ลองทำตามขั้นตอนการแก้ไขปัญหาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="745e2-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="745e2-226">ตรวจสอบว่าบัญชีที่คุณใช้ในการเข้าสู่ระบบ Microsoft Teams เป็นเดียวกันกับที่คุณใช้สำหรับการเข้าถึง Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="745e2-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="745e2-227">ตรวจสอบว่าคุณเป็นผู้อนุมัติที่ถูกต้องสำหรับคำขอดังกล่าว โดยตรวจสอบการตั้งค่าลำดับงานสำหรับการอนุมัติการลางาน</span><span class="sxs-lookup"><span data-stu-id="745e2-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="745e2-228">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลำดับงานคำขอลางาน ดูที่ [สร้างลำดับงานคำขอลางาน](hr-leave-and-absence-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="745e2-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="745e2-229">ปัญหาเกี่ยวกับความสามารถในการเข้าถึงที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="745e2-229">Known accessibility issues</span></span>

<span data-ttu-id="745e2-230">แอปพลิเคชันทรัพยากรบุคคลใน Teams มีปัญหาความสามารถในการเข้าถึงต่อไปนี้ซึ่งเรากำลังทำการแก้ไขในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="745e2-230">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="745e2-231">ออก</span><span class="sxs-lookup"><span data-stu-id="745e2-231">Issue</span></span> | <span data-ttu-id="745e2-232">วิธีการแก้ปัญหาหรือคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="745e2-232">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="745e2-233">การซูมภาพเป็น 400% บนเดสก์ท็อปจะซ่อนปุ่มการดำเนินการบางปุ่มจากมุมมอง</span><span class="sxs-lookup"><span data-stu-id="745e2-233">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="745e2-234">เราขอแนะนำให้ใช้แว่นขยายแทน จนกว่าเราจะสามารถสนับสนุนระดับการย่อ/ขยายนี้ได้</span><span class="sxs-lookup"><span data-stu-id="745e2-234">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="745e2-235">บนแท็บ **เวลาหยุดพัก** voiceover ประกาศการดำเนินการปุ่ม ในขณะที่อ่านส่วนหัวสำหรับกริดเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="745e2-235">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="745e2-236">ส่วนหัวและองค์ประกอบภายในกริดมีการจัดกลุ่มตามปี และจะสามารถยุบได้</span><span class="sxs-lookup"><span data-stu-id="745e2-236">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="745e2-237">Voiceover จะแปลเป็นสินค้าที่สามารถดำเนินการได้ แต่ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="745e2-237">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="745e2-238">บนแท็บ **เวลาหยุดพัก** มีท่าทางการรูดพิเศษเมื่อนำทางไปยัง **รหัสเหตุผล** ในคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="745e2-238">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="745e2-239">ไม่มีตัวควบคุมที่ซ่อนอยู่ซึ่งการนำทางการรูดกำลังพยายามเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="745e2-239">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="745e2-240">บนแท็บ **เวลาหยุดพัก** ถ้าคุณปัดนิ้วในขณะที่ปฏิทินเปิดอยู่ คุณจะไปอยู่ที่ภายนอกตัวควบคุม แทนที่จะอยู่ด้านบนในคำขอใหม่ หรือในขณะที่แก้ไขคำขอ</span><span class="sxs-lookup"><span data-stu-id="745e2-240">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="745e2-241">เมื่อคุณเข้าถึง **ไปยังวันนี้** ให้พิจารณาว่าจะเป็นจุดสิ้นสุดของการควบคุมและปัดนิ้วในทิศทางย้อนกลับเพื่อกลับไปด้านบน</span><span class="sxs-lookup"><span data-stu-id="745e2-241">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="745e2-242">บนแท็บ **แชท** โฟกัสจะข้ามไปที่ด้านบนสุด เมื่อคุณป้อนวันที่ในขณะที่ใช้เครื่องมือช่วยเหลือหรือการนำทางของคีย์บอร์ด</span><span class="sxs-lookup"><span data-stu-id="745e2-242">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="745e2-243">แตะจนกว่าคุณจะไปถึงพื้นที่อินพุตของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="745e2-243">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="745e2-244">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="745e2-244">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="745e2-245">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="745e2-245">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="745e2-246">ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="745e2-246">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="745e2-247">ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="745e2-247">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="745e2-248">อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/)</span><span class="sxs-lookup"><span data-stu-id="745e2-248">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="745e2-249">บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง</span><span class="sxs-lookup"><span data-stu-id="745e2-249">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="745e2-250">ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="745e2-250">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="745e2-251">โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="745e2-251">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="745e2-252">บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="745e2-252">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="745e2-253">ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure</span><span class="sxs-lookup"><span data-stu-id="745e2-253">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="745e2-254">เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="745e2-254">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="745e2-255">อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)</span><span class="sxs-lookup"><span data-stu-id="745e2-255">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="745e2-256">เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="745e2-256">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="745e2-257">Microsoft Teams, กริดเหตุการณ์ Azure และ Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="745e2-257">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="745e2-258">เมื่อใช้แอป Dynamics 365 Human Resources ใน Microsoft Teams ข้อมูลลูกค้าบางรายอาจส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่มีการใช้บริการ Human Resources ของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="745e2-258">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="745e2-259">Dynamics 365 Human Resources ส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยังกริดเหตุการณ์ Microsoft Azure และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-259">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="745e2-260">ข้อมูลนี้อาจจัดเก็บไว้ในกริดเหตุการณ์ Microsoft Azure นานถึง 24 ชั่วโมงและจะประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="745e2-260">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="745e2-261">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="745e2-261">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="745e2-262">ในขณะที่สนทนากับบอทแชทในแอปทรัพยากรบุคคล เนื้อหาการสนทนาอาจจัดเก็บไว้ใน Azure Cosmos DB และส่งผ่านไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-262">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="745e2-263">ข้อมูลนี้อาจจัดเก็บไว้ใน Azure Cosmos DB ได้สูงสุด24ชั่วโมงและอาจได้รับการประมวลผลภายนอกภูมิภาคทางภูมิศาสตร์ที่มีการปรับใช้บริการทรัพยากรบุคคลของผู้เช่าของคุณจะถูกเข้ารหัสในการส่งต่อและในส่วนที่เหลือและไม่ได้ใช้โดย Microsoft หรือผู้ประมวลผลย่อยสำหรับการฝึกอบรมหรือการให้ปรับปรุงการบริการ</span><span class="sxs-lookup"><span data-stu-id="745e2-263">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="745e2-264">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="745e2-264">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="745e2-265">เมื่อต้องการจำกัดการเข้าถึงแอปพลิเคชันทรัพยากรบุคคลใน Microsoft Teams สำหรับองค์กรหรือผู้ใช้ภายในองค์กรของคุณ ให้ดูที่ [จัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="745e2-265">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="745e2-266">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="745e2-266">See also</span></span>

[<span data-ttu-id="745e2-267">ดาวน์โหลดและติดตั้ง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-267">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="745e2-268">ศูนย์ความช่วยเหลือ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-268">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="745e2-269">แอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="745e2-269">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]