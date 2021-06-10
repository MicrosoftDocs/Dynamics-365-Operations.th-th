---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (08 กรกฎาคม 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 8 กรกฏาคม 2020
author: andreabichsel
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 433eef4f11f385e85648d137521996a47a8ffd7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053934"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="665bd-103">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (8 กรกฎาคม 2020)</span><span class="sxs-lookup"><span data-stu-id="665bd-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="665bd-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="665bd-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="665bd-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3382</span><span class="sxs-lookup"><span data-stu-id="665bd-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="665bd-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="665bd-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="665bd-107">การล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="665bd-107">Database logging</span></span>

<span data-ttu-id="665bd-108">การล็อกฐานข้อมูลจะช่วยให้คุณสามารถกำหนดตารางและฟิลด์ที่จะตรวจสอบได้</span><span class="sxs-lookup"><span data-stu-id="665bd-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="665bd-109">นอกจากนี้ยังช่วยให้คุณสามารถกำหนดเหตุการณ์ที่ควรทริกเกอร์การติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="665bd-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="665bd-110">คุณสามารถใช้ความสามารถในการบันทึกฐานข้อมูลเพื่อดูการเปลี่ยนแปลงเหล่านี้เมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="665bd-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="665bd-111">สำหรับข้อมูลเพิ่มเติมให้ ดูที่ [ตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล](hr-admin-database-logging.md)</span><span class="sxs-lookup"><span data-stu-id="665bd-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="665bd-112">ตั้งค่าคอนฟิกชื่อของระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="665bd-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="665bd-113">ใน **พารามิเตอร์ทรัพยากรบุคคล** คุณสามารถเปลี่ยนชื่อของพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน** เป็น **ระบบบริการตนเอง** ได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="665bd-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="665bd-114">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปลี่ยนชื่อพื้นที่ทำงานระบบบริการตนเองของพนักงาน](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="665bd-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="665bd-115">การจัดการสวัสดิการเปิดการเข้าถึงการลงทะเบียนนอกรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="665bd-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="665bd-116">การนำออกใช้นี้ช่วยแก้ไขจุดบกพร่องที่พนักงานสามารถเข้าถึงการลงทะเบียนแบบเปิดของสวัสดิการภายนอกรอบระยะเวลาการลงทะเบียน หรือโดยไม่มีเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="665bd-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="665bd-117">ด้วยเหตุนี้ ถ้าคุณต้องการสาธิตการลงทะเบียนแบบเปิดในระบบบริการตนเองของพนักงาน คุณต้องปรับปรุงวันที่ของการลงทะเบียนแบบเปิดเป็นวันนี้ (หรือก่อนหน้านี้) เพื่อให้สามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="665bd-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="665bd-118">คุณสามารถเปลี่ยนการตั้งค่านี้ภายใต้ **การจัดการสวัสดิการ > รอบระยะเวลาของกฎและตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="665bd-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="665bd-119">การยืนยันการลงทะเบียนของพนักงานทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="665bd-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="665bd-120">ขณะนี้คุณสามารถส่งอีเมลไปยังพนักงานได้ หลังจากที่พวกเขาทำการเลือกผลประโยชน์ของพวกเขาเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="665bd-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="665bd-121">คุณสามารถส่งข้อความเริ่มต้น หรือใช้เท็มเพลตอีเมลขององค์กรได้</span><span class="sxs-lookup"><span data-stu-id="665bd-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="665bd-122">การตั้งค่าเหล่านี้อยู่ภายใต้ **พารามิเตอร์ทรัพยากรบุคคล > การจัดการสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="665bd-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="665bd-123">การลางานที่ยกเลิกยังคงแสดงอยู่ในเวลาที่กำลังจะเกิดขึ้นในพื้นที่ทำงานของบุคคล (441358)</span><span class="sxs-lookup"><span data-stu-id="665bd-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="665bd-124">การลางานที่ยกเลิกไม่แสดงอีกต่อไปเป็นการหยุดพักที่กำลังจะมาถึงในบัตรลางานในพื้นที่ทำงาน **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="665bd-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="665bd-125">ไม่สามารถใช้คุณสมบัติเอนทิตีของแผนกในเอนทิตี PositionV2 (456486)</span><span class="sxs-lookup"><span data-stu-id="665bd-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="665bd-126">ขณะนี้คุณสามารถเพิ่มแผนกได้โดยไม่มีการสร้างความสัมพันธ์ที่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="665bd-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="665bd-127">PayrollWorkerEnrolledBenefitDetailEntity ควรใช้เฉพาะฟิลด์ที่คำนวณได้สำหรับแผนการเกษียณอายุ (459779)</span><span class="sxs-lookup"><span data-stu-id="665bd-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="665bd-128">เมื่อส่งออกเอนทิตี **PayrollWorkerEnrolledBenefitDetailEntity** การส่งออกจะกำหนดว่าควรจะใช้ฟิลด์ที่คำนวณได้ตามตารางอัตรา หรือใช้ฟิลด์ **ContributionAmountCur** บนตารางสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="665bd-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="665bd-129">ตรรกะที่ใช้โดยเอนทิตีข้อมูลจะใช้ตารางอัตราในสถานการณ์ที่แอปพลิเคชันตามปกติไม่ใช้</span><span class="sxs-lookup"><span data-stu-id="665bd-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="665bd-130">ตรรกะนี้ทำให้เกิดการส่งออกเอนทิตี้เพื่อส่งคืนค่าศูนย์สำหรับคอลัมน์นี้ เนื่องจากไม่มีตารางอัตราการคำนวณและผลิตภัณฑ์ไม่อนุญาตให้ลูกค้าระบุ</span><span class="sxs-lookup"><span data-stu-id="665bd-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="665bd-131">การแปลที่สับสนในภาษาเช็กในการบริหารบุคลากรและระบบบริการตนเองของพนักงาน (400276)</span><span class="sxs-lookup"><span data-stu-id="665bd-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="665bd-132">การนำออกใช้นี้แก้ไขการแปลสำหรับ **ไดเรกทอรีของบริษัท** **หลักสูตรที่ลงทะเบียนถัดไป** **งาน** และ **ตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="665bd-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="665bd-133">ตาราง WorkCalendarEmployment ไม่ได้เปิดใช้งานฟิลด์ระบบที่สร้างและที่แก้ไข (460171)</span><span class="sxs-lookup"><span data-stu-id="665bd-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="665bd-134">ขณะนี้มีการเปิดใช้งานฟิลด์ระบบที่สร้างและที่แก้ไขบนตาราง **WorkCalendarEmployment** ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="665bd-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="665bd-135">ข้อยกเว้นการอ้างอิง Null สำหรับการจ้างงานและเพิ่มรายละเอียดสำหรับพนักงานในอนาคต (455475)</span><span class="sxs-lookup"><span data-stu-id="665bd-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="665bd-136">การนำออกใช้นี้จะแก้ไขข้อผิดพลาด (การอ้างอิง null) ในรายการพนักงานที่มีประสิทธิภาพ เมื่อคุณจ้างงานพนักงานโดยใช้ตัวเลือกเพื่อ **จ้างและเพิ่มรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="665bd-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="665bd-137">การเปลี่ยนแปลงที่เกิดขึ้นในเอนทิตีของผู้ปฏิบัติงาน Dataverse ไม่ได้แสดงในทรัพยากรบุคคล (455652)</span><span class="sxs-lookup"><span data-stu-id="665bd-137">Changes made in the Dataverse Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="665bd-138">การเปลี่ยนแปลงที่เกิดขึ้นกับฟิลด์ต่อไปนี้ในเอนทิตี **ผู้ปฏิบัติงาน** ใน Dataverse จะแสดงขึ้นในทรัพยากรบุคคลในขณะนี้:</span><span class="sxs-lookup"><span data-stu-id="665bd-138">Changes made to the following fields in the **Worker** entity in Dataverse will now show up in Human Resources:</span></span>

- <span data-ttu-id="665bd-139">**ทำงานจากบ้าน**</span><span class="sxs-lookup"><span data-stu-id="665bd-139">**Works from home**</span></span>
- <span data-ttu-id="665bd-140">**วันที่ของอายุงาน**</span><span class="sxs-lookup"><span data-stu-id="665bd-140">**Seniority date**</span></span>
- <span data-ttu-id="665bd-141">**วันที่ครบรอบปี**</span><span class="sxs-lookup"><span data-stu-id="665bd-141">**Anniversary date**</span></span>
- <span data-ttu-id="665bd-142">**วันที่จ้างงานเดิม**</span><span class="sxs-lookup"><span data-stu-id="665bd-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="665bd-143">ระดับค่าตอบแทนที่ถูกต้องไม่ใช่ค่าเริ่มต้นตามงานที่กำหนดให้กับตำแหน่ง (394136)</span><span class="sxs-lookup"><span data-stu-id="665bd-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="665bd-144">ด้วยการเปลี่ยนแปลงนี้ ระดับค่าตอบแทนที่ถูกต้องจะขึ้นอยู่กับเรกคอร์ด **วันที่มีผลบังคับใช้** สำหรับ **รายละเอียดตำแหน่ง** และ **วันที่เริ่มต้น** ของ **การกำหนดแผนค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="665bd-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="665bd-145">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="665bd-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="665bd-146">ฟิลด์บังคับ</span><span class="sxs-lookup"><span data-stu-id="665bd-146">Mandatory fields</span></span> 

<span data-ttu-id="665bd-147">ขณะนี้คุณสามารถทำให้ฟิลด์บังคับโดยใช้ความสามารถในการตั้งค่าส่วนบุคคลของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="665bd-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="665bd-148">ลักษณะการทำงานนี้จำเป็นต้องใช้ **มุมมองที่บันทึกไว้**</span><span class="sxs-lookup"><span data-stu-id="665bd-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="665bd-149">โปรแกรมประบุกต์ Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="665bd-149">Human Resources application in Teams</span></span>

<span data-ttu-id="665bd-150">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="665bd-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="665bd-151">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="665bd-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="665bd-152">สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](./hr-admin-teams-leave-app.md)</span><span class="sxs-lookup"><span data-stu-id="665bd-152">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="665bd-153">เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="665bd-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="665bd-154">เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="665bd-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="665bd-155">เอนทิตี DMF อนุญาตให้คุณสามารถนำเข้าและส่งออกข้อมูลเพื่อให้ตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="665bd-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="665bd-156">แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="665bd-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="665bd-157">แม่แบบส่งออกและนำเข้าข้อมูลตามลำดับตามการอ้างอิงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="665bd-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="665bd-158">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="665bd-158">Buy and sell leave</span></span> 

<span data-ttu-id="665bd-159">บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="665bd-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="665bd-160">กระบวนการนี้มักจะมีการจัดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="665bd-160">This process is often managed manually.</span></span> <span data-ttu-id="665bd-161">คุณลักษณะนี้จะทำให้การจัดการนโยบายและการร้องขอสำหรับแผนก HR เป็นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="665bd-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="665bd-162">ซึ่งช่วยลดขั้นตอนซ้ำซ้อนของกระบวนการการจัดการลางาน และช่วยกำจัดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="665bd-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="665bd-163">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="665bd-163">For more information, see:</span></span>

- [<span data-ttu-id="665bd-164">จัดการนโยบายซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="665bd-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="665bd-165">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="665bd-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="665bd-166">การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว</span><span class="sxs-lookup"><span data-stu-id="665bd-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="665bd-167">ลูกค้าสามารถประมวลผลการรับรู้สำหรับบริษัทเดียวหรือแผนการลางานและการขาดงานเดียว</span><span class="sxs-lookup"><span data-stu-id="665bd-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="665bd-168">ความสามารถนี้จะให้ความชัดเจนสำหรับกระบวนการรับรู้สำหรับลูกค้าที่มีปีของการลางานหรือนโยบายการรับรู้การลางานที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="665bd-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="665bd-169">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรับรู้การลางานสำหรับแต่ละบริษัทหรือสำหรับแผนการลางานแต่ละแผน](hr-leave-and-absence-accrue.md)</span><span class="sxs-lookup"><span data-stu-id="665bd-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="665bd-170">เพิ่มเอกสารแนบไปยังคำขอเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="665bd-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="665bd-171">ความสามารถในการเพิ่มเอกสารแนบไปยังคำขอลางานที่ได้รับการอนุมัติ เป็นสิ่งสำคัญในสภาพแวดล้อม COVID-19 ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="665bd-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="665bd-172">ขณะนี้พนักงานสามารถเพิ่มเอกสารแนบเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="665bd-172">Employees can now add these attachments.</span></span> <span data-ttu-id="665bd-173">นอกจากนี้ ยังมีข้อมูลเชิงลึกเพิ่มเติมเกี่ยวกับวิธีการที่จะทำการปรับปรุงไปยังคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="665bd-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="665bd-174">สำหรับข้อมูลเพิ่มเติม ให้ดู [เพิ่มเอกสารแนบไปยังคำขอที่มีอยู่](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)</span><span class="sxs-lookup"><span data-stu-id="665bd-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="665bd-175">เพิ่มรหัสเหตุผลไปยังการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="665bd-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="665bd-176">รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="665bd-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="665bd-177">กฎการยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="665bd-177">Carry forward rules</span></span> 

<span data-ttu-id="665bd-178">คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="665bd-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="665bd-179">ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน</span><span class="sxs-lookup"><span data-stu-id="665bd-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="665bd-180">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)</span><span class="sxs-lookup"><span data-stu-id="665bd-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="665bd-181">ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="665bd-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="665bd-182">คุณสามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ไม่ได้รับชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="665bd-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="665bd-183">การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น</span><span class="sxs-lookup"><span data-stu-id="665bd-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="665bd-184">คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="665bd-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="665bd-185">เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="665bd-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="665bd-186">ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="665bd-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="665bd-187">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="665bd-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="665bd-188">เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="665bd-188">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="665bd-189">เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="665bd-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="665bd-190">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="665bd-190">See also</span></span>

[<span data-ttu-id="665bd-191">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="665bd-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="665bd-192">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="665bd-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="665bd-193">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="665bd-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="665bd-194">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="665bd-194">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]