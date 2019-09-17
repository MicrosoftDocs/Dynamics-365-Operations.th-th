---
title: สร้างทีมงานการจ้างงานโดยการใช้ Dynamics 365 for Talent - Onboard
description: หัวข้อนี้จะอธิบายวิธีใช้แอป Microsoft Dynamics 365 for Talent - Onboard เพื่อสร้างทีมงานการเตรียมความพร้อม
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 996fc42881ce708992614c58877927e03bbf78bf
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731660"
---
# <a name="create-a-hiring-team-by-using-dynamics-365-for-talent-onboard"></a><span data-ttu-id="73a9e-103">สร้างทีมงานการจ้างงานโดยการใช้ Dynamics 365 for Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="73a9e-103">Create a hiring team by using Dynamics 365 for Talent: Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="73a9e-104">ใน Microsoft Dynamics 365 for Talent: Onboard คุณสามารถสร้างทีมงานการจ้างงานได้</span><span class="sxs-lookup"><span data-stu-id="73a9e-104">In Microsoft Dynamics 365 for Talent: Onboard, you can create hiring teams.</span></span> <span data-ttu-id="73a9e-105">จากนั้นคุณสามารถกำหนดคู่มือและเท็มเพลตการเตรียมความพร้อมให้กับแต่ละทีมได้</span><span class="sxs-lookup"><span data-stu-id="73a9e-105">You can then assign onboarding guides and templates to each team.</span></span>

## <a name="create-a-hiring-team"></a><span data-ttu-id="73a9e-106">สร้างทีมงานการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-106">Create a hiring team</span></span>

1. <span data-ttu-id="73a9e-107">บนเมนูด้านซ้าย ให้เลือก **ทีมงาน**</span><span class="sxs-lookup"><span data-stu-id="73a9e-107">On the left menu, select **Teams**.</span></span>
2. <span data-ttu-id="73a9e-108">ภายใต้ **ทีมงาน** ให้เลือก **เพิ่ม** ไทล์ (เครื่องหมายบวก \[**+**\])</span><span class="sxs-lookup"><span data-stu-id="73a9e-108">Under **Teams**, select the **Add** (plus sign \[**+**\]) tile.</span></span>
3. <span data-ttu-id="73a9e-109">ในกล่องโต้ตอบ **สร้างทีมงานใหม่** ภายใต้ **ชื่อทีมงาน** ให้ป้อนชื่อสำหรับทีมงานการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-109">In the **Create a new team** dialog box, under **Team name**, enter a name for the hiring team.</span></span>

    ![[การสร้างทีมงานใหม่ใน Onboard] (./media/onboard-create-team.png)](./media/onboard-create-team.png)

4. <span data-ttu-id="73a9e-111">ภายใต้ **เลือกสมาชิกทีมงาน** ป้อนชื่อหรือที่อยู่อีเมลของสมาชิกทีมงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="73a9e-111">Under **Choose team members**, enter the name or email address of each team member.</span></span>

    <span data-ttu-id="73a9e-112">ถ้าต้องการลบสมาชิกทีมงาน ให้เลือก **X** ที่ปรากฏถัดจากชื่อภายใต้กล่อง</span><span class="sxs-lookup"><span data-stu-id="73a9e-112">To remove team members, select the **X** that appears next to their name under the box.</span></span>

5. <span data-ttu-id="73a9e-113">เมื่อต้องการส่งอีเมลถึงสมาชิกทีมงานใหม่ ให้เปิดใช้งานตัวเลือก **ส่งอีเมลไปยังสมาชิกใหม่**</span><span class="sxs-lookup"><span data-stu-id="73a9e-113">To email new team members, turn on the **Send an email to the new members** option.</span></span>
6. <span data-ttu-id="73a9e-114">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="73a9e-114">Select **Create**.</span></span>
7. <span data-ttu-id="73a9e-115">ถ้าคุณระบุว่าคุณต้องการส่งอีเมลถึงสมาชิกทีมงานใหม่ ให้แก้ไขอีเมลในกล่องโต้ตอบถัดไป แล้วเลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="73a9e-115">If you indicated that you want to email new team members, edit the email in the next dialog box, and then select **Done**.</span></span>

## <a name="assign-onboarding-guides-to-a-hiring-team"></a><span data-ttu-id="73a9e-116">กำหนดคู่มือการเตรียมความพร้อมให้กับทีมงานการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-116">Assign onboarding guides to a hiring team</span></span>

1. <span data-ttu-id="73a9e-117">บนเมนูด้านซ้าย ให้เลือก **ทีมงาน**</span><span class="sxs-lookup"><span data-stu-id="73a9e-117">On the left menu, select **Teams**.</span></span>
2. <span data-ttu-id="73a9e-118">เลือกทีมงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-118">Select the team.</span></span>
3. <span data-ttu-id="73a9e-119">บนแท็บ **คู่มือ** เลือก **เพิ่มคู่มือ**</span><span class="sxs-lookup"><span data-stu-id="73a9e-119">On the **Guides** tab, select **Add guides**.</span></span>

    ![[การเพิ่มคู่มือการเตรียมควาพร้อมให้กับทีมงาน] (./media/onboard-add-guides-to-team.png)](./media/onboard-add-guides-to-team.png)

4. <span data-ttu-id="73a9e-121">เลือกกล่องกาเครื่องหมายสำหรับแต่ละคู่มือการเตรียมควาพร้อมที่คุณต้องการกำหนดให้กับทีมงาน แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="73a9e-121">Select the check box for each onboarding guide that you want to assign to the team, and then select **Add**.</span></span>

    ![[<span data-ttu-id="73a9e-122">การเลือกคู่มือการเตรียมควาพร้อมเพื่อเพิ่มให้กับทีมงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-122">Selecting the onboarding guides to add to the team</span></span>](./media/onboard-select-guides.png)](./media/onboard-select-guides.png)

## <a name="assign-onboarding-templates-to-a-hiring-team"></a><span data-ttu-id="73a9e-123">กำหนดเท็มเพลตการเตรียมความพร้อมให้กับทีมงานการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-123">Assign onboarding templates to a hiring team</span></span>

1. <span data-ttu-id="73a9e-124">บนเมนูด้านซ้าย ให้เลือก **ทีมงาน**</span><span class="sxs-lookup"><span data-stu-id="73a9e-124">On the left menu, select **Teams**.</span></span>
2. <span data-ttu-id="73a9e-125">เลือกทีมงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-125">Select the team.</span></span>
3. <span data-ttu-id="73a9e-126">บนแท็บ **เท็มเพลต** เลือก **เพิ่มเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="73a9e-126">On the **Templates** tab, select **Add templates**.</span></span>

    ![[<span data-ttu-id="73a9e-127">การเพิ่มเท็มเพลตให้กับทีมงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-127">Adding templates to a team</span></span>](./media/onboard-add-templates-to-team.png)](./media/onboard-add-templates-to-team.png)

4. <span data-ttu-id="73a9e-128">เลือกกล่องกาเครื่องหมายสำหรับแต่ละเท็มเพลตที่คุณต้องการกำหนดให้กับทีมงาน แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="73a9e-128">Select the check box for each template that you want to assign to the team, and then select **Add**.</span></span>

    ![[<span data-ttu-id="73a9e-129">การเลือกเท็มเพลตเพื่อเพิ่มให้กับทีมงาน</span><span class="sxs-lookup"><span data-stu-id="73a9e-129">Selecting the templates to add to the team</span></span>](./media/onboard-select-templates.png)](./media/onboard-select-templates.png)

### <a name="see-also"></a><span data-ttu-id="73a9e-130">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="73a9e-130">See also</span></span>

- [<span data-ttu-id="73a9e-131">ลองหรือซื้อแอป Onboard</span><span class="sxs-lookup"><span data-stu-id="73a9e-131">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="73a9e-132">มีอะไรใหม่</span><span class="sxs-lookup"><span data-stu-id="73a9e-132">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="73a9e-133">บันทึกย่อประจำรุ่น</span><span class="sxs-lookup"><span data-stu-id="73a9e-133">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="73a9e-134">รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="73a9e-134">Get support</span></span>](./talent-support.md)
