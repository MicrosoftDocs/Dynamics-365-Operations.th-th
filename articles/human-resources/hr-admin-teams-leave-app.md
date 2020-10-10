---
title: แอปทรัพยากรบุคคลใน Teams
description: หัวข้อนี้จะแนะนำแอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
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
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828925"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="7007e-103">แอปทรัพยากรบุคคลใน Teams</span><span class="sxs-lookup"><span data-stu-id="7007e-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7007e-104">แอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้พนักงานสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดได้ใน Microsoft Teams ในทันที</span><span class="sxs-lookup"><span data-stu-id="7007e-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="7007e-105">พนักงานสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7007e-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="7007e-106">แท็บ **การลาหยุด** แสดงรายละเอียดเพิ่มเติม นอกจากนี้ผู้ใช้จะสามารถส่งข้อมูลเกี่ยวกับการลาานที่กำลังจะเกิดขึ้นในทีมและการสนทนานอกแอปพลิเคชันทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="7007e-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![บอทของแอปการลาหยุด Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![ใบร้องขอการลางานของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="7007e-110">ติดตั้งและตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="7007e-110">Install and setup</span></span>

<span data-ttu-id="7007e-111">คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams</span><span class="sxs-lookup"><span data-stu-id="7007e-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="7007e-112">สำหรับข้อมูลเกี่ยวกับการติดตั้งแอป Teams ให้ดูที่ [การจัดการคำร้องขอการลาหยุดใน Teams](hr-teams-leave-app.md)</span><span class="sxs-lookup"><span data-stu-id="7007e-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="7007e-113">สำหรับข้อมูลเกี่ยวกับการจัดการสิทธิ์การได้รับอนุญาตของแอปใน Teams ให้ดูที่ [การจัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="7007e-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="7007e-114">เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="7007e-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="7007e-115">ถ้าคุณต้องการให้ผู้ใช้ได้รับการแจ้งเตือนคำขอการลางานในแอป Teams คุณต้องเปิดใช้งานการแจ้งเตือนใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="7007e-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="7007e-116">เฉพาะผู้ใช้ที่ลงชื่อเข้าใช้ Teams และใช้แอป Human Resources Teams เท่านั้นที่จะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="7007e-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="7007e-117">ในทรัพยากรบุคคล เลือก **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="7007e-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="7007e-118">เลือก **ลิงก์**</span><span class="sxs-lookup"><span data-stu-id="7007e-118">Select **Links**.</span></span>

3. <span data-ttu-id="7007e-119">ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ระบบ**</span><span class="sxs-lookup"><span data-stu-id="7007e-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="7007e-120">บนแท็บ **ทั่วไป** ตั้งค่า **เปิดใช้งานการแจ้งเตือนสำหรับแอป Teams** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7007e-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![เปิดใช้งานการแจ้งเตือนแอป Teams ในพารามิเตอร์ระบบ](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="7007e-122">เมื่อต้องการเปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้ทั้งหมด ให้เลือก **ใช่** ที่พร้อมท์</span><span class="sxs-lookup"><span data-stu-id="7007e-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![เปิดใช้งานการแจ้งเตือนของ Teams สำหรับผู้ใช้ทั้งหมด](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="7007e-124">เปิดหรือปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้แต่ละราย</span><span class="sxs-lookup"><span data-stu-id="7007e-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="7007e-125">หลังจากที่คุณได้เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources Teams แล้ว คุณสามารถเปิดหรือปิดการแจ้งเตือนสำหรับผู้ใช้แต่ละรายได้</span><span class="sxs-lookup"><span data-stu-id="7007e-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="7007e-126">ในทรัพยากรบุคคล เลือก **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="7007e-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="7007e-127">เลือก **ลิงก์**</span><span class="sxs-lookup"><span data-stu-id="7007e-127">Select **Links**.</span></span>

3. <span data-ttu-id="7007e-128">ภายใต้ **ผู้ใช้** ให้เลือก **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="7007e-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="7007e-129">เลือกแท็บ **ลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="7007e-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="7007e-130">ตั้งค่า **เปิดใช้งานการแจ้งเตือนสำหรับแอป Teams** เป็น **ใช่** เพื่อเปิดใช้งานการแจ้งเตือนสำหรับผู้ใช้ หรือ **ไม่** เพื่อปิดใช้งานการแจ้งเตือนสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="7007e-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![เปิดใช้งานการแจ้งเตือนของแอป Teams ในแท็บลำดับงานของตัวเลือกผู้ใช้](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="7007e-132">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7007e-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="7007e-133">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="7007e-133">Known issues</span></span>

| <span data-ttu-id="7007e-134">ออก</span><span class="sxs-lookup"><span data-stu-id="7007e-134">Issue</span></span> | <span data-ttu-id="7007e-135">สถานะ</span><span class="sxs-lookup"><span data-stu-id="7007e-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="7007e-136">การเลื่อนแนวนอนไม่ทำงานบนโทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="7007e-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="7007e-137">การเลื่อนแนวนอนไม่ใช่ปัญหาบนอุปกรณ์ iOS หรือเดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="7007e-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="7007e-138">เรากำลังดำเนินการแก้ไขสำหรับ Android</span><span class="sxs-lookup"><span data-stu-id="7007e-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="7007e-139">ยอดดุลไม่ถูกต้องเมื่อส่งเวลาสำหรับวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="7007e-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="7007e-140">การคาดการณ์ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7007e-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="7007e-141">ยอดดุลปัจจุบันแสดงสำหรับวันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7007e-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="7007e-142">ไม่สามารถยกเลิกการร้องขอ **รอการตรวจทาน** ได้</span><span class="sxs-lookup"><span data-stu-id="7007e-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="7007e-143">ฟังก์ชันนี้ไม่ได้รับการสนับสนุนในขณะนี้และจะถูกเพิ่มในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="7007e-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="7007e-144">มีการคำนวณข้อมูลยอดดุล ณ วันที่วันนี้</span><span class="sxs-lookup"><span data-stu-id="7007e-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="7007e-145">ระบบปัจจุบันไม่แสดงยอดดุล ณ วันที่ของรอบระยะเวลาการคงค้าง ถึงแม้ว่าจะมีการตั้งค่าคอนฟิกในพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="7007e-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="7007e-146">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="7007e-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="7007e-147">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="7007e-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="7007e-148">ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="7007e-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="7007e-149">ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="7007e-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="7007e-150">อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/)</span><span class="sxs-lookup"><span data-stu-id="7007e-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="7007e-151">บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง</span><span class="sxs-lookup"><span data-stu-id="7007e-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="7007e-152">ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="7007e-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="7007e-153">โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="7007e-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="7007e-154">บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="7007e-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7007e-155">ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure</span><span class="sxs-lookup"><span data-stu-id="7007e-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="7007e-156">เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="7007e-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="7007e-157">อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)</span><span class="sxs-lookup"><span data-stu-id="7007e-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="7007e-158">เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="7007e-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="7007e-159">Microsoft Teams, กริดเหตุการณ์ Azure และ Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7007e-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="7007e-160">เมื่อใช้แอป Dynamics 365 Human Resources ใน Microsoft Teams ข้อมูลลูกค้าบางรายอาจส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่มีการใช้บริการ Human Resources ของผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="7007e-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="7007e-161">Dynamics 365 Human Resources ส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยังกริดเหตุการณ์ Microsoft Azure และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7007e-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="7007e-162">ข้อมูลนี้อาจจัดเก็บไว้ในกริดเหตุการณ์ Microsoft Azure นานถึง 24 ชั่วโมงและจะประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="7007e-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="7007e-163">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="7007e-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="7007e-164">ในขณะที่สนทนากับบอทแชทในแอปทรัพยากรบุคคล เนื้อหาการสนทนาอาจจัดเก็บไว้ใน Azure Cosmos DB และส่งผ่านไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7007e-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="7007e-165">ข้อมูลนี้อาจจัดเก็บไว้ใน Azure Cosmos DB ได้สูงสุด24ชั่วโมงและอาจได้รับการประมวลผลภายนอกภูมิภาคทางภูมิศาสตร์ที่มีการปรับใช้บริการทรัพยากรบุคคลของผู้เช่าของคุณจะถูกเข้ารหัสในการส่งต่อและในส่วนที่เหลือและไม่ได้ใช้โดย Microsoft หรือผู้ประมวลผลย่อยสำหรับการฝึกอบรมหรือการให้ปรับปรุงการบริการ</span><span class="sxs-lookup"><span data-stu-id="7007e-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="7007e-166">เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="7007e-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="7007e-167">เมื่อต้องการจำกัดการเข้าถึงแอปพลิเคชันทรัพยากรบุคคลใน Microsoft Teams สำหรับองค์กรหรือผู้ใช้ภายในองค์กรของคุณ ให้ดูที่ [จัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="7007e-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="7007e-168">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="7007e-168">See also</span></span> 

[<span data-ttu-id="7007e-169">ดาวน์โหลดและติดตั้ง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7007e-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="7007e-170">ศูนย์ความช่วยเหลือ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7007e-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="7007e-171">จัดการคำขอลางานใน Teams</span><span class="sxs-lookup"><span data-stu-id="7007e-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

