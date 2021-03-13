---
title: แอปทรัพยากรบุคคลใน Teams
description: หัวข้อนี้จะแนะนำแอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: tfehr
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba520f873de5b20111f9134e87281bcdf4025785
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114449"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="809de-103">แอปทรัพยากรบุคคลใน Teams</span><span class="sxs-lookup"><span data-stu-id="809de-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="809de-104">แอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้พนักงานสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดได้ใน Microsoft Teams ในทันที</span><span class="sxs-lookup"><span data-stu-id="809de-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="809de-105">พนักงานสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูล</span><span class="sxs-lookup"><span data-stu-id="809de-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="809de-106">แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="809de-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="809de-107">นอกจากนี้ พวหเขายังสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะเกิดขึ้นของคุณในทีมและการสนทนาภายนอกแอปพลิเคชันทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="809de-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![บอทของแอปการลาหยุด Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![ใบร้องขอการลางานของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="809de-111">ติดตั้งและตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="809de-111">Install and setup</span></span>

<span data-ttu-id="809de-112">คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams</span><span class="sxs-lookup"><span data-stu-id="809de-112">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="809de-113">สำหรับข้อมูลเกี่ยวกับการติดตั้งแอป Teams ให้ดูที่ [การจัดการคำร้องขอการลาหยุดใน Teams](hr-teams-leave-app.md)</span><span class="sxs-lookup"><span data-stu-id="809de-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="809de-114">สำหรับข้อมูลเกี่ยวกับการจัดการสิทธิ์การได้รับอนุญาตของแอปใน Teams ให้ดูที่ [การจัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="809de-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="809de-115">เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="809de-115">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="809de-116">ถ้าคุณต้องการให้ผู้ใช้ได้รับการแจ้งเตือนคำขอการลางานในแอป Teams คุณต้องเปิดใช้งานการแจ้งเตือนใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="809de-116">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="809de-117">เฉพาะผู้ใช้ที่ลงชื่อเข้าใช้ Teams และใช้แอป Human Resources Teams เท่านั้นที่จะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="809de-117">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="809de-118">ในทรัพยากรบุคคล เลือก **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="809de-118">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="809de-119">เลือก **ลิงก์**</span><span class="sxs-lookup"><span data-stu-id="809de-119">Select **Links**.</span></span>

3. <span data-ttu-id="809de-120">ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ระบบ**</span><span class="sxs-lookup"><span data-stu-id="809de-120">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="809de-121">บนแท็บ **ทั่วไป** ตั้งค่า **เปิดใช้งานการแจ้งเตือนสำหรับแอป Teams** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="809de-121">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![เปิดใช้งานการแจ้งเตือนแอป Teams ในพารามิเตอร์ระบบ](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="809de-123">เมื่อต้องการเปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้ทั้งหมด ให้เลือก **ใช่** ที่พร้อมท์</span><span class="sxs-lookup"><span data-stu-id="809de-123">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![เปิดใช้งานการแจ้งเตือนของ Teams สำหรับผู้ใช้ทั้งหมด](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="809de-125">เปิดหรือปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้แต่ละราย</span><span class="sxs-lookup"><span data-stu-id="809de-125">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="809de-126">หลังจากที่คุณได้เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources Teams แล้ว คุณสามารถเปิดหรือปิดการแจ้งเตือนสำหรับผู้ใช้แต่ละรายได้</span><span class="sxs-lookup"><span data-stu-id="809de-126">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="809de-127">ในทรัพยากรบุคคล เลือก **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="809de-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="809de-128">เลือก **ลิงก์**</span><span class="sxs-lookup"><span data-stu-id="809de-128">Select **Links**.</span></span>

3. <span data-ttu-id="809de-129">ภายใต้ **ผู้ใช้** ให้เลือก **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="809de-129">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="809de-130">เลือกแท็บ **ลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="809de-130">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="809de-131">ตั้งค่า **เปิดใช้งานการแจ้งเตือนสำหรับแอป Teams** เป็น **ใช่** เพื่อเปิดใช้งานการแจ้งเตือนสำหรับผู้ใช้ หรือ **ไม่** เพื่อปิดใช้งานการแจ้งเตือนสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="809de-131">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![เปิดใช้งานการแจ้งเตือนของแอป Teams ในแท็บลำดับงานของตัวเลือกผู้ใช้](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="809de-133">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="809de-133">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="809de-134">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="809de-134">Known issues</span></span>

| <span data-ttu-id="809de-135">ออก</span><span class="sxs-lookup"><span data-stu-id="809de-135">Issue</span></span> | <span data-ttu-id="809de-136">สถานะ</span><span class="sxs-lookup"><span data-stu-id="809de-136">Status</span></span> |
| --- | --- |
| <span data-ttu-id="809de-137">ยอดดุลไม่ถูกต้องเมื่อส่งเวลาสำหรับวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="809de-137">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="809de-138">การคาดการณ์ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="809de-138">Forecasting isn't yet available.</span></span> <span data-ttu-id="809de-139">ยอดดุลปัจจุบันแสดงสำหรับวันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="809de-139">The balance displays for the current date.</span></span> |
| <span data-ttu-id="809de-140">ไม่สามารถยกเลิกการร้องขอ **รอการตรวจทาน** ได้</span><span class="sxs-lookup"><span data-stu-id="809de-140">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="809de-141">ฟังก์ชันนี้ไม่ได้รับการสนับสนุนในขณะนี้และจะถูกเพิ่มในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="809de-141">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="809de-142">มีการคำนวณข้อมูลยอดดุล ณ วันที่วันนี้</span><span class="sxs-lookup"><span data-stu-id="809de-142">Balance information is calculated as of today.</span></span> | <span data-ttu-id="809de-143">ระบบปัจจุบันไม่แสดงยอดดุล ณ วันที่ของรอบระยะเวลาการคงค้าง ถึงแม้ว่าจะมีการตั้งค่าคอนฟิกในพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="809de-143">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="809de-144">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="809de-144">Troubleshooting</span></span>

<span data-ttu-id="809de-145">ถ้าผู้ใช้กำลังมีปัญหาในการเข้าสู่ระบบ หรือใช้แอป Human Resources Teams ให้ลองปฏิบัติตามคำแนะนำในการแก้ไขปัญหาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="809de-145">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="809de-146">ถ้าคุณยังคงมีปัญหาหลังการแก้ไขปัญหา โปรดติดต่อฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="809de-146">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="809de-147">สำหรับข้อมูลเพิ่มเติม ดู [รับการสนับสนุน](hr-admin-troubleshooting-support.md)</span><span class="sxs-lookup"><span data-stu-id="809de-147">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="809de-148">ไม่สามารถเข้าสู่ระบบแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="809de-148">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="809de-149">ถ้าผู้ติดต่อของผู้ใช้คุณ เนื่องจากไม่สามารถเข้าสู่ระบบแอปได้ ให้ตรวจสอบว่าผู้ใช้มีเรกคอร์ดพนักงานที่เกี่ยวข้องใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="809de-149">If a user contacts you because they can't sign into the app, verify that the user has an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="809de-150">เกิดข้อผิดพลาดขณะอนุมัติคำขอการลางานในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="809de-150">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="809de-151">ถ้าผู้ใช้ได้รับข้อผิดพลาดขณะพยายามอนุมัติคำขอการลางานในแอป Teams ให้ทำตามขั้นตอนการแก้ไขปัญหาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="809de-151">If a user receives an error while trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="809de-152">ตรวจสอบว่าบัญชี Teams ของพวกเขาเป็นอันเดียวกับที่ใช้สำหรับการเข้าถึง Human Resources</span><span class="sxs-lookup"><span data-stu-id="809de-152">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="809de-153">ตรวจสอบว่าพวกเขาเป็นผู้อนุมัติที่ถูกต้องสำหรับคำขอดังกล่าว โดยตรวจสอบการตั้งค่าลำดับงานสำหรับการอนุมัติการลางาน</span><span class="sxs-lookup"><span data-stu-id="809de-153">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="809de-154">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลำดับงานคำขอลางาน ดูที่ [สร้างลำดับงานคำขอลางาน](hr-leave-and-absence-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="809de-154">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="809de-155">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="809de-155">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="809de-156">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="809de-156">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="809de-157">ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="809de-157">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="809de-158">ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="809de-158">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="809de-159">อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/)</span><span class="sxs-lookup"><span data-stu-id="809de-159">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="809de-160">บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง</span><span class="sxs-lookup"><span data-stu-id="809de-160">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="809de-161">ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="809de-161">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="809de-162">โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="809de-162">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="809de-163">บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="809de-163">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="809de-164">ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure</span><span class="sxs-lookup"><span data-stu-id="809de-164">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="809de-165">เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="809de-165">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="809de-166">อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)</span><span class="sxs-lookup"><span data-stu-id="809de-166">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="809de-167">เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="809de-167">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="809de-168">Microsoft Teams, กริดเหตุการณ์ Azure และ Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="809de-168">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="809de-169">เมื่อใช้แอป Dynamics 365 Human Resources ใน Microsoft Teams ข้อมูลลูกค้าบางรายอาจส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่มีการใช้บริการ Human Resources ของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="809de-169">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="809de-170">Dynamics 365 Human Resources ส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยังกริดเหตุการณ์ Microsoft Azure และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="809de-170">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="809de-171">ข้อมูลนี้อาจจัดเก็บไว้ในกริดเหตุการณ์ Microsoft Azure นานถึง 24 ชั่วโมงและจะประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="809de-171">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="809de-172">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="809de-172">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="809de-173">ในขณะที่สนทนากับบอทแชทในแอปทรัพยากรบุคคล เนื้อหาการสนทนาอาจจัดเก็บไว้ใน Azure Cosmos DB และส่งผ่านไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="809de-173">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="809de-174">ข้อมูลนี้อาจจัดเก็บไว้ใน Azure Cosmos DB ได้สูงสุด24ชั่วโมงและอาจได้รับการประมวลผลภายนอกภูมิภาคทางภูมิศาสตร์ที่มีการปรับใช้บริการทรัพยากรบุคคลของผู้เช่าของคุณจะถูกเข้ารหัสในการส่งต่อและในส่วนที่เหลือและไม่ได้ใช้โดย Microsoft หรือผู้ประมวลผลย่อยสำหรับการฝึกอบรมหรือการให้ปรับปรุงการบริการ</span><span class="sxs-lookup"><span data-stu-id="809de-174">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="809de-175">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="809de-175">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="809de-176">เมื่อต้องการจำกัดการเข้าถึงแอปพลิเคชันทรัพยากรบุคคลใน Microsoft Teams สำหรับองค์กรหรือผู้ใช้ภายในองค์กรของคุณ ให้ดูที่ [จัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="809de-176">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="809de-177">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="809de-177">See also</span></span> 

[<span data-ttu-id="809de-178">ดาวน์โหลดและติดตั้ง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="809de-178">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="809de-179">ศูนย์ความช่วยเหลือ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="809de-179">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="809de-180">จัดการคำขอลางานใน Teams</span><span class="sxs-lookup"><span data-stu-id="809de-180">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

