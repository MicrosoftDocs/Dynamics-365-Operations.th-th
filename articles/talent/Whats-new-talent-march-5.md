---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent (5 มีนาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e4ad32ef71c87f52e59959d80c21ae7fcd6d6524
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/12/2019
ms.locfileid: "949816"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a><span data-ttu-id="bd032-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent (5 มีนาคม 2019)</span><span class="sxs-lookup"><span data-stu-id="bd032-103">What's new or changed in Dynamics 365 for Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd032-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงใน Talent อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bd032-104">This topic describes features that are either new or changed in Talent</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="bd032-105">การเปลี่ยนแปลงใน Attract</span><span class="sxs-lookup"><span data-stu-id="bd032-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="bd032-106">การขยายชุดตัวเลือกใน Attract</span><span class="sxs-lookup"><span data-stu-id="bd032-106">Extending option sets in Attract</span></span>

<span data-ttu-id="bd032-107">ใน Attract มีฟิลด์หลายฟิลด์ที่เป็นชุดตัวเลือกภายใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="bd032-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="bd032-108">ความสามารถใหม่ได้ถูกนำมาใช้ในการขยายชุดตัวเลือก โดยเริ่มต้นด้วยฟิลด์เหตุผล **การปฏิเสธ** ฟิลด์ **ชนิดการจ้างงาน** และฟิลด์ **ชนิดของอายุงาน**</span><span class="sxs-lookup"><span data-stu-id="bd032-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd032-109">ฟังก์ชันการโพสต์งานไปยัง LinkedIn จำเป็นต้องมีการใช้ฟิลด์ **ชนิดการจ้างงาน** และฟิลด์ **ชนิดของอายุงาน** ในหน้า **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="bd032-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="bd032-110">ค่าเริ่มต้นในฟิลด์เหล่านี้ได้รับการสนับสนุน โดย LinkedIn และจะแสดงขึ้นเมื่อมีการโพสต์งาน</span><span class="sxs-lookup"><span data-stu-id="bd032-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="bd032-111">ถ้าคุณกำลังโพสต์งานไปยัง LinkedIn และคุณปรับเปลี่ยนค่าชุดตัวเลือกที่มีอยู่สำหรับฟิลด์เหล่านี้ งานจะยังคงโพสต์ แต่ LinkedIn จะไม่แสดงค่า **ชนิดการจ้างงาน** และ **ชนิดของอายุงาน** แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="bd032-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="bd032-112">การเปลี่ยนแปลงในการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="bd032-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="bd032-113">การแสดงตัวอย่างแบบส่วนตัวสำหรับทีมงานเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="bd032-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="bd032-114">ขณะนี้ คุณสามารถแบ่งปันและทำงานร่วมกันได้อย่างง่ายดายบนเท็มเพลตทั่วทั้งองค์กรทั้งหมดของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd032-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="bd032-115">สำหรับข้อมูลเพิ่มเติม ดู [แบ่งปันแนวทางปฏิบัติทั่วทั้งองค์กรของคุณโดยใช้ทีมงานเตรียมความพร้อม](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams)</span><span class="sxs-lookup"><span data-stu-id="bd032-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="bd032-116">การแสดงตัวอย่างแบบส่วนตัวสำหรับตัวยึดตำแหน่งผู้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="bd032-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="bd032-117">คุณสามารถเพิ่มเท็มเพลตของคุณได้ โดยการกำหนดกิจกรรมให้กับบทบาท แทนที่จะเป็นแต่ละบุคคล</span><span class="sxs-lookup"><span data-stu-id="bd032-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="bd032-118">จากนั้น บทบาทจะถูกกำหนดให้กับแต่ละบุคคลในขณะที่สร้างคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bd032-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="bd032-119">สำหรับข้อมูลเพิ่มเติม ดู [ลดขั้นตอนซ้ำซ้อนการจัดการคู่มือตามการกำหนดกิจกรรมให้กับบทบาท](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles)</span><span class="sxs-lookup"><span data-stu-id="bd032-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="bd032-120">การเปลี่ยนแปลงใน Core HR</span><span class="sxs-lookup"><span data-stu-id="bd032-120">Changes in Core HR</span></span>
<span data-ttu-id="bd032-121">**สร้าง 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="bd032-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="bd032-122">ตั้งค่าคอนฟิกลำดับงานให้อนุมัติอัตโนมัติ หรือทำตามลำดับงานเมื่อผู้จัดการฝ่าย HR หรือสายงาน ส่งหรือปรับปรุงคำขอการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="bd032-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="bd032-123">มีการเพิ่มเงื่อนไขลำดับงานใหม่เพื่ออนุญาตให้คำขอลางานได้รับอนุมัติโดยอัตโนมัติ ถ้าถูกส่งโดยผู้จัดการของพนักงาน หรือโดย HR</span><span class="sxs-lookup"><span data-stu-id="bd032-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="bd032-124">วิธีหนึ่งที่จะได้รับการอนุมัติโดยอัตโนมัตินี้ในลำดับงานคือ การเปิดใช้งานการดำเนินการอัตโนมัติในการอนุมัติลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd032-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="bd032-125">เงื่อนไขที่ได้ถูกเพิ่มประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="bd032-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="bd032-126">ถูกส่งโดย - ใช้เพื่อประเมินรหัสผู้ใช้ระบบของผู้ใช้ที่ส่งคำขอไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd032-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="bd032-127">ถูกส่งในนามของ - ใช้เพื่อประเมิน ถ้ามีการส่งคำขอลางานในนามของผู้ปฏิบัติงานที่เกี่ยวข้องกับคำขอ</span><span class="sxs-lookup"><span data-stu-id="bd032-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="bd032-128">ถูกส่งโดยทรัพยากรบุคคล - ใช้เพื่อประเมิน หากผู้ใช้ระบบที่ส่งคำขอไปยังลำดับงานอยู่ในบทบาทของฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="bd032-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="bd032-129">ถูกส่งโดยผู้จัดการ - ใช้เพื่อประเมินว่าผู้ใช้ที่ส่งคำขอลางานไปที่ลำดับงานคือ ผู้จัดการลำดับชั้นของรายการของผู้ปฏิบัติงานที่เกี่ยวข้องกับคำขอหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bd032-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="bd032-130">เปิดใช้งานค่าตอบแทนคงที่ของพนักงานสำหรับการมอบหมายตำแหน่งในอนาคต</span><span class="sxs-lookup"><span data-stu-id="bd032-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="bd032-131">เป็นเรื่องปกติสำหรับพนักงานที่จะเข้าร่วมกับองค์กรที่มีวันที่เริ่มต้นในอนาคต</span><span class="sxs-lookup"><span data-stu-id="bd032-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="bd032-132">การเปลี่ยนแปลงนี้เปิดใช้งานการกำหนดค่าตอบแทนคงที่สำหรับพนักงานที่มีการมอบหมายตำแหน่งงานในอนาคต</span><span class="sxs-lookup"><span data-stu-id="bd032-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="bd032-133">ฟิลด์ค่าจ้างของตำแหน่งจะว่างเปล่า เมื่อแก้ไขตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="bd032-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="bd032-134">ด้วยการเปลี่ยนแปลงนี้ เมื่อมีการร้องขอการเปลี่ยนแปลงไปยังตำแหน่งที่มีอยู่ ในขณะนี้ ฟิลด์ค่าจ้างจะตั้งค่าเริ่มต้นจะเป็นค่าปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bd032-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="bd032-135">การแก้ไขปัญหาบักเบ็ดเตล็ดอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="bd032-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="bd032-136">การแก้ไขบักรองอื่นๆ ถูกรวมอยู่กับรุ่นนี้</span><span class="sxs-lookup"><span data-stu-id="bd032-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="bd032-137">อัพเกรดเป็น Common Data Service</span><span class="sxs-lookup"><span data-stu-id="bd032-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="bd032-138">เวลาสิ้นสุดการอัพเกรดเป็น Common Data Service ใกล้จะมาถึงเร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="bd032-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="bd032-139">ล็อกอินไปยังศูนย์การจัดการ PowerApps เพื่อตรวจสอบว่า ฐานข้อมูลของคุณต้องได้รับการอัพเกรดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bd032-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="bd032-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกำหนดเวลาสิ้นสุดและขั้นตอนที่จำเป็นในการอัพเกรด ดู [อัพเกรดเป็น Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds)</span><span class="sxs-lookup"><span data-stu-id="bd032-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="bd032-141">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="bd032-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="bd032-142">ความปลอดภัยของค่าตอบแทนขั้นสูง (คงที่และผันแปร)</span><span class="sxs-lookup"><span data-stu-id="bd032-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="bd032-143">ในหลายองค์กร ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถเข้าถึงได้เฉพาะเรกคอร์ดค่าตอบแทนบางรายการ เช่น เรกคอร์ดสำหรับผู้บริหารหรือพนักงานตามภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="bd032-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="bd032-144">ด้วยการเปลี่ยนแปลงนี้ คุณสามารถจัดการและรักษาแผนค่าตอบแทนสำหรับกลุ่มพนักงานอื่นๆ ในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="bd032-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="bd032-145">แผนคงที่และผันแปรสามารถถูกกำหนด security role ซึ่งจะกำหนดการเข้าถึงแผนและข้อมูลพนักงานที่เกี่ยวข้องกับแผน เช่น เรกคอร์ดเงินโบนัสหรือเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="bd032-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="bd032-146">เฉพาะบทบาทที่มีการเข้าถึงที่กำหนด จะสามารถดำเนินการค่าตอบแทนสำหรับพนักงานเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="bd032-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24"></a><span data-ttu-id="bd032-147">แพลตฟอร์ม update 24</span><span class="sxs-lookup"><span data-stu-id="bd032-147">Platform update 24</span></span>
<span data-ttu-id="bd032-148">สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการอัพเดตแพลตฟอร์ม 24 ดู [มีอะไรใหม่ หรือเปลี่ยนแปลงใน Finance and Operations การอัพเดตแพลตฟอร์ม 24 (มีนาคม 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24)</span><span class="sxs-lookup"><span data-stu-id="bd032-148">For additional details about Platform update 24, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
