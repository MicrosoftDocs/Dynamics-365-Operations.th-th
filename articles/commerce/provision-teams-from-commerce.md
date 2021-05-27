---
title: เตรียมใช้งาน Microsoft Teams จาก Dynamics 365 Commerce
description: หัวข้อนี้จะอธิบายวิธีการเตรียมใช้งาน Microsoft Teams โดยใช้ข้อมูลองค์กรจาก Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1cb28fb50bdc972d1dae6d03a45f70a2f3a63357
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022457"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="0728b-103">เตรียมใช้งาน Microsoft Teams จาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0728b-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0728b-104">หัวข้อนี้จะอธิบายวิธีการเตรียมใช้งาน Microsoft Teams โดยใช้ข้อมูลองค์กรจาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0728b-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0728b-105">Dynamics 365 Commerce เสนอวิธีที่ง่ายในการเตรียมใช้งาน Teams ถ้าคุณยังไม่ได้ตั้งค่า Teams ให้กับร้านค้าปลีกของคุณที่นั่น</span><span class="sxs-lookup"><span data-stu-id="0728b-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="0728b-106">โดยการใช้ข้อมูลที่กําหนดไว้อย่างชัดเจนจาก Commerce ที่คุณต้องการใช้ใน Teams คุณสามารถช่วยให้พนักงานร้านค้าของคุณสามารถเริ่มต้นใช้งานใน Teams ได้</span><span class="sxs-lookup"><span data-stu-id="0728b-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="0728b-107">ข้อมูลนี้ประกอบด้วยลำดับชั้นขององค์กร ชื่อร้านค้า ข้อมูลพนักงาน และบัญชี Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="0728b-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="0728b-108">กระบวนการเตรียมใช้งาน Teams มีสองขั้นตอนหลักดังนี้</span><span class="sxs-lookup"><span data-stu-id="0728b-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="0728b-109">ใน Teams ให้สร้างทีมงานให้กับร้านค้าปลีกแต่ละร้าน และเพิ่มผู้ปฏิบัติงานของร้านค้าเป็นสมาชิกของทีมงานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="0728b-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="0728b-110">ถ้าพนักงานเชื่อมโยงกับร้านค้าปลีกมากกว่าหนึ่งร้าน การเป็นสมาชิกทีมงานจะสะท้อนถึงข้อเท็จจริงนั้น</span><span class="sxs-lookup"><span data-stu-id="0728b-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="0728b-111">ทีมการสื่อสารที่มีผู้จัดการภูมิภาคเป็นสมาชิกจะถูกสร้างขึ้นเพื่อช่วยเผยแพร่งานจาก Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="0728b-112">อัพโหลดลำดับชั้นองค์กรของคุณจาก Commerce ไปที่ Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="0728b-113">เตรียมใช้งาน Teams ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="0728b-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="0728b-114">ก่อนที่คุณจะเตรียมใช้งาน Microsoft Teams ให้จัดเตรียมงานเหล่านี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0728b-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="0728b-115">ยืนยันว่าผู้จัดการส่วนภูมิภาคทั้งหมดได้ยืนยันให้ผู้จัดการฝ่ายสื่อสารแล้ว</span><span class="sxs-lookup"><span data-stu-id="0728b-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="0728b-116">ยืนยันว่าบัญชี Azure ของผู้จัดการร้านค้าทุกแห่งและผู้ปฏิบัติงานได้รับการเชื่อมโยงกับเรกคอร์ดผู้ปฏิบัติงานของผู้จัดการหรือผู้ปฏิบัติงานในศูนย์ควบคุม Commerce หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0728b-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="0728b-117">เมื่อต้องการเตรียมใช้งาน Teams ในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0728b-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0728b-118">ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**</span><span class="sxs-lookup"><span data-stu-id="0728b-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="0728b-119">บนบานหน้าต่างการดำเนินการ เลือก **เตรียมใช้งาน Teams**</span><span class="sxs-lookup"><span data-stu-id="0728b-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="0728b-120">ชุดงานที่มีชื่อว่า **การเตรียมใช้งาน Teams** จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0728b-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="0728b-121">ไปที่ **การจัดการระบบ \> การสอบถาม \> ชุดงาน** และค้นหางานล่าสุดที่มีคำอธิบาย **การเตรียมใช้งาน Teams**</span><span class="sxs-lookup"><span data-stu-id="0728b-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="0728b-122">รอจนกว่างานนี้จะเสร็จสิ้นการรัน</span><span class="sxs-lookup"><span data-stu-id="0728b-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="0728b-123">หากไม่มีผู้จัดการระดับภูมิภาค ผู้จัดการร้านค้า และผู้ปฏิบัติงานร้านค้าใดเกี่ยวข้องกับลิขสิทธิ์ของ Teams คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ล้มเหลวในการดึงข้อมูลประเภท Sku ที่รับผิดชอบของผู้ใช้"</span><span class="sxs-lookup"><span data-stu-id="0728b-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="0728b-124">เมื่อต้องการแก้ปัญหา ให้เลือก **ซิงค์ Teams และสมาชิก** ในบานหน้าต่างการการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0728b-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="0728b-125">ตรวจสอบความถูกต้องของการเตรียมใช้งาน Teams ในศูนย์การจัดการ Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="0728b-126">หากต้องการตรวจสอบความถูกต้องของการเตรียมใช้งาน Microsoft Teams ในศูนย์การจัดการ Microsoft Teams ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0728b-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="0728b-127">ไปที่ [ศูนย์การจัดการ Teams](https://admin.teams.microsoft.com/)และเข้าสู่ระบบในฐานะผู้ดูแลระบบของผู้เช่า e-commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="0728b-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="0728b-128">ในบานหน้าต่างนําทางด้านซ้าย ให้เลือก **Teams** เพื่อขยาย แล้วเลือก **จัดการ Teams**</span><span class="sxs-lookup"><span data-stu-id="0728b-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="0728b-129">ยืนยันว่ามีการสร้างทีมงานหนึ่งทีมขึ้นแล้วในร้านค้าปลีก Commerce แต่ละร้าน</span><span class="sxs-lookup"><span data-stu-id="0728b-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="0728b-130">เลือกทีมงาน และยืนยันว่ามีการเพิ่มผู้ปฏิบัติงานของร้านค้าเป็นสมาชิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="0728b-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="0728b-131">ในบานหน้าต่างนําทางด้านซ้าย ให้เลือก **ผู้ใช้** และยืนยันว่าพนักงานในร้านค้าทั้งหมดในร้านค้าทั้งหมดได้เพิ่มเป็นผู้ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="0728b-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="0728b-132">ตัวอย่างต่อไปนี้จะแสดงตัวอย่างของหน้า **จัดการ Teams** ในศูนย์การจัดการ Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![ตัวอย่างของหน้าการจัดการทีมงานในศูนย์การจัดการ Teams](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="0728b-134">อัพโหลดลำดับชั้นองค์กร Commerce ไปที่ Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="0728b-135">ลำดับชั้นองค์กรของ Commerce สามารถใช้ใน Microsoft Teams เพื่อเผยแพร่งานไปยังร้านค้าทั้งหมดหรือร้านค้าที่เลือกที่ใช้โครงสร้างลำดับชั้นเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0728b-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="0728b-136">หากต้องการอัพโหลดลำดับชั้นองค์กรของ Commerce ไปยัง Teams ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="0728b-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="0728b-137">ในศูนย์ควบคุม Commerce ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**</span><span class="sxs-lookup"><span data-stu-id="0728b-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="0728b-138">เลือก **ดาวน์โหลดลำดับชั้นเป้าหมาย** แล้วเลือก **ร้านค้าปลีกตามภูมิภาค** เพื่อดาวน์โหลดไฟล์ค่าที่แบ่งด้วยเครื่องหมายจุลภาค (CSV) ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="0728b-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="0728b-139">ติดตั้งโมดูล Microsoft Teams PowerShell โดยปฏิบัติตามขั้นตอนต่อไปนี้ใน [ติดตั้ง Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install)</span><span class="sxs-lookup"><span data-stu-id="0728b-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="0728b-140">เมื่อคุณเห็นพร้อมต์ในหน้าต่าง Teams PowerShell เข้าสู่ระบบโดยใช้บัญชีผู้ดูแลระบบของผู้เช่า Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="0728b-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="0728b-141">ปฏิบัติตามขั้นตอนใน [ตั้งค่าลำดับชั้นของเป้าหมายทีมงาน](/microsoftteams/set-up-your-team-hierarchy) ของคุณเพื่ออัพโหลดไฟล์ CSV ไปยังลำดับชั้นเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="0728b-141">Follow the steps in [Set up your team targeting hierarchy](/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="0728b-142">ตรวจสอบว่าอัพโหลดลำดับชั้นขององค์กรไปยัง Teamsแล้ว</span><span class="sxs-lookup"><span data-stu-id="0728b-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="0728b-143">หากต้องการตรวจสอบว่าอัพโหลดลำดับชั้นขององค์กรไปยัง Microsoft Teams แล้ว ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0728b-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="0728b-144">ลงชื่อเข้าใช้สู่ Teams ในฐานะผู้จัดการการสื่อสาร</span><span class="sxs-lookup"><span data-stu-id="0728b-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="0728b-145">ในบานหน้าต่างนําทางด้านซ้าย ให้เลือก **งานตามผู้วางแผน**</span><span class="sxs-lookup"><span data-stu-id="0728b-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="0728b-146">บนแท็บ **รายการที่เผยแพร่** ให้สร้างรายการใหม่ที่มีงานดัมมี</span><span class="sxs-lookup"><span data-stu-id="0728b-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="0728b-147">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="0728b-147">Select **Publish**.</span></span> <span data-ttu-id="0728b-148">ลำดับชั้นขององค์กรควรแสดงในกล่องโต้ตอบ **เลือกว่าใครจะเผยแพร่** ดังที่แสดงในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0728b-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![ตัวอย่างของลำดับชั้นขององค์กรในกล่องโต้ตอบ เลือกผู้ที่จะเผยแพร่ไปยัง](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="0728b-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0728b-150">Additional resources</span></span>

[<span data-ttu-id="0728b-151">ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="0728b-152">เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="0728b-153">ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="0728b-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="0728b-154">จัดการบทบาทผู้ใช้ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="0728b-155">แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="0728b-156">คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0728b-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)