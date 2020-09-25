---
title: สร้างทีมโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการสร้างและการจัดการทีมโครงการ
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760674"
---
# <a name="create-a-project-team"></a><span data-ttu-id="54ead-103">สร้างทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="54ead-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54ead-104">เพื่อใช้บทบาทที่ได้ตั้งค่าไว้ก่อนหน้านี้ในโครงการ ผู้จัดการโครงการต้องเชื่อมโยงบทบาทกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="54ead-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="54ead-105">คุณสามารถกำหนดบทบาทได้หลายบทบาทสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="54ead-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="54ead-106">เพื่อป้องกันไม่ให้สับสน บทบาทเหล่านี้จะถูกกำหนดป้ายชื่อโดยอัตโนมัติระหว่างการจอง</span><span class="sxs-lookup"><span data-stu-id="54ead-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="54ead-107">ตัวอย่างเช่น ถ้าผู้จัดการโครงการต้องการวิศวกรซอฟต์แวร์สามคน บทบาทวิศวกรซอฟต์แวร์สามคน ที่มี **วิศวกรซอฟต์แวร์ 1**, **วิศวกรซอฟต์แวร์ 2** และ **วิศวกรซอฟต์แวร์ 3** เป็นป้ายชื่อของพวกเขา จะถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="54ead-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="54ead-108">ถ้าลักษณะบทบาทได้ถูกตั้งค่าไว้ก่อนหน้านี้สำหรับบทบาท จะถูกใช้เป็นตัวกรองข้อมูลในระหว่างการค้นหาทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="54ead-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="54ead-109">สามารถมีการเพิ่มลักษณะเพิ่มเติมตามที่จำเป็นเพื่อการปรับปรุงการค้นหาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="54ead-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="54ead-110">การตั้งค่ามุมมองยังสามารถกำหนดเองได้เพื่อให้มุมมองที่ดีขึ้นของความพร้อมของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="54ead-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="54ead-111">มีตัวเลือกเพื่อแสดงความพร้อมใช้งานรายชั่วโมง รายวัน รายสัปดาห์ รายเดือน รายไตรมาส และรายปี</span><span class="sxs-lookup"><span data-stu-id="54ead-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="54ead-112">นอกจากนี้ ยังมีตัวเลือกในการแสดงกำลังการผลิตที่พร้อมใช้งานและที่เหลือบนทรัพยากรได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="54ead-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="54ead-113">ตัวเลือกนี้มีประโยชน์สำหรับการจัดการเวลา เมื่อคุณกำลังประเมินเวลาว่างสำหรับกิจกรรมหรือความพร้อมของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="54ead-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="54ead-114">ผู้จัดการโครงการสามารถเลือกบทบาทได้บนหน้า แล้วจากนั้น ถ้ามีทรัพยากรที่พร้อมใช้งานที่เหมาะสมกับความต้องการ ให้เลือกเพื่อจองทรัพยากรเพื่อเติมเต็มบทบาท</span><span class="sxs-lookup"><span data-stu-id="54ead-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="54ead-115">หมายเหตุว่า ทรัพยากรไม่จำเป็นต้องถูกจอง ณ จุดนี้ในระหว่างระยะการวางแผน</span><span class="sxs-lookup"><span data-stu-id="54ead-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="54ead-116">เมื่อคุณสร้าง WBS คุณสามารถแทนที่บทบาทด้วยทรัพยากรที่จัดหาพนักงานไว้แล้วสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="54ead-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="54ead-117">ถ้าบทบาทถูกแทนที่ด้วยทรัพยากรที่จัดหาพนักงานไว้แล้วใน WBS การตั้งค่าทรัพยากรจะอัปเดตการแสดงรายการ และการจัดกำหนดการของทีมโครงการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="54ead-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="54ead-118">[![การแสดงรายการทีมโครงการที่รวมทั้งบทบาทและทรัพยากรจริง](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="54ead-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="54ead-119">ผู้จัดการโครงการมีตัวเลือกต่างๆ สำหรับการจองทรัพยากรสำหรับโครงการ เช่น **กำลังการผลิตที่เหลือ** **กำลังการผลิตทั้งหมด** **เปอร์เซ็นต์ของกำลังการผลิต**และ **ระบุชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="54ead-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="54ead-120">ตัวเลือกการสำรองเหล่านี้สามารถถูกยกเลิกได้ตลอดเวลา ถ้ามีการเปลี่ยนแปลงการกำหนดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="54ead-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="54ead-121">การจองสองชนิดนี้จะได้รับการสนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="54ead-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="54ead-122">**จองทรัพยากรแบบตายตัว** – การจองทรัพยากรได้รับอนุมัติและยืนยันว่าจะทำงานในการมีส่วนร่วมสำหรับระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="54ead-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="54ead-123">**จองทรัพยากรแบบไม่ตายตัว**– การจองทรัพยากรทีถูกตั้งค่าอย่างคร่าวให้ทำงานในการมีส่วนร่วมสำหรับระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="54ead-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="54ead-124">กระบวนงานต่อไปนี้อธิบายวิธีสร้างทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="54ead-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="54ead-125">สร้างทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="54ead-125">Create a project team</span></span>

1. <span data-ttu-id="54ead-126">ในหน้ารายการ **โครงการทั้งหมด** เลือกโครงการ และจากนั้นเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="54ead-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="54ead-127">ในแท็บ **ทีมโครงการและการจัดกำหนดการ** ในฟิลด์ **จัดกำหนดการวันที่สิ้นสุด** ให้ป้อนวันที่เริ่มต้นของกำหนดการบวกด้วยหนึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="54ead-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="54ead-128">ตัวอย่างเช่น ถ้าวันที่เริ่มต้นของกำหนดการ คือ 24 มิถุนายน 2017 (24/06/2017) ให้ป้อน **24/07/2017**</span><span class="sxs-lookup"><span data-stu-id="54ead-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="54ead-129">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="54ead-129">Select **Add**.</span></span>
4. <span data-ttu-id="54ead-130">ในบานหน้าต่าง **เพิ่มบทบาทไปยังโครงการ** ในฟิลด์ **บทบาท**เลือก **ผู้จัดการโครงการอาวุโส**</span><span class="sxs-lookup"><span data-stu-id="54ead-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="54ead-131">เลือก **ความสามารถที่ต้องการ**</span><span class="sxs-lookup"><span data-stu-id="54ead-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="54ead-132">ในหน้า **เลือกลักษณะ** ลักษณะที่คุณตั้งค่าไว้ก่อนหน้านี้สำหรับบทบาทผู้จัดการโครงการอาวุโส ถูกเลือกโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="54ead-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="54ead-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="54ead-133">Select **OK**.</span></span>
7. <span data-ttu-id="54ead-134">ในหน้า **เพิ่มบทบาทไปยังโครงการ** ในฟิลด์ **จำนวนทรัพยากร** ให้ป้อน **1**</span><span class="sxs-lookup"><span data-stu-id="54ead-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="54ead-135">ในฟิลด์ **ทรัพยากร** การค้นหาจะแสดงทรัพยากรทั้งหมดที่มีความสามารถที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54ead-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="54ead-136">เลือก **Daniel Goldschmidt**แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="54ead-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="54ead-137">บนหน้า **โครงการ** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="54ead-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="54ead-138">ในบานหน้าต่าง **เพิ่มบทบาทไปยังโครงการ** ในฟิลด์ **บทบาท** เลือก **สมาชิกทีมงาน**</span><span class="sxs-lookup"><span data-stu-id="54ead-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="54ead-139">ในฟิลด์ **จำนวนของทรัพยากร** ให้ป้อน **5**</span><span class="sxs-lookup"><span data-stu-id="54ead-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="54ead-140">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="54ead-140">Select **Create**.</span></span>
12. <span data-ttu-id="54ead-141">ในหน้า **โครงการ** เลือก **เติมทรัพยากรให้สมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="54ead-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="54ead-142">ตรวจสอบทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="54ead-142">Monitor project teams</span></span>
1. <span data-ttu-id="54ead-143">ในหน้า **โครงการทั้งหมด** เลือกลิงค์ **รหัสโครงการ** สำหรับโครงการ **โครงการการอัปเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="54ead-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="54ead-144">ใน FastTab **ทีมโครงการและการจัดกำหนดการ** ตรวจสอบว่า ทรัพยากรของโครงการที่ถูกแสดงรายการนั้นถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="54ead-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
