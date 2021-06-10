---
title: จัดการคำขอลาหยุดใน Teams
description: หัวข้อนี้จะแสดงวิธีการขอลาหยุดในแอป Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097270"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="0e415-103">จัดการคำขอลางานใน Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0e415-104">แอป Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้คุณสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดของคุณได้ใน Microsoft Teams ในทันที</span><span class="sxs-lookup"><span data-stu-id="0e415-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="0e415-105">คุณสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูลและเริ่มต้นการร้องขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="0e415-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="0e415-106">แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="0e415-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="0e415-107">นอกจากนี้ คุณยังสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะเกิดขึ้นใน Teams และแชทภายนอกแอปทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="0e415-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="0e415-108">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="0e415-108">Install the app</span></span>

<span data-ttu-id="0e415-109">คุณสามารถค้นหาแอป Dynamics 365 Human Resources ในร้านค้า Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="0e415-110">ใน Microsoft Teams ให้นําทางไปยังรายการแอป</span><span class="sxs-lookup"><span data-stu-id="0e415-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="0e415-111">ค้นหา Dynamics 365 Human Resources และเลือกไทล์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="0e415-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="0e415-112">เลือก **เพิ่ม** เพื่อติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="0e415-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="0e415-113">ถ้าแอปนั้นไม่ได้ลงชื่อเข้าใช้คุณโดยอัตโนมัติ ให้เลือกแท็บ **การตั้งค่า** เพื่อลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="0e415-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="0e415-114">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="0e415-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="0e415-115">ถ้าคุณมีสิทธิ์เข้าถึงอินสแตนซ์ของทรัพยากรบุคคลมากกว่าหนึ่งอินสแตนซ์ คุณสามารถเลือกสภาพแวดล้อมที่คุณต้องการเชื่อมต่อในแท็บ **การตั้งค่า** ได้</span><span class="sxs-lookup"><span data-stu-id="0e415-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="0e415-116">ขณะนี้แอปพลิเคชันสนับสนุนบทบาทความปลอดภัยของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="0e415-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="0e415-117">ใช้บอท</span><span class="sxs-lookup"><span data-stu-id="0e415-117">Use the bot</span></span>

<span data-ttu-id="0e415-118">หลังจากที่ติดตั้งแอปแล้ว ข้อความต้อนรับจะปรากฏขึ้นให้คุณทราบชนิดของการดำเนินการที่บอทสามารถใช้ในนามของคุณได้</span><span class="sxs-lookup"><span data-stu-id="0e415-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="0e415-119">เมื่อมีการโต้ตอบกับบอทครั้งแรก คุณอาจจำเป็นต้องลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="0e415-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="0e415-120">ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัป</span><span class="sxs-lookup"><span data-stu-id="0e415-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="0e415-121">คุณสามารถขอให้บอทไปที่:</span><span class="sxs-lookup"><span data-stu-id="0e415-121">You can ask the bot to:</span></span>

- <span data-ttu-id="0e415-122">ดูยอดดุลการลางานปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e415-122">View your current leave balances.</span></span> <span data-ttu-id="0e415-123">ตัวอย่างเช่น ส่งข้อความที่ระบุว่า "ดูยอดดุลการลางาน"</span><span class="sxs-lookup"><span data-stu-id="0e415-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="0e415-124">เริ่มต้นการร้องขอการลาหยุดสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="0e415-124">Start a leave request for you.</span></span> <span data-ttu-id="0e415-125">ตัวอย่างเช่น ส่งข้อความ "ลางาน" หรือ "ฉันต้องการหยุดพักร้อนในวันพฤหัสบดีและวันศุกร์" ถัดไป เพื่อเจาะจงมากขึ้นหากต้องการลางานในวันหยุด</span><span class="sxs-lookup"><span data-stu-id="0e415-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![เริ่มต้นการร้องขอการลางานในแชท Teams](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="0e415-127">แชทบอทจะเติมข้อมูลการขอลางานให้คุณ</span><span class="sxs-lookup"><span data-stu-id="0e415-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="0e415-128">เลือก **ส่งคำขอการลาหยุด** และแก้ไขรายละเอียดเกี่ยวกับคำขอของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e415-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="0e415-129">ถ้าคุณต้องการส่งใบขอลางานชนิดต่างๆ ในวันเดียวกัน ให้เลือกตัวเลือก **แบ่งวันด้วย** จากเมนู **ตัวเลือกเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="0e415-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="0e415-130">ถ้าคุณเลือกการลางานของครึ่งวัน เมื่อหน่วยการลางานของการร้องขออยู่ในหน่วยวัน คุณสามารถระบุได้ว่าคุณต้องการร้องขอเวลาปิดครึ่งวันแรกหรือครึ่งวันที่สอง โดยการเลือกตัวเลือก **ข้อนิยามครึ่งวัน** จากเมนู **ตัวเลือกเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="0e415-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![การนิยามครึ่งวัน](./media/HalfDayDefinitions.png)

- <span data-ttu-id="0e415-132">เมื่อคุณแก้ไขรายละเอียดการลาหยุดของคุณเสร็จแล้ว ให้เลือก **ส่ง** เพื่อส่งคำขอเพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="0e415-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![ส่งคำขอการลาหยุด](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="0e415-134">จัดการคำขอลางานของคุณใน Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-134">Manage your leave in Teams</span></span>

<span data-ttu-id="0e415-135">แท็บ **การลาหยุด** จะช่วยให้คุณสามารถดูสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0e415-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="0e415-136">ข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้</span><span class="sxs-lookup"><span data-stu-id="0e415-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="0e415-137">คำขอการลางานที่กำลังจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="0e415-137">Upcoming leave requests</span></span>

- <span data-ttu-id="0e415-138">คำขอลาหยุด</span><span class="sxs-lookup"><span data-stu-id="0e415-138">Time-off requests</span></span>

- <span data-ttu-id="0e415-139">ร่างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="0e415-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="0e415-140">สร้างคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="0e415-140">Create a new request</span></span>

1. <span data-ttu-id="0e415-141">หากต้องการสร้างคำขอลางานใหม่ ให้เลือก **สร้างคำขอ**</span><span class="sxs-lookup"><span data-stu-id="0e415-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="0e415-142">ป้อนวันหรือวันที่ที่คุณต้องการลางาน แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="0e415-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![เพิ่มการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/TimeOffHours.png)

3. <span data-ttu-id="0e415-144">ถ้าใช้ได้ ให้ป้อนรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="0e415-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="0e415-145">ป้อนข้อคิดเห็นและเพิ่มไฟล์แนบใดๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="0e415-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="0e415-146">ให้เลือกตัวเลือก **แบ่งวันด้วย** จากเมนู **ตัวเลือกเพิ่มเติม** ถ้าคุณต้องการส่งใบขอลางานชนิดต่างๆ ในวันเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0e415-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="0e415-147">เลือกตัวเลือก **คำนิยามครึ่งวัน** เพื่อระบุว่าคุณต้องการร้องขอการหยุดครึ่งวันแรกหรือครึ่งวันที่สอง</span><span class="sxs-lookup"><span data-stu-id="0e415-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="0e415-148">ตัวเลือกนี้จะพร้อมใช้งานเมื่อหน่วยการลางานอยู่ในหน่วยวัน และจำนวนที่ร้องขอคือ 0.5 วัน</span><span class="sxs-lookup"><span data-stu-id="0e415-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="0e415-149">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้ป้อน **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="0e415-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="0e415-150">นอกจากนี้คุณยังสามารถป้อน **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="0e415-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="0e415-151">จัดการคำขอที่ร่าง</span><span class="sxs-lookup"><span data-stu-id="0e415-151">Manage draft requests</span></span>

1. <span data-ttu-id="0e415-152">เลือกแท็บ **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="0e415-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="0e415-153">เลือกดินสอเพื่อแก้ไขคำขอ หรือเลือกถังขยะเพื่อลบคำขอ</span><span class="sxs-lookup"><span data-stu-id="0e415-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="0e415-154">ทำการเปลี่ยนแปลงที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="0e415-154">Make any necessary changes.</span></span> <span data-ttu-id="0e415-155">เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="0e415-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="0e415-156">นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="0e415-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="0e415-157">การตอบสนองต่อการแจ้งเตือนของ Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-157">Respond to Teams notifications</span></span>

<span data-ttu-id="0e415-158">เมื่อคุณหรือผู้ปฏิบัติงานที่คุณเป็นผู้อนุมัติสำหรับส่งกาคำขอการลางาน คุณจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="0e415-159">คุณสามารถเลือกการแจ้งเตือนที่จะดูได้</span><span class="sxs-lookup"><span data-stu-id="0e415-159">You can select the notification to view it.</span></span> <span data-ttu-id="0e415-160">การแจ้งเตือนจะปรากฏในพื้นที่ **การแชท** ด้วย</span><span class="sxs-lookup"><span data-stu-id="0e415-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="0e415-161">ถ้าคุณเป็นผู้อนุมัติ คุณสามารถเลือก **อนุมัติ** หรือ **ปฏิเสธ** ในการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="0e415-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="0e415-162">นอกจากนี้ คุณยังสามารถระบุข้อความที่เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="0e415-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="0e415-163">ส่งข้อมูลการลางานที่กำลังจะมาถึงให้กับเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e415-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="0e415-164">หลังจากที่คุณติดตั้งแอปพลิเคชันทรัพยากรบุคคลสำหรับ Teams แล้วคุณสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะมาถึงของคุณในทีมหรือการสนทนาได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="0e415-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="0e415-165">ในทีมงานหรือการสนทนาใน Teams ให้เลือกปุ่มทรัพยากรบุคคลที่อยู่ด้านล่างของหน้าต่างการสนทนา</span><span class="sxs-lookup"><span data-stu-id="0e415-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![ปุ่มทรัพยากรบุคคลด้านล่างของหน้าต่างการสนทนา](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="0e415-167">เลือกคำขอลางานคุณต้องการแชร์</span><span class="sxs-lookup"><span data-stu-id="0e415-167">Select the leave request you want to share.</span></span> <span data-ttu-id="0e415-168">ถ้าคุณต้องการใช้การร้องขอการลางานแบบร่างร่วมกัน ให้เลือก **แบบร่าง** ก่อน</span><span class="sxs-lookup"><span data-stu-id="0e415-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="0e415-169">การร้องขอการลางานของคุณจะปรากฏในการสนทนา</span><span class="sxs-lookup"><span data-stu-id="0e415-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="0e415-170">ถ้าคุณใช้การร้องขอแบบร่างร่วมกัน เอกสารจะแสดงเป็นแบบร่าง:</span><span class="sxs-lookup"><span data-stu-id="0e415-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="0e415-171">ดูปฏิทินการงานของทีมของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e415-171">View your team's leave calendar</span></span>

<span data-ttu-id="0e415-172">ถ้าคุณเป็นผู้จัดการที่มีผู้ใต้บังคับบัญชาโดยตรง คุณสามารถดูการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของทีมของคุณได้</span><span class="sxs-lookup"><span data-stu-id="0e415-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="0e415-173">ในแอป Human Resources ใน Teams ให้เลือก **การลาหยุด**</span><span class="sxs-lookup"><span data-stu-id="0e415-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="0e415-174">เลือก **ปฏิทินของทีม**</span><span class="sxs-lookup"><span data-stu-id="0e415-174">Select **Team calendar**.</span></span> <span data-ttu-id="0e415-175">ปฏิทินแสดงการลาหยุดที่ได้รับอนุมัติและที่ค้างอยู่ของผู้บังคับบัญชาโดยตรงของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e415-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0e415-176">หากคุณไม่เห็นปฏิทินของ Teams โปรดขอให้ผู้ดูแลระบบของคุณเปิดใช้งานปฏิทินนั้น</span><span class="sxs-lookup"><span data-stu-id="0e415-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="0e415-177">สำหรับข้อมูลเพิ่มเติม ดูที่ [ติดตั้งและตั้งค่า](hr-admin-teams-leave-app.md#install-and-setup)</span><span class="sxs-lookup"><span data-stu-id="0e415-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="0e415-178">ภาษาที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="0e415-178">Supported languages</span></span>

<span data-ttu-id="0e415-179">แอป Dynamics 365 Human Resources ใน Teams สนับสนุนภาษาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0e415-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="0e415-180">รหัสภาษา</span><span class="sxs-lookup"><span data-stu-id="0e415-180">Locale ID</span></span> | <span data-ttu-id="0e415-181">ภาษา</span><span class="sxs-lookup"><span data-stu-id="0e415-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="0e415-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="0e415-182">de-DE</span></span> | <span data-ttu-id="0e415-183">ภาษาเยอรมัน (เยอรมนี)</span><span class="sxs-lookup"><span data-stu-id="0e415-183">German (Germany)</span></span> |
| <span data-ttu-id="0e415-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="0e415-184">es-ES</span></span> | <span data-ttu-id="0e415-185">ภาษาสเปน (สเปน)</span><span class="sxs-lookup"><span data-stu-id="0e415-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="0e415-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="0e415-186">es-MX</span></span> | <span data-ttu-id="0e415-187">ภาษาสเปน (เม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="0e415-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="0e415-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="0e415-188">fr-CA</span></span> | <span data-ttu-id="0e415-189">ภาษาฝรั่งเศส (แคนาดา)</span><span class="sxs-lookup"><span data-stu-id="0e415-189">French (Canada)</span></span> |
| <span data-ttu-id="0e415-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="0e415-190">fr-FR</span></span> | <span data-ttu-id="0e415-191">ภาษาฝรั่งเศส (ฝรั่งเศส)</span><span class="sxs-lookup"><span data-stu-id="0e415-191">French (France)</span></span> |
| <span data-ttu-id="0e415-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="0e415-192">it-IT</span></span> | <span data-ttu-id="0e415-193">ภาษาอิตาลี (อิตาลี)</span><span class="sxs-lookup"><span data-stu-id="0e415-193">Italian (Italy)</span></span> |
| <span data-ttu-id="0e415-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="0e415-194">nl-NL</span></span> | <span data-ttu-id="0e415-195">ภาษาดัตช์ (เนเธอร์แลนด์)</span><span class="sxs-lookup"><span data-stu-id="0e415-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="0e415-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="0e415-196">pt-BR</span></span> | <span data-ttu-id="0e415-197">ภาษาโปรตุเกส (บราซิล)</span><span class="sxs-lookup"><span data-stu-id="0e415-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="0e415-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="0e415-198">tr-TR</span></span> | <span data-ttu-id="0e415-199">ภาษาตุรกี (ตุรกี)</span><span class="sxs-lookup"><span data-stu-id="0e415-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="0e415-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="0e415-200">zh-CN</span></span> | <span data-ttu-id="0e415-201">จีน (ประยุกต์)</span><span class="sxs-lookup"><span data-stu-id="0e415-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="0e415-202">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="0e415-202">Troubleshooting</span></span>

<span data-ttu-id="0e415-203">หากคุณกำลังมีปัญหาในการเข้าสู่ระบบ หรือการใช้แอป Dynamics 365 Human Resources Teams ให้ลองปฏิบัติตามคำแนะนำในการแก้ไขปัญหาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="0e415-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="0e415-204">ถ้าคุณยังคงมีปัญหาหลังการแก้ไขปัญหา โปรดติดต่อฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="0e415-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="0e415-205">สำหรับข้อมูลเพิ่มเติม ดู [รับการสนับสนุน](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)</span><span class="sxs-lookup"><span data-stu-id="0e415-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="0e415-206">ไม่สามารถเข้าสู่ระบบแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="0e415-207">หากคุณไม่สามารถเข้าสู่ระบบแอปได้ อาจเป็นไปได้ว่าบัญชีที่คุณใช้ในการเข้าสู่ระบบ Microsoft Teams ไม่เชื่อมโยงกับเรกคอร์ดพนักงานใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="0e415-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0e415-208">โปรดติดต่อผู้ดูแลระบบของคุณ เพื่อให้แน่ใจว่าเรกคอร์ดพนักงานของคุณเชื่อมโยงอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0e415-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="0e415-209">การแปลแสดงไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0e415-209">Translations don't display correctly</span></span>

<span data-ttu-id="0e415-210">หากการแปลไม่แสดงตามที่คาดไว้ ให้ตรวจสอบให้แน่ใจว่าภาษาที่คุณเลือกใน Teams ตรงกับภาษาที่เลือกไว้ใน ทรัพยากรบุคคล **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="0e415-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="0e415-211">ใน Teams ให้ดู **ภาษาของแอป** ใน **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="0e415-211">In Teams, look at **App language** in **Settings**.</span></span>

![การตั้งค่า Teams](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="0e415-213">ในทรัพยากรบุคคล ให้เลือก **การตั้งค่า** แล้วเลือก **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="0e415-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="0e415-214">ตรวจสอบว่าฟิลด์ **ภาษา** ตรงกับฟิลด์ **ภาษาของแอป** ใน Teams หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e415-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![ตัวเลือกผู้ใช้ทรัพยากรบุคคล](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="0e415-216">หากคุณยังคงพบปัญหาการแปล โปรดแจ้งให้เราทราบ</span><span class="sxs-lookup"><span data-stu-id="0e415-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="0e415-217">สำหรับข้อมูล ให้ดูที่ [การขอความช่วยเหลือสำหรับแอป Finance and Operations หรือ Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="0e415-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="0e415-218">เกิดข้อผิดพลาดขณะอนุมัติคำขอการลางานในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="0e415-219">ถ้าคุณได้รับข้อผิดพลาดขณะที่คุณพยายามอนุมัติคำขอการลางานในแอป Teams ให้ลองทำตามขั้นตอนการแก้ไขปัญหาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0e415-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="0e415-220">ตรวจสอบว่าบัญชีที่คุณใช้ในการเข้าสู่ระบบ Microsoft Teams เป็นเดียวกันกับที่คุณใช้สำหรับการเข้าถึง Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="0e415-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="0e415-221">ตรวจสอบว่าคุณเป็นผู้อนุมัติที่ถูกต้องสำหรับคำขอดังกล่าว โดยตรวจสอบการตั้งค่าลำดับงานสำหรับการอนุมัติการลางาน</span><span class="sxs-lookup"><span data-stu-id="0e415-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="0e415-222">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลำดับงานคำขอลางาน ดูที่ [สร้างลำดับงานคำขอลางาน](hr-leave-and-absence-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="0e415-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="0e415-223">ปล่อยให้ผู้อนุมัติไม่ได้รับข้อความสนทนาของ Teams ในการอนุมัติคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="0e415-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="0e415-224">ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการแจ้งเตือนสำหรับสภาพแวดล้อมและผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0e415-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="0e415-225">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) และ [เปิดหรือปิดการแจ้งเตือน Teams สำหรับผู้ใช้แต่ละราย](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)</span><span class="sxs-lookup"><span data-stu-id="0e415-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="0e415-226">ตรวจสอบให้แน่ใจว่าผู้ใช้ลงชื่อเข้าใช้แท็บ **การสนทนา** โดยใช้ข้อมูลส่วนบุคคลเดียวกับที่ผู้ใช้ใช้ในการอนุมัติคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="0e415-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="0e415-227">ใช้ข้อความ "ลงชื่อออก" แล้ว "ลงชื่อเข้าใช้" เพื่อลงชื่อเข้าใช้ด้วยข้อมูลส่วนบุคคลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0e415-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="0e415-228">หากปัญหายังคงอยู่ ให้ตรวจสอบสถานะของชุดงานระบบเหตุการณ์ทางธุรกิจในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="0e415-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="0e415-229">ถ้าอยู่ในขั้นที่รออยู่หรือปฏิบัติการ ให้ตรวจสอบย้อนกลับในอีกสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="0e415-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="0e415-230">หากสถานะยังคงไม่เปลี่ยนแปลง ให้บันทึกตั๋วการสนับสนุน เพื่อให้ทีมงานของเราสามารถแก้ปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="0e415-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="0e415-231">ปัญหาเกี่ยวกับความสามารถในการเข้าถึงที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="0e415-231">Known accessibility issues</span></span>

<span data-ttu-id="0e415-232">แอปพลิเคชันทรัพยากรบุคคลใน Teams มีปัญหาความสามารถในการเข้าถึงต่อไปนี้ซึ่งเรากำลังทำการแก้ไขในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="0e415-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="0e415-233">ออก</span><span class="sxs-lookup"><span data-stu-id="0e415-233">Issue</span></span> | <span data-ttu-id="0e415-234">วิธีการแก้ปัญหาหรือคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="0e415-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="0e415-235">การซูมภาพเป็น 400% บนเดสก์ท็อปจะซ่อนปุ่มการดำเนินการบางปุ่มจากมุมมอง</span><span class="sxs-lookup"><span data-stu-id="0e415-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="0e415-236">เราขอแนะนำให้ใช้แว่นขยายแทน จนกว่าเราจะสามารถสนับสนุนระดับการย่อ/ขยายนี้ได้</span><span class="sxs-lookup"><span data-stu-id="0e415-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="0e415-237">บนแท็บ **เวลาหยุดพัก** voiceover ประกาศการดำเนินการปุ่ม ในขณะที่อ่านส่วนหัวสำหรับกริดเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="0e415-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="0e415-238">ส่วนหัวและองค์ประกอบภายในกริดมีการจัดกลุ่มตามปี และจะสามารถยุบได้</span><span class="sxs-lookup"><span data-stu-id="0e415-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="0e415-239">Voiceover จะแปลเป็นสินค้าที่สามารถดำเนินการได้ แต่ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="0e415-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="0e415-240">บนแท็บ **เวลาหยุดพัก** มีท่าทางการรูดพิเศษเมื่อนำทางไปยัง **รหัสเหตุผล** ในคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="0e415-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="0e415-241">ไม่มีตัวควบคุมที่ซ่อนอยู่ซึ่งการนำทางการรูดกำลังพยายามเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="0e415-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="0e415-242">บนแท็บ **เวลาหยุดพัก** ถ้าคุณปัดนิ้วในขณะที่ปฏิทินเปิดอยู่ คุณจะไปอยู่ที่ภายนอกตัวควบคุม แทนที่จะอยู่ด้านบนในคำขอใหม่ หรือในขณะที่แก้ไขคำขอ</span><span class="sxs-lookup"><span data-stu-id="0e415-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="0e415-243">เมื่อคุณเข้าถึง **ไปยังวันนี้** ให้พิจารณาว่าจะเป็นจุดสิ้นสุดของการควบคุมและปัดนิ้วในทิศทางย้อนกลับเพื่อกลับไปด้านบน</span><span class="sxs-lookup"><span data-stu-id="0e415-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="0e415-244">บนแท็บ **แชท** โฟกัสจะข้ามไปที่ด้านบนสุด เมื่อคุณป้อนวันที่ในขณะที่ใช้เครื่องมือช่วยเหลือหรือการนำทางของคีย์บอร์ด</span><span class="sxs-lookup"><span data-stu-id="0e415-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="0e415-245">แตะจนกว่าคุณจะไปถึงพื้นที่อินพุตของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0e415-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="0e415-246">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="0e415-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="0e415-247">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="0e415-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="0e415-248">ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0e415-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="0e415-249">ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="0e415-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="0e415-250">อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/)</span><span class="sxs-lookup"><span data-stu-id="0e415-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="0e415-251">บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง</span><span class="sxs-lookup"><span data-stu-id="0e415-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="0e415-252">ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0e415-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="0e415-253">โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="0e415-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="0e415-254">บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="0e415-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0e415-255">ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure</span><span class="sxs-lookup"><span data-stu-id="0e415-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="0e415-256">เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="0e415-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="0e415-257">อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)</span><span class="sxs-lookup"><span data-stu-id="0e415-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="0e415-258">เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="0e415-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="0e415-259">Microsoft Teams, กริดเหตุการณ์ Azure และ Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="0e415-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="0e415-260">เมื่อใช้แอป Dynamics 365 Human Resources ใน Microsoft Teams ข้อมูลลูกค้าบางรายอาจส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่มีการใช้บริการ Human Resources ของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="0e415-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="0e415-261">Dynamics 365 Human Resources ส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยังกริดเหตุการณ์ Microsoft Azure และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="0e415-262">ข้อมูลนี้อาจจัดเก็บไว้ในกริดเหตุการณ์ Microsoft Azure นานถึง 24 ชั่วโมงและจะประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="0e415-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0e415-263">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="0e415-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="0e415-264">ในขณะที่สนทนากับบอทแชทในแอปทรัพยากรบุคคล เนื้อหาการสนทนาอาจจัดเก็บไว้ใน Azure Cosmos DB และส่งผ่านไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="0e415-265">ข้อมูลนี้อาจจัดเก็บไว้ใน Azure Cosmos DB ได้สูงสุด24ชั่วโมงและอาจได้รับการประมวลผลภายนอกภูมิภาคทางภูมิศาสตร์ที่มีการปรับใช้บริการทรัพยากรบุคคลของผู้เช่าของคุณจะถูกเข้ารหัสในการส่งต่อและในส่วนที่เหลือและไม่ได้ใช้โดย Microsoft หรือผู้ประมวลผลย่อยสำหรับการฝึกอบรมหรือการให้ปรับปรุงการบริการ</span><span class="sxs-lookup"><span data-stu-id="0e415-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0e415-266">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="0e415-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="0e415-267">เมื่อต้องการจำกัดการเข้าถึงแอปพลิเคชันทรัพยากรบุคคลใน Microsoft Teams สำหรับองค์กรหรือผู้ใช้ภายในองค์กรของคุณ ให้ดูที่ [จัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="0e415-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="0e415-268">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="0e415-268">See also</span></span>

[<span data-ttu-id="0e415-269">ดาวน์โหลดและติดตั้ง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="0e415-270">ศูนย์ความช่วยเหลือ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="0e415-271">แอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="0e415-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
