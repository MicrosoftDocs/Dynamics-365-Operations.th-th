---
title: สร้างโครงการใหม่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการสร้างทีมโครงการใหม่
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760673"
---
# <a name="create-a-new-project"></a><span data-ttu-id="fc05f-103">สร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="fc05f-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc05f-104">ดำเนินขั้นตอนต่อไปนี้เพื่อสร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="fc05f-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="fc05f-105">ในหน้า **การจัดการโครงการ** เลือก **โครงการใหม่** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc05f-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="fc05f-106">**ชนิดของโครงการ:** เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="fc05f-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="fc05f-107">**ชื่อโครงการ:** การอัปเกรด XYZ ระยะที่ 2</span><span class="sxs-lookup"><span data-stu-id="fc05f-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="fc05f-108">**กลุ่มโครงการ:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="fc05f-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="fc05f-109">**รหัสสัญญาโครงการ:** 00000002</span><span class="sxs-lookup"><span data-stu-id="fc05f-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="fc05f-110">เลือก **สร้างโครงการ**</span><span class="sxs-lookup"><span data-stu-id="fc05f-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="fc05f-111">มอบหมายทรัพยากรให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc05f-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="fc05f-112">ในหน้า **ผู้ปฏิบัติงาน** ในรายการ **ผู้ปฏิบัติงาน** เลือกเรกคอร์ดสำหรับผู้ปฏิบัติงานที่คุณตั้งค่าความสามารถให้ก่อนหน้านี้ และเปิดเรกคอร์ดผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="fc05f-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="fc05f-113">ในบานหน้าต่างการดำเนินการ บนแท็บ **โครงการ** ในกลุ่ม **การตั้งค่า** เลือก **มอบหมายโครงการ**</span><span class="sxs-lookup"><span data-stu-id="fc05f-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="fc05f-114">ในหน้า **การมอบหมายโครงการสำหรับการตรวจสอบความถูกต้องของทรัพยากร** บนแท็บ **โครงการ** ในฟิลด์ **เพิ่มโครงการไปยังโครงการที่เลือก** กรองข้อมูลในโครงการ **การอัปเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="fc05f-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="fc05f-115">ในบานหน้าต่าง **โครงการคงเหลือ** ให้เลือกโครงการ และจากนั้นคลิกปุ่มลูกศรเพื่อเพิ่มเข้าไปในบานหน้าต่า **โครงการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="fc05f-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="fc05f-116">นอกจากนี้คุณยังสามารถกำหนดประเภทสำหรับทรัพยากรตามที่คุณต้องการได้</span><span class="sxs-lookup"><span data-stu-id="fc05f-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="fc05f-117">ชนิดของประเภทเป็น **ต้นทุน** หรือ **รายได้** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fc05f-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="fc05f-118">ชนิดประเภทขึ้นอยู่กับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="fc05f-118">The category type is determined by your organization.</span></span> <span data-ttu-id="fc05f-119">ถ้าไม่มีประเภทที่กำหนดไว้สำหรับทรัพยากร Finance จะค้นหาประเภทเริ่มต้นจากราคาต่อชั่วโมงสำหรับต้นทุนและรายได้</span><span class="sxs-lookup"><span data-stu-id="fc05f-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="fc05f-120">ตั้งค่าทรัพยากรโครงการและลักษณะของบทบาท</span><span class="sxs-lookup"><span data-stu-id="fc05f-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="fc05f-121">ผู้จัดการโครงการสามารถใช้ฟังก์ชันการจัดหาทรัพยากรของโครงการ เพื่อสร้างบทบาทที่จำเป็นสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc05f-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="fc05f-122">สามารถใช้บทบาทเมื่อทรัพยากรที่ยืนยันยังคงไม่รู้จัก ในระหว่างการจองทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fc05f-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="fc05f-123">บทบาทสามารถถูกจองเป็นทรัพยากรที่วางแผนไว้ชั่วคราว เพื่อให้คุณสามารถดำเนินขั้นการวางแผนโครงการต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="fc05f-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="fc05f-124">[![ตัวอย่างของบทบาท](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc05f-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="fc05f-125">**สถานการณ์จำลอง:** Contoso ถูกจ้างให้ดำเนินโครงการเวลาและวัสดุให้เสร็จสมบูรณ์ ซึ่งได้อนุมัติแบบรายละเอียดการทำโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc05f-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="fc05f-126">ผู้จัดการโครงการหน้าใหม่จะยังคงดำเนินขอบเขตของโครงการให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc05f-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="fc05f-127">ในขณะนี้ผู้จัดการทรัพยากรกำลังระบุทรัพยากรที่เฉพาะเจาะจง ที่จะถูกจองให้กับงานในโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="fc05f-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="fc05f-128">เนื่องจากลักษณะสำคัญของโครงการ ผู้สนับสนุนโครงการร้องขอผู้จัดการโครงการอาวุโสเป็นหนึ่งในบทบาท</span><span class="sxs-lookup"><span data-stu-id="fc05f-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="fc05f-129">ผู้จัดการทรัพยากรต้องได้รับทรัพยากรใหม่ และกำหนดบทบาทในระบบ ในกรณีที่ผู้จัดการโครงการหน้าใหม่ต้องการข้อมูลทรัพยากรในระหว่างการวางแผนโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc05f-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="fc05f-130">ขั้นตอนต่อไปนี้แสดงวิธีที่ผู้จัดการทรัพยากรสามารถติดตั้งบทบาทผู้จัดการโครงการอาวุโสและเชื่อมโยงด้วยลักษณะทรัพยากรดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="fc05f-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="fc05f-131">ในภายหลัง บทบาทสามารถถูกใช้เพื่อค้นหาทรัพยากรที่มีอยู่ ซึ่งตรงกับความสามารถของทรัพยากรที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="fc05f-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="fc05f-132">ในหน้า **ตั้งค่าบทบาท** เลือก **ใหม่** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc05f-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="fc05f-133">**รหัสบทบาท:** ผู้จัดการโครงการอาวุโส</span><span class="sxs-lookup"><span data-stu-id="fc05f-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="fc05f-134">**คำอธิบาย:** ผู้จัดการโครงการอาวุโส</span><span class="sxs-lookup"><span data-stu-id="fc05f-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="fc05f-135">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="fc05f-135">Select **Create**.</span></span>
3. <span data-ttu-id="fc05f-136">เลือกบทบาท **ผู้จัดการโครงการอาวุโส** และเลือก **ตั้งค่าคอนฟิกลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="fc05f-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="fc05f-137">ในฟิลด์ **ชนิดของลักษณะ** ให้เลือก **ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="fc05f-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="fc05f-138">ในฟิลด์ **ลักษณะที่พร้อมใช้งาน** ให้ป้อนทักษะเพื่อค้นหา</span><span class="sxs-lookup"><span data-stu-id="fc05f-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="fc05f-139">ในฟิลด์ **ชนิดของลักษณะ** ให้เลือก **ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="fc05f-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="fc05f-140">ในฟิลด์ **ลักษณะที่พร้อมใช้งาน** ให้ป้อนชนิดใบรับรองเพื่อค้นหา</span><span class="sxs-lookup"><span data-stu-id="fc05f-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="fc05f-141">มอบหมายทรัพยากรโครงการให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc05f-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="fc05f-142">ในหน้า **โครงการทั้งหมด** เลือกโครงการ **การอัปเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="fc05f-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="fc05f-143">ในแท็บ **ทีมงานและการจัดกำหนดการโครงการ** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="fc05f-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="fc05f-144">ในฟิลด์ **บทบาท** ให้เลือก **สมาชิกทีม**</span><span class="sxs-lookup"><span data-stu-id="fc05f-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="fc05f-145">เลือก **จองจากปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="fc05f-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="fc05f-146">ในหน้า **ความพร้อมของทรัพยากร** เลือก **ดูการตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="fc05f-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="fc05f-147">ในหน้า **ปรับการตั้งค่ามุมมอง** ให้ป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc05f-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="fc05f-148">**รูปแบบสำหรับมุมมองช่วงวันที่:** วัน</span><span class="sxs-lookup"><span data-stu-id="fc05f-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="fc05f-149">**แสดงคำอธิบายความพร้อม:** ใช่</span><span class="sxs-lookup"><span data-stu-id="fc05f-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="fc05f-150">**แสดงกำลังการผลิตที่เหลือ:** ใช่</span><span class="sxs-lookup"><span data-stu-id="fc05f-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="fc05f-151">ในรายการของทรัพยากร ให้เลือกทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fc05f-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="fc05f-152">เลือก **จองทรัพยากรแบบตายตัว** และ **กำลังการผลิตที่สมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="fc05f-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="fc05f-153">กำหนดทรัพยากรต่างๆให้กับบทบาทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fc05f-153">Assign a resource to a default role</span></span>

<span data-ttu-id="fc05f-154">เพื่อช่วยให้ผู้จัดการโครงการหรือทรัพยากรสามารถดูรายละเอียดเพิ่มเติมเกี่ยวกับทรัพยากรที่สามารถถูกจองให้กับโครงการได้</span><span class="sxs-lookup"><span data-stu-id="fc05f-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="fc05f-155">คุณสามารถเชื่อมโยงบทบาทเริ่มต้นด้วยทรัพยากรที่มีอยู่ หรือทรัพยากรที่ถูกซื้อมาใหม่ </span><span class="sxs-lookup"><span data-stu-id="fc05f-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="fc05f-156">ตัวอย่างเช่น เมื่อ Daniel ถูกจ้าง เขามีประสบการณ์และทักษะในการเติมเต็มบทบาทนักวิเคราะห์ธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="fc05f-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="fc05f-157">ผู้จัดการทรัพยากรกำหนดบทบาทนี้เป็น บทบาทเริ่มต้นของ Daniel</span><span class="sxs-lookup"><span data-stu-id="fc05f-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="fc05f-158">ดังนั้น ผู้จัดการทรัพยากรได้เพิ่ม Daniel ลงในกลุ่มของนักวิเคราะห์ธุรกิจ ที่พร้อมทำงานในโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc05f-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="fc05f-159">ในระหว่างการจองทรัพยากร ผู้จัดการโครงการสามารถกรองทรัพยากรบทบาทที่พร้อมทำงานในโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc05f-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="fc05f-160">พวกเขาสามารถใช้ข้อมูลนี้เป็นเงื่อนไขหนึ่ง เมื่อพวกเขาทำการวิเคราะห์ตัดสินใจแบบหลายเงื่อนไข ในระหว่างการเติมสินค้าทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fc05f-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="fc05f-161">พวกเขายังสามารถเพิ่มลักษณะทรัพยากรอื่นๆ ลงในตัวกรองข้อมูล เพื่อค้นหาทรัพยากรที่มีทักษะเฉพาะ การศึกษา และประสบการณ์ สำหรับโครงการที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="fc05f-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="fc05f-162">**สถานการณ์จำลอง:** มีการเริ่มต้นโครงการที่ได้รับอนุมัติ และมีการจองบทบาทผู้จัดการโครงการอาวุโสเป็นทรัพยากรที่วางแผนไว้ในระหว่างขั้นตอนการวางแผนโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc05f-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="fc05f-163">ในขณะนี้ ผู้จัดการทรัพยากรได้รับทรัพยากรเพื่อเติมเต็มบทบาทผู้จัดการโครงการอาวุโสแล้ว</span><span class="sxs-lookup"><span data-stu-id="fc05f-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="fc05f-164">ในหน้า **รายการทรัพยากร** ให้เลือก **Daniel Goldschmidt**</span><span class="sxs-lookup"><span data-stu-id="fc05f-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="fc05f-165">ในหน้า **บทบาททรัพยากร** เลือก **ใหม่** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc05f-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="fc05f-166">**มีผลบังคับใช้:** ป้อนวันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="fc05f-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="fc05f-167">**วันหมดอายุ:** ป้อน **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="fc05f-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="fc05f-168">**บทบาท:** ป้อน **ผู้จัดการโครงการอาวุโส**</span><span class="sxs-lookup"><span data-stu-id="fc05f-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="fc05f-169">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fc05f-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="fc05f-170">บนแท็บ **ความสามารถ** ให้เพิ่มทักษะ **ProjectMgmt** และใบรับรอง **PMP**</span><span class="sxs-lookup"><span data-stu-id="fc05f-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
