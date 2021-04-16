---
title: ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS
description: หัวข้อนี้จะอธิบายวิธีการซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และการขายหน้าร้าน Dynamics 365 Commerce (POS)
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ca0cb32ac3ee508ddcd5346a895fb9904fa92517
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842755"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="4e60f-103">ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="4e60f-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4e60f-104">หัวข้อนี้จะอธิบายวิธีการซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และการขายหน้าร้าน Dynamics 365 Commerce (POS)</span><span class="sxs-lookup"><span data-stu-id="4e60f-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="4e60f-105">หนึ่งในวัตถุประสงค์หลักของการรวม Teams คือเพื่อเปิดใช้งานการซิงโครไนส์การจัดการงานระหว่างโปรแกรมประยุกต์ POS และ Teams</span><span class="sxs-lookup"><span data-stu-id="4e60f-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="4e60f-106">ด้วยวิธีนี้ พนักงานที่จัดเก็บสามารถใช้โปรแกรมประยุกต์ POS หรือ Teams เพื่อจัดการงานและไม่ต้องสลับโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="4e60f-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="4e60f-107">เนื่องจาก Planner ใช้เป็นที่เก็บภารกิจใน Teams จึงต้องมีการเชื่อมโยงระหว่าง Teams และ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4e60f-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="4e60f-108">ลิงค์นี้จะสร้างขึ้นโดยใช้รหัสแผนเฉพาะสำหรับทีมงานร้านค้าที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="4e60f-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="4e60f-109">ขั้นตอนต่อไปนี้แสดงวิธีการตั้งค่าการซิงโครไนส์การจัดการงานระหว่างโปรแกรมประยุกต์ POS และ Teams</span><span class="sxs-lookup"><span data-stu-id="4e60f-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="4e60f-110">เผยแพร่รายการงานทดสอบใน Teams</span><span class="sxs-lookup"><span data-stu-id="4e60f-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="4e60f-111">ขั้นตอนต่อไปนี้สมมติว่าทีมงานร้านค้าของคุณใช้การรวมการจัดการงาน Microsoft Teams กับ Commerce เป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="4e60f-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="4e60f-112">หากต้องการเผยแพร่รายการงานทดสอบใน Teams ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4e60f-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="4e60f-113">ลงชื่อเข้าใช้สู่ Teams ในฐานะผู้จัดการการสื่อสาร</span><span class="sxs-lookup"><span data-stu-id="4e60f-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="4e60f-114">โดยทั่วไป ผู้จัดการการสื่อสารคือผู้ใช้ที่มีบทบาทเป็น **ผู้จัดการภูมิภาค** ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="4e60f-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="4e60f-115">ในบานหน้าต่างนําทางด้านซ้าย ให้เลือก **งานตามผู้วางแผน**</span><span class="sxs-lookup"><span data-stu-id="4e60f-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="4e60f-116">บนแท็บ **รายการที่เผยแพร่** ให้เลือก **รายการใหม่** ที่ด้านล่างซ้าย และตั้งชื่อรายการงาน **รายการงานทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="4e60f-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="4e60f-117">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="4e60f-117">Select **Create**.</span></span> <span data-ttu-id="4e60f-118">รายการใหม่ปรากฎภายใต้ **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="4e60f-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="4e60f-119">ภายใต้ **ชื่องาน** ให้ตั้งชื่องานแรก **การรวมการทดสอบ Teams**</span><span class="sxs-lookup"><span data-stu-id="4e60f-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="4e60f-120">จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4e60f-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="4e60f-121">ในรายการ **แบบร่าง** ให้เลือกรายการงาน</span><span class="sxs-lookup"><span data-stu-id="4e60f-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="4e60f-122">แล้วเลือก  **เผยแพร่** ในมุมด้านขวาบน</span><span class="sxs-lookup"><span data-stu-id="4e60f-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="4e60f-123">ในกล่องโต้ตอบ **เลือกว่าใครจะเผยแพร่** ให้เลือกทีมงานที่ควรได้รับรายการงานทดสอบ</span><span class="sxs-lookup"><span data-stu-id="4e60f-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="4e60f-124">เลือก **ถัดไป** เพื่อตรวจทานแผนการเผยแพร่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4e60f-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="4e60f-125">ถ้าคุณต้องเปลี่ยนแปลง ให้เลือก  **ย้อนกลับ**</span><span class="sxs-lookup"><span data-stu-id="4e60f-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="4e60f-126">เลือก **ยืนยันเพื่อดําเนินการต่อ** แล้วเลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="4e60f-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="4e60f-127">หลังจากที่การเผยแพร่เสร็จสมบูรณ์ ข้อความที่ด้านบนของแท็บ **รายการที่เผยแพร่** บ่งชี้ว่ามีการจัดส่งรายการงานของคุณเสร็จเรียบร้อยแล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4e60f-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="4e60f-128">สำหรับข้อมูลเพิ่มเติม ให้ดู [เผยแพร่รายการงานเพื่อสร้างและติดตามงานในองค์กรของคุณ](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df)</span><span class="sxs-lookup"><span data-stu-id="4e60f-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="4e60f-129">เชื่อมโยง POS และ Teams เพื่อการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="4e60f-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="4e60f-130">หากต้องการเชื่อมโยงโปรแกรมประยุกต์ POS และ Microsoft Teams ของการจัดการงานในศูนย์ควบคุม Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4e60f-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4e60f-131">ไปที่ **Retail และ Commerce \> การจัดการงาน \> การรวมงานด้วย Microsoft Teams**</span><span class="sxs-lookup"><span data-stu-id="4e60f-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="4e60f-132">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="4e60f-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4e60f-133">ตั้งค่าตัวเลือก **เปิดใช้งานการรวมการจัดการงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="4e60f-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="4e60f-134">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4e60f-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="4e60f-135">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="4e60f-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="4e60f-136">คุณควรได้รับการแจ้งเตือนที่บ่งชี้ว่าชุดงานที่ชื่อ **การเตรียมใช้งาน Teams** จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="4e60f-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="4e60f-137">ไปที่ **การจัดการระบบ \> การสอบถาม \> ชุดงาน** และค้นหางานล่าสุดที่มีคำอธิบาย **การเตรียมใช้งาน Teams**</span><span class="sxs-lookup"><span data-stu-id="4e60f-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="4e60f-138">รอจนกว่างานนี้จะเสร็จสิ้นการรัน</span><span class="sxs-lookup"><span data-stu-id="4e60f-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="4e60f-139">รันงาน **CDX 1070** เพื่อเผยแพร่รหัสแผนและข้อมูลอ้างอิงร้านค้าไปยังเซิร์ฟเวอร์ Retail</span><span class="sxs-lookup"><span data-stu-id="4e60f-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e60f-140">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4e60f-140">Additional resources</span></span>

[<span data-ttu-id="4e60f-141">ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4e60f-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="4e60f-142">เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4e60f-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="4e60f-143">สํารอง Microsoft Teams จาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4e60f-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="4e60f-144">จัดการบทบาทผู้ใช้ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4e60f-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="4e60f-145">แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4e60f-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="4e60f-146">คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4e60f-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
