---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (03 กันยายน 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 3 กันยายน 2020
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 965f3ca859c601d26470038a889b0f21d2bdff5f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800128"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="164b3-103">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (3 กันยายน 2020)</span><span class="sxs-lookup"><span data-stu-id="164b3-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="164b3-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="164b3-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="164b3-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3504</span><span class="sxs-lookup"><span data-stu-id="164b3-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="164b3-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุน Lifecycle Services (LCS) สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="164b3-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="164b3-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะที่กำลังจะเกิดขึ้นใน Human Resources ดูที่ [ภาพรวมของ Dynamics 365 Human Resources 2019 เวฟการนำออกใช้ 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</span><span class="sxs-lookup"><span data-stu-id="164b3-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="164b3-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตสำหรับ Human Resources ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)</span><span class="sxs-lookup"><span data-stu-id="164b3-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="164b3-109">ในการเผยแพร่นี้</span><span class="sxs-lookup"><span data-stu-id="164b3-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="164b3-110">ตารางมิติทางการเงินเริ่มต้นและรูปแบบกล่องโต้ตอบใหม่ใน Human Resources (469495)</span><span class="sxs-lookup"><span data-stu-id="164b3-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="164b3-111">ขณะนี้รูปแบบใหม่สำหรับมิติทางการเงินจะพร้อมใช้งานในส่วนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="164b3-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="164b3-112">กำหนดตำแหน่งการดำเนินการ (แบบฟอร์ม: **HcmPositionActionDetail**)</span><span class="sxs-lookup"><span data-stu-id="164b3-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="164b3-113">รหัสรายได้ค่าจ้าง (แบบฟอร์ม: **PayrollEarningCode**)</span><span class="sxs-lookup"><span data-stu-id="164b3-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="164b3-114">รายการไม่ปรากฏในปฏิทินการลางานของบริษัทถ้าไม่ได้เปิดใช้งานการปรับปรุงปฏิทินการลางานและการขาดงาน (484406)</span><span class="sxs-lookup"><span data-stu-id="164b3-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="164b3-115">การเผยแพร่นี้แก้ไขปัญหาที่ไม่มีการแสดงรายการลางานในปฏิทินการลางานของบริษัท</span><span class="sxs-lookup"><span data-stu-id="164b3-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="164b3-116">ปัญหานี้จะเกิดขึ้นเฉพาะเมื่อไม่ได้เปิดใช้งานตัวเลือก **การปรับปรุงปฏิทินการลางงานและการขาดงาน** ของการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="164b3-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="164b3-117">ปัญหา BenefitPlanEmployeeEntity (467597)</span><span class="sxs-lookup"><span data-stu-id="164b3-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="164b3-118">การเผยแพร่นี้จะแก้ไขปัญหาที่เกิดขึ้นกับเอนทิตี้ **BenefitsPlanEmployee**</span><span class="sxs-lookup"><span data-stu-id="164b3-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="164b3-119">เมื่อมีการนำเข้าการลงทะเบียนของผู้ปฏิบัติงาน **รหัสความคุ้มครอง** และ **รหัสชนิดของแผน** มีการตั้งค่าอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="164b3-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="164b3-120">ปัญหานี้ทำให้แผนสวัสดิการของพนักงานแสดงอย่างไม่ถูกต้องในแบบฟอร์ม **แผนสวัสดิการของผู้ปฏิบัติงาน** และแบบฟอร์ม **การลงทะเบียนที่เปิด** ในระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="164b3-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="164b3-121">ผลลัพธ์ของไฟล์อิเล็กทรอนิกส์ 1094-C ไม่มีตัวอักษรใน XML (435190)</span><span class="sxs-lookup"><span data-stu-id="164b3-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="164b3-122">การเปลี่ยนแปลงนี้แก้ไขปัญหาที่เกิดขึ้นกับไฟล์เอาต์พุต1094-C ไม่มีอักขระที่จำเป็นเมื่อส่งไปที่ IRS</span><span class="sxs-lookup"><span data-stu-id="164b3-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="164b3-123">ตารางค่าตอบแทนผันแปรของพนักงานที่แม็ปกับแบบฟอร์มค่าตอบแทนคงที่ (476117)</span><span class="sxs-lookup"><span data-stu-id="164b3-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="164b3-124">การเปลี่ยนแปลงนี้จัดตำแหน่งฟิลด์ค่าตอบแทนคงที่ให้สอดคล้องกับแบบฟอร์มค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="164b3-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="164b3-125">ขณะนี้ฟิลด์ค่าตอบแทนผันแปรสามารถใช้งานกับแบบฟอร์มค่าตอบแทนผันแปรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="164b3-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="164b3-126">อนุญาตให้มีการร้องขอการลางานก่อนการลงทะเบียนถ้าชนิดการลางานนั้นมียอดคงเหลือต่ำสุดเป็นค่าลบ (469917)</span><span class="sxs-lookup"><span data-stu-id="164b3-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="164b3-127">การเปลี่ยนแปลงนี้ไม่อนุญาตให้ป้อนการร้องขอการลางานก่อนที่จะลงทะเบียนในแผน ถึงแม้ว่าการลงทะเบียนจะมียอดคงเหลือต่ำสุดที่เป็นค่าลบ</span><span class="sxs-lookup"><span data-stu-id="164b3-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="164b3-128">คุณสามารถป้อนหรือส่งคำขอได้เฉพาะเมื่อแผนเปิดใช้งานอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="164b3-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="164b3-129">เท็มเพลตเอกสารไม่ดาวน์โหลด (457279)</span><span class="sxs-lookup"><span data-stu-id="164b3-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="164b3-130">เมื่อคุณทำการเปลี่ยนแปลงนี้ คุณสามารถดาวน์โหลดเท็มเพลตเอกสารทั้งหมดได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="164b3-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="164b3-131">ข้อมูลจะแสดงเป็นส่วนหัวของคอลัมน์แทนแถวสำหรับฟิลด์อัตราการชำระค่าจ้างในรายงานแผนค่าตอบแทน (476077)</span><span class="sxs-lookup"><span data-stu-id="164b3-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="164b3-132">รายงานการวิเคราะห์จะแสดงข้อมูลที่ถูกต้องสำหรับ **อัตราการชำระค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="164b3-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="164b3-133">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="164b3-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="164b3-134">โปรแกรมประบุกต์ Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="164b3-134">Human Resources application in Teams</span></span>

<span data-ttu-id="164b3-135">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="164b3-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="164b3-136">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="164b3-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="164b3-137">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="164b3-137">For more information, see:</span></span>

- <span data-ttu-id="164b3-138">[การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 1</span><span class="sxs-lookup"><span data-stu-id="164b3-138">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="164b3-139">[แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="164b3-139">[Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="164b3-140">คุณลักษณะรุ่นพรีวิวของแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="164b3-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="164b3-141">**การแจ้งเตือน**: ผู้ส่งและผู้อนุมัติที่ส่งคำขอการลาหยุดจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="164b3-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="164b3-142">ผู้อนุมัติจะสามารถอนุมัติหรือปฏิเสธคำขอการลาหยุดได้</span><span class="sxs-lookup"><span data-stu-id="164b3-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="164b3-143">ผู้ส่งจะได้รับการแจ้งเตือนถ้าคำขอได้รับการอนุมัติหรือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="164b3-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="164b3-144">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="164b3-144">For more information, see:</span></span>
   - <span data-ttu-id="164b3-145">[การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2</span><span class="sxs-lookup"><span data-stu-id="164b3-145">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="164b3-146">[เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="164b3-146">[Enable notifications for the Human Resources app in Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="164b3-147">[เปิดหรือปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้แต่ละราย](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="164b3-147">[Turn Teams notifications on or off for individual users](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="164b3-148">[การแจ้งเตือนของ Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="164b3-148">[Teams notifications](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="164b3-149">[ดูปฏิทินการลางานของทีมของคุณ](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="164b3-149">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="164b3-150">**ปฏิทินการลาหยุดของผู้จัดการ**: ผู้จัดการจะสามารถดูการลาหยุดที่อนุมัติและที่ค้างอยู่สำหรับผู้ใต้บังคับบัญชาโดยตรงของตนในมุมมองปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="164b3-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="164b3-151">มุมมองนี้จะทำให้เข้าใจง่ายเมื่อสมาชิกในทีมของตนไม่มาทำงาน</span><span class="sxs-lookup"><span data-stu-id="164b3-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="164b3-152">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="164b3-152">For more information, see:</span></span>
   - <span data-ttu-id="164b3-153">[การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2</span><span class="sxs-lookup"><span data-stu-id="164b3-153">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="164b3-154">[ดูปฏิทินการลางานของทีมของคุณ](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="164b3-154">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="164b3-155">ตัวเลือกการตั้งค่าคอนฟิกเพื่อกำหนดตำแหน่งรายการงานที่กำหนดให้กับฉัน (477004)</span><span class="sxs-lookup"><span data-stu-id="164b3-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="164b3-156">ขณะนี้ตัวเลือกใหม่จะพร้อมใช้งานในการกำหนดตำแหน่งรายการของ **รายการงานที่กำหนดให้กับฉัน** ในคอลัมน์ทางด้านขวาของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="164b3-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="164b3-157">เมื่อมีการเปลี่ยนแปลงนี้ รายการงานและรายการสิ่งที่ต้องทำทั้งหมดแสดงในพื้นที่เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="164b3-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="164b3-158">เปิดใช้งานฟังก์ชันนี้โดยการเปิด **พรีวิว - การปรับปรุงประสบการณ์ของลำดับงาน** ในการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="164b3-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="164b3-159">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดคุณลักษณะพรีวิว ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)</span><span class="sxs-lookup"><span data-stu-id="164b3-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="164b3-160">คุณลักษณะนี้จะส่งเสริมตัวเลือกลำดับงานที่จะปรากฏในแบบฟอร์มการดำเนินการด้านบุคลากร</span><span class="sxs-lookup"><span data-stu-id="164b3-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="164b3-161">ตัวเลือกลำดับงานจะปรากฎในแท็บด่วนการดำเนินการเพื่อให้สามารถเข้าถึงได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="164b3-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="164b3-162">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="164b3-162">For more information, see:</span></span> 

- <span data-ttu-id="164b3-163">[การปรับปรุงประสบการณ์การใช้งานลำดับงานการจัดการองค์กรและบุคลากร](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) ในแผน Dynamics 365 2020 การนำออกใช้เวฟ 2</span><span class="sxs-lookup"><span data-stu-id="164b3-163">[Organization and personnel management workflow experience enhancements](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![รายการงานที่กำหนดให้กับฉัน](./media/hr-workflow-work-items-assigned-to-me.png)

![การเข้าถึงด่วนของรายการลำดับงาน](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="164b3-166">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="164b3-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="164b3-167">เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="164b3-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="164b3-168">เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="164b3-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="164b3-169">รหัสเหตุผลของการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="164b3-169">Benefits management reason codes</span></span>

<span data-ttu-id="164b3-170">รหัสเหตุผลของการจัดการสวัสดิการจะมีการรวมเข้ากับรหัสเหตุผลที่มีอยู่ใน Human Resources ในเร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="164b3-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="164b3-171">ถ้าคุณสร้างรหัสเหตุผลไว้ในการจัดการสวัสดิการที่มีอักขระเกินกว่า 15 ตัว คุณต้องเปลี่ยนชื่อของรหัสเหตุผลในแบบฟอร์ม **รหัสเหตุผล** ของการจัดการสวัสดิการเป็นอักขระ15 ตัวหรือน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="164b3-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="164b3-172">หลังจากที่คุณอัปเดตชื่อ รหัสเหตุผลจะปรากฏขึ้นภายใต้แบบฟอร์มรหัสเหตุผลที่มีอยู่ในการจัดการบุคลากร</span><span class="sxs-lookup"><span data-stu-id="164b3-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="164b3-173">การเปลี่ยนแปลงนี้จะพร้อมใช้งานในอนาคตและจะไม่มีผลกระทบต่อฟังก์ชันการทำงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="164b3-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="164b3-174">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="164b3-174">See also</span></span>

[<span data-ttu-id="164b3-175">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="164b3-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="164b3-176">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="164b3-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="164b3-177">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="164b3-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="164b3-178">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="164b3-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]