---
title: แอปทรัพยากรบุคคลใน Teams
description: หัวข้อนี้จะแนะนำแอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: AnnBe
ms.date: 08/06/2020
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
ms.openlocfilehash: 4822cc6560926df878a8b4e9f821b331ede27a8c
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666371"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="2ebe6-103">แอปทรัพยากรบุคคลใน Teams</span><span class="sxs-lookup"><span data-stu-id="2ebe6-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2ebe6-104">แอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้พนักงานสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดได้ใน Microsoft Teams ในทันที</span><span class="sxs-lookup"><span data-stu-id="2ebe6-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="2ebe6-105">พนักงานสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2ebe6-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="2ebe6-106">แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="2ebe6-106">The **Time off** tab provides more detailed information.</span></span>

![บอทของแอปการลาหยุด Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="2ebe6-109">ติดตั้งและตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="2ebe6-109">Install and setup</span></span>

<span data-ttu-id="2ebe6-110">คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams</span><span class="sxs-lookup"><span data-stu-id="2ebe6-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="2ebe6-111">สำหรับข้อมูลเกี่ยวกับการติดตั้งแอป Teams ให้ดูที่ [การจัดการคำร้องขอการลาหยุดใน Teams](hr-teams-leave-app.md)</span><span class="sxs-lookup"><span data-stu-id="2ebe6-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="2ebe6-112">สำหรับข้อมูลเกี่ยวกับการจัดการสิทธิ์การได้รับอนุญาตของแอปใน Teams ให้ดูที่ [การจัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="2ebe6-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="2ebe6-113">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="2ebe6-113">Known issues</span></span>

| <span data-ttu-id="2ebe6-114">ออก</span><span class="sxs-lookup"><span data-stu-id="2ebe6-114">Issue</span></span> | <span data-ttu-id="2ebe6-115">สถานะ</span><span class="sxs-lookup"><span data-stu-id="2ebe6-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="2ebe6-116">การเลื่อนแนวนอนไม่ทำงานบนโทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="2ebe6-116">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="2ebe6-117">การเลื่อนแนวนอนไม่ใช่ปัญหาบนอุปกรณ์ iOS หรือเดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="2ebe6-117">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="2ebe6-118">เรากำลังดำเนินการแก้ไขสำหรับ Android</span><span class="sxs-lookup"><span data-stu-id="2ebe6-118">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="2ebe6-119">ข้อผิดพลาด: มีปัญหาในการค้นหาสภาพแวดล้อมที่จะเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="2ebe6-119">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="2ebe6-120">คุณอาจได้รับข้อผิดพลาดนี้ แม้ว่าคุณจะได้ตรวจสอบความถูกต้องว่าผู้ใช้สามารถเข้าถึงสภาพแวดล้อมของทรัพยากรบุคคลอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="2ebe6-120">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="2ebe6-121">นอกจากนี้ คุณอาจไม่เห็นสภาพแวดล้อมทั้งหมดที่คุณคาดไว้</span><span class="sxs-lookup"><span data-stu-id="2ebe6-121">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="2ebe6-122">จนกว่าเราจะแก้ไขปัญหานี้ ให้ลบผู้ใช้ และจากนั้น นำเข้าอีกครั้งเพื่อแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="2ebe6-122">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="2ebe6-123">ยอดดุลไม่ถูกต้องเมื่อส่งเวลาสำหรับวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="2ebe6-123">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="2ebe6-124">การคาดการณ์ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2ebe6-124">Forecasting isn't yet available.</span></span> <span data-ttu-id="2ebe6-125">ยอดดุลปัจจุบันแสดงสำหรับวันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2ebe6-125">The balance displays for the current date.</span></span> |
| <span data-ttu-id="2ebe6-126">เมื่อลดจำนวนชั่วโมงที่ใช้ในการร้องขอที่มีอยู่ **ยอดดุลคงเหลือจะถูก** จะลดลงแทนที่จะเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="2ebe6-126">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="2ebe6-127">เราจะจัดการปัญหาที่ทราบนี้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="2ebe6-127">We'll address this known issue in the future.</span></span> <span data-ttu-id="2ebe6-128">การแสดงผลไม่ถูกต้องแต่มีการปรับปรุงยอดที่ถูกต้องเมื่อทำการส่ง</span><span class="sxs-lookup"><span data-stu-id="2ebe6-128">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="2ebe6-129">ไม่สามารถยกเลิกการร้องขอ **รอการตรวจทาน** ได้</span><span class="sxs-lookup"><span data-stu-id="2ebe6-129">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="2ebe6-130">ฟังก์ชันนี้ไม่ได้รับการสนับสนุนในขณะนี้และจะถูกเพิ่มในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="2ebe6-130">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="2ebe6-131">มีการคำนวณข้อมูลยอดดุล ณ วันที่วันนี้</span><span class="sxs-lookup"><span data-stu-id="2ebe6-131">Balance information is calculated as of today.</span></span> | <span data-ttu-id="2ebe6-132">ระบบปัจจุบันไม่แสดงยอดดุล ณ วันที่ของรอบระยะเวลาการคงค้าง ถึงแม้ว่าจะมีการตั้งค่าคอนฟิกในพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="2ebe6-132">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="2ebe6-133">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="2ebe6-133">Privacy notice</span></span>

<span data-ttu-id="2ebe6-134">ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="2ebe6-134">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2ebe6-135">ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="2ebe6-135">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2ebe6-136">อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/)</span><span class="sxs-lookup"><span data-stu-id="2ebe6-136">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2ebe6-137">บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง</span><span class="sxs-lookup"><span data-stu-id="2ebe6-137">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2ebe6-138">ข้อมูลนี้จะถูกส่งผ่านไปยัง [กรอบงานบอท Azure](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2ebe6-138">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2ebe6-139">โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="2ebe6-139">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2ebe6-140">บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="2ebe6-140">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2ebe6-141">ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure</span><span class="sxs-lookup"><span data-stu-id="2ebe6-141">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2ebe6-142">เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ</span><span class="sxs-lookup"><span data-stu-id="2ebe6-142">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2ebe6-143">อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)</span><span class="sxs-lookup"><span data-stu-id="2ebe6-143">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2ebe6-144">เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="2ebe6-144">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="2ebe6-145">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="2ebe6-145">See also</span></span> 

[<span data-ttu-id="2ebe6-146">ดาวน์โหลดและติดตั้ง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2ebe6-146">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2ebe6-147">ศูนย์ความช่วยเหลือ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2ebe6-147">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2ebe6-148">จัดการคำขอลางานใน Teams</span><span class="sxs-lookup"><span data-stu-id="2ebe6-148">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

