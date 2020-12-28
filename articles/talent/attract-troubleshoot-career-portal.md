---
title: ผู้ใช้ Attract ไม่สามารถสมัครงานจากพอร์ทัลการทำงานได้
description: หัวข้อนี้จะอธิบายถึงวิธีการแก้ไขปัญหาที่ผู้ใช้ Attract ไม่สามารถสมัครงานจากพอร์ทัลการทำงานได้
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462675"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="cef64-103">ผู้ใช้ Attract ไม่สามารถสมัครงานจากพอร์ทัลการทำงานได้</span><span class="sxs-lookup"><span data-stu-id="cef64-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="cef64-104">ออก</span><span class="sxs-lookup"><span data-stu-id="cef64-104">Issue</span></span>

<span data-ttu-id="cef64-105">ผู้ใช้ Attract ไม่สามารถสมัครงานจากพอร์ทัลการทำงานได้</span><span class="sxs-lookup"><span data-stu-id="cef64-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="cef64-106">เมื่อพวกเขาพยายามสมัครงานที่สร้างขึ้นใน Dynamics 365 Talent: Attract เบราว์เซอร์จะโหลดหน้าดังกล่าวอย่างต่อเนื่อง และไม่ทำการดำเนินการให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="cef64-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="cef64-107">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="cef64-107">Cause</span></span>

<span data-ttu-id="cef64-108">ปัญหานี้จะเกิดขึ้นเมื่อ Talent Relationship Team ไม่มีบทบาทผู้ใช้ Talent</span><span class="sxs-lookup"><span data-stu-id="cef64-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="cef64-109">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="cef64-109">Resolution</span></span>

<span data-ttu-id="cef64-110">กำหนดบทบาทผู้ใช้ Talent ให้กับ Talent Relationship Team</span><span class="sxs-lookup"><span data-stu-id="cef64-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="cef64-111">ล็อกอินไปยัง [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com) โดยใช้ข้อมูลประจำตัวของผู้ดูแลระบบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cef64-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="cef64-112">ผู้ดูแลระบบ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cef64-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="cef64-113">ผู้ดูแลระบบส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="cef64-113">Global admin</span></span>
   - <span data-ttu-id="cef64-114">ผู้ดูแลระบบ Power Platform</span><span class="sxs-lookup"><span data-stu-id="cef64-114">Power Platform admin</span></span>

2. <span data-ttu-id="cef64-115">ในบานหน้าต่างนำทาง ให้เลือก **สภาพแวดล้อมแล้ว** จากนั้นเลือกสภาพแวดล้อมที่จะกำหนดบทบาทผู้ใช้ Talent ให้กับ Talent Relationship Team</span><span class="sxs-lookup"><span data-stu-id="cef64-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![เลือกสภาพแวดล้อม](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="cef64-117">ในบานหน้าต่าง **สภาพแวดล้อม** ให้เลือก **URL ของสภาพแวดล้อม** และล็อกอินไปยังพอร์ทัลผู้ดูแลระบบของสภาพแวดล้อม (ตัวอย่างเช่น https:<orgname>crm.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="cef64-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="cef64-118">เลือก **การตั้งค่า** เลือก **ระบบ** แล้วเลือก **ความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="cef64-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![นำทางไปยังความปลอดภัย](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="cef64-120">เลือก **Teams**</span><span class="sxs-lookup"><span data-stu-id="cef64-120">Select **Teams**.</span></span>

   ![เลือก Teams](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="cef64-122">ค้นหา **Talent Relationship Team** ในกล่องค้นหา แล้วเลือกทีมจากผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="cef64-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="cef64-123">เลือก **MANAGE ROLES** จาก ribbon</span><span class="sxs-lookup"><span data-stu-id="cef64-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="cef64-124">ในกล่องโต้ตอบ **จัดการบทบาทของทีม** ให้เลือก **ผู้ใช้ Talent** จากรายการของบทบาทที่มีอยู่ แล้วเลือก **ตกลง** เพื่อใช้บทบาท</span><span class="sxs-lookup"><span data-stu-id="cef64-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![ใช้บทบาท](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="cef64-126">ทดสอบการเปลี่ยนแปลงของคุณ:</span><span class="sxs-lookup"><span data-stu-id="cef64-126">Test your changes:</span></span>

   1. <span data-ttu-id="cef64-127">ล็อกอินไปยังพอร์ทัลการทำงานจากหน้าต่างเบราเซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="cef64-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="cef64-128">สมัครงานจากพอร์ทัลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="cef64-128">Apply for the job from the career portal.</span></span> 