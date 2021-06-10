---
title: แม็ปทักษะ
description: คุณสามารถสร้างการค้นหาการแม็ปทักษะเพื่อค้นหาบุคคลที่เข้าเกณฑ์ใน Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076617"
---
# <a name="map-skills"></a><span data-ttu-id="809f0-103">แม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="809f0-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="809f0-104">คุณสามารถสร้างการค้นหาการแม็ปทักษะเพื่อค้นหาบุคคลที่เข้าเกณฑ์ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="809f0-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="809f0-105">การแม็ปทักษะจะค้นหาผลลัพธ์การส่งคืนเงื่อนไขที่คุณป้อนโดยค้นหาข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="809f0-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="809f0-106">ทักษะ</span><span class="sxs-lookup"><span data-stu-id="809f0-106">Skills</span></span>
- <span data-ttu-id="809f0-107">การศึกษา</span><span class="sxs-lookup"><span data-stu-id="809f0-107">Education</span></span>
- <span data-ttu-id="809f0-108">ประกาศนียบัตร</span><span class="sxs-lookup"><span data-stu-id="809f0-108">Certificates</span></span>
- <span data-ttu-id="809f0-109">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="809f0-109">Positions</span></span>
- <span data-ttu-id="809f0-110">ประสบการณ์โครงการ</span><span class="sxs-lookup"><span data-stu-id="809f0-110">Project experience</span></span>

<span data-ttu-id="809f0-111">ตัวอย่างเช่น คุณสามารถค้นหาบุคคลในองค์กรของคุณที่ได้รับ CPA ของตน</span><span class="sxs-lookup"><span data-stu-id="809f0-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="809f0-112">โพรไฟล์การแม็ปทักษะให้คุณสามารถค้นหาพนักงานหรือผู้สมัครปัจจุบันที่มีคุณสมบัติที่ตรงกับความต้องการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="809f0-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="809f0-113">เฉพาะผู้ปฏิบัติงาน ผู้สมัคร และผู้ติดต่อที่ถูกเลือกเพื่อรวมในการแม็ปทักษะค้นหาสามารถแสดงในรายการผลลัพธ์ของการแม็ปทักษะ หรือรวมอยู่ในโพรไฟล์ทักษะ</span><span class="sxs-lookup"><span data-stu-id="809f0-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="809f0-114">เมื่อต้องการรวมบุคคลในการค้นหาการแม็ปทักษะ ตั้งการเลือก **รวมในการแม็ปทักษะ** เป็น **ใช่** ในหน้าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="809f0-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="809f0-115">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="809f0-115">Worker</span></span><br>
> - <span data-ttu-id="809f0-116">พนักงาน</span><span class="sxs-lookup"><span data-stu-id="809f0-116">Employee</span></span><br>
> - <span data-ttu-id="809f0-117">ผู้ขอเปิด</span><span class="sxs-lookup"><span data-stu-id="809f0-117">Applicant</span></span><br>
> - <span data-ttu-id="809f0-118">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="809f0-118">Contacts</span></span><br>

<span data-ttu-id="809f0-119">เมื่อต้องการสร้างการแม็ปทักษะ ให้ไป **การพัฒนาพนักงาน > ลิงก์ > การแม็ปทักษะ**</span><span class="sxs-lookup"><span data-stu-id="809f0-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="809f0-120">เมื่อต้องการสร้างโปรไฟล์การแม็ปทักษะ ให้ไป **การพัฒนาพนักงาน > ลิงก์ > โปรไฟล์การแม็ปทักษะ**</span><span class="sxs-lookup"><span data-stu-id="809f0-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="809f0-121">การวิเคราะห์และการวิเคราะห์ช่องว่างของทักษะ</span><span class="sxs-lookup"><span data-stu-id="809f0-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="809f0-122">คุณสามารถสร้างการวิเคราะห์โปรไฟล์ทักษะเพื่อดูรายการของความสามารถของบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="809f0-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="809f0-123">คุณสามารถสร้างการวิเคราะห์ช่องว่างของทักษะเพื่อเปรียบเทียบทักษะของบุคคลและทักษะที่จำเป็นสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="809f0-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="809f0-124">เมื่อต้องการสร้างการวิเคราะห์ช่องว่าง ให้ไปที่ **การพัฒนาพนักงาน >ลิงค์>การวิเคราะห์ช่องว่างของทักษะ - บุคคล**</span><span class="sxs-lookup"><span data-stu-id="809f0-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="809f0-125">เมื่อต้องการสร้างการวิเคราะห์โปรไฟล์ทักษะ ให้ไป **การพัฒนาพนักงาน > ลิงก์ > การวิเคราะห์โปรไฟล์ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="809f0-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="809f0-126">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="809f0-126">See also</span></span>

[<span data-ttu-id="809f0-127">กำหนดค่าทักษะ</span><span class="sxs-lookup"><span data-stu-id="809f0-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="809f0-128">ป้อนทักษะ</span><span class="sxs-lookup"><span data-stu-id="809f0-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]