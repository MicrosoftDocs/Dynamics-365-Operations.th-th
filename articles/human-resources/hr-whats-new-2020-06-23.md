---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Human Resources (25 มิถุนายน 2020)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Human Resources
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa02cf10b2b4fe08440d3641472e83dfe58169c9
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614397"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="3906d-103">มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Human Resources (23 มิถุนายน 2020)</span><span class="sxs-lookup"><span data-stu-id="3906d-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

<span data-ttu-id="3906d-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="3906d-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3906d-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3347</span><span class="sxs-lookup"><span data-stu-id="3906d-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="3906d-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="3906d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="3906d-107">เมื่อมีการลงทะเบียนหมดอายุสำหรับพนักงานที่สิ้นสุดการจ้างงาน ชนิดการลางาน ยอดดุล และยอดเงินจะถูกล้างทั้งหมดในแบบฟอร์มการลงทะเบียนการลา (444867)</span><span class="sxs-lookup"><span data-stu-id="3906d-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="3906d-108">ค่าใน **ชนิดการลางาน** **ยอดดุล** และ **ยอดเงิน** ขณะนี้ยังคงถูกเก็บรักษาแทนการลบออกเมื่อทำการเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="3906d-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="3906d-109">ยอดดุลที่คาดการณ์ไว้ไม่ถูกต้องเมื่อมีการเปิดใช้งานคุณลักษณะใหม่ (การลางานคงค้างสำหรับบริษัทหนึ่งๆ หรือแผนเดียว) (456553)</span><span class="sxs-lookup"><span data-stu-id="3906d-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="3906d-110">ยอดดุลที่คาดการณ์ไว้ที่ถูกต้องขณะนี้แสดงเมื่อเปิดใช้งานการคงค้างการลางานสำหรับบริษัทหนึ่งๆ หรือแผนเดียว</span><span class="sxs-lookup"><span data-stu-id="3906d-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="3906d-111">เอนทิตีที่มีความสัมพันธ์ที่มีผลในคุณสมบัติการนำทางที่ซ้ำกัน (456486)</span><span class="sxs-lookup"><span data-stu-id="3906d-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="3906d-112">รุ่นนี้แก้ไขปัญหาเกี่ยวกับคุณสมบัติการนำทาง (ความสัมพันธ์) ของหลายเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="3906d-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="3906d-113">ตรวจพบความสัมพันธ์ที่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="3906d-113">Duplicate relations are detected.</span></span> <span data-ttu-id="3906d-114">สถานการณ์เหล่านี้ได้รับการแก้ไขทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="3906d-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="3906d-115">ความคิดเห็นข้ามบริษัทบนการตรวจทานประสิทธิภาพ (455536)</span><span class="sxs-lookup"><span data-stu-id="3906d-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="3906d-116">ความคิดเห็นข้ามบริษัทในขณะนี้สามารถมองเห็นได้จากการตรวจทานประสิทธิภาพด้วยการแก้ไขนี้</span><span class="sxs-lookup"><span data-stu-id="3906d-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="3906d-117">การเปลี่ยนแปลงนี้จะแก้ไขมุมมองของข้อคิดเห็นของผู้ตรวจทานที่ป้อนไว้ในบริษัทต่างๆ สำหรับการตรวจทานประสิทธิภาพเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="3906d-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="3906d-118">ความไม่สอดคล้องกันในการแสดงข้อมูลการจัดการค่าตอบแทน (432562)</span><span class="sxs-lookup"><span data-stu-id="3906d-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="3906d-119">ขณะนี้ยังคงมีมุมมองที่สอดคล้องกันของข้อมูลค่าตอบแทนในบริการตนเองของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="3906d-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="3906d-120">ข้อมูลค่าตอบแทนจะแสดงต่อผู้จัดการอย่างสอดคล้องกัน ทั้งนี้ขึ้นอยู่กับวิธีการนำทางไปยัง **รายละเอียดค่าตอบแทน** ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3906d-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="3906d-121">ค่าเริ่มต้นวันที่มีผลบังคับใช้ของแผนค่าตอบแทนคงที่เป็นวันที่ของวันนี้ (411994)</span><span class="sxs-lookup"><span data-stu-id="3906d-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="3906d-122">ขณะนี้มีการกำหนดวันที่เริ่มต้นการชดเชยตามวันที่เริ่มต้นของตำแหน่งงานที่กำหนดให้กับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="3906d-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="3906d-123">แบบฟอร์มการลางานและการขาดงานเปิดใช้งานข้อกำหนดครึ่งวันถูกปิดใช้งานเมื่อเปิดแบบฟอร์ม (452607)</span><span class="sxs-lookup"><span data-stu-id="3906d-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="3906d-124">เมื่อมีการเปลี่ยนแปลงนี้ **การเปิดใช้งานข้อกำหนดครึ่งวัน** จะเปิดใช้งานจนกว่าจะมีธุรกรรมการลางานใหม่อยู่</span><span class="sxs-lookup"><span data-stu-id="3906d-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="3906d-125">ไม่สามารถเผยแพร่ไปยัง HcmDiscussionEntity ผ่านทาง Excel ได้ ข้อผิดพลาดฟิลด์ TotalRatingScore (453899)</span><span class="sxs-lookup"><span data-stu-id="3906d-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="3906d-126">ขณะนี้คุณสามารถอัปเดตฟิลด์ **TotalRatingScore** โดยใช้ **HCMDiscussionEntity** ในโปรแกรมออกแบบสมุดงาน Excel</span><span class="sxs-lookup"><span data-stu-id="3906d-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="3906d-127">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3906d-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="3906d-128">การล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3906d-128">Database logging</span></span>

<span data-ttu-id="3906d-129">การล็อกฐานข้อมูลจะช่วยให้คุณสามารถกำหนดตารางและฟิลด์ที่จะตรวจสอบได้</span><span class="sxs-lookup"><span data-stu-id="3906d-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="3906d-130">นอกจากนี้ยังช่วยให้คุณสามารถกำหนดเหตุการณ์ที่ควรทริกเกอร์การติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="3906d-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="3906d-131">คุณสามารถใช้ความสามารถในการบันทึกฐานข้อมูลเพื่อดูการเปลี่ยนแปลงเหล่านี้เมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="3906d-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="3906d-132">สำหรับข้อมูลเพิ่มเติมให้ ดูที่ [ตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล](hr-admin-database-logging.md)</span><span class="sxs-lookup"><span data-stu-id="3906d-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="3906d-133">ฟิลด์บังคับ</span><span class="sxs-lookup"><span data-stu-id="3906d-133">Mandatory fields</span></span> 

<span data-ttu-id="3906d-134">ขณะนี้คุณสามารถทำให้ฟิลด์บังคับโดยใช้ความสามารถในการตั้งค่าส่วนบุคคลของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="3906d-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="3906d-135">ลักษณะการทำงานนี้จำเป็นต้องใช้ **มุมมองที่บันทึกไว้**</span><span class="sxs-lookup"><span data-stu-id="3906d-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="3906d-136">โปรแกรมประบุกต์ Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="3906d-136">Human Resources application in Teams</span></span>

<span data-ttu-id="3906d-137">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3906d-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="3906d-138">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="3906d-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="3906d-139">สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841)</span><span class="sxs-lookup"><span data-stu-id="3906d-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="3906d-140">เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3906d-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="3906d-141">เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="3906d-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="3906d-142">เอนทิตี DMF อนุญาตให้คุณสามารถนำเข้าและส่งออกข้อมูลเพื่อให้ตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="3906d-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="3906d-143">แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3906d-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="3906d-144">แม่แบบส่งออกและนำเข้าข้อมูลตามลำดับตามการอ้างอิงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3906d-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="3906d-145">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="3906d-145">Buy and sell leave</span></span> 

<span data-ttu-id="3906d-146">บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="3906d-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="3906d-147">กระบวนการนี้มักจะมีการจัดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="3906d-147">This process is often managed manually.</span></span> <span data-ttu-id="3906d-148">คุณลักษณะนี้จะทำให้การจัดการนโยบายและการร้องขอสำหรับแผนก HR เป็นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3906d-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="3906d-149">ซึ่งช่วยลดขั้นตอนซ้ำซ้อนของกระบวนการการจัดการลางาน และช่วยกำจัดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="3906d-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="3906d-150">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="3906d-150">For more information, see:</span></span>

- [<span data-ttu-id="3906d-151">จัดการนโยบายซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="3906d-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="3906d-152">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="3906d-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="3906d-153">การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว</span><span class="sxs-lookup"><span data-stu-id="3906d-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="3906d-154">ลูกค้าสามารถประมวลผลการรับรู้สำหรับบริษัทเดียวหรือแผนการลางานและการขาดงานเดียว</span><span class="sxs-lookup"><span data-stu-id="3906d-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="3906d-155">ความสามารถนี้จะให้ความชัดเจนแก่กระบวนการรับรู้สำหรับลูกค้าที่มีปีของการลางานหรือนโยบายการรับรู้การลางานที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="3906d-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="3906d-156">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรับรู้การลางานสำหรับแต่ละบริษัทหรือสำหรับแผนการลางานแต่ละแผน](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan)</span><span class="sxs-lookup"><span data-stu-id="3906d-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="3906d-157">เพิ่มเอกสารแนบไปยังคำขอเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="3906d-157">Add attachments to time off requests</span></span>

<span data-ttu-id="3906d-158">ความสามารถในการเพิ่มเอกสารแนบไปยังคำขอลางานที่ได้รับการอนุมัติ เป็นสิ่งสำคัญในสภาพแวดล้อม COVID-19 ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3906d-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="3906d-159">ขณะนี้พนักงานสามารถเพิ่มเอกสารแนบเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="3906d-159">Employees can now add these attachments.</span></span> <span data-ttu-id="3906d-160">นอกจากนี้ ยังมีข้อมูลเชิงลึกเพิ่มเติมเกี่ยวกับวิธีการที่จะทำการปรับปรุงไปยังคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="3906d-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="3906d-161">สำหรับข้อมูลเพิ่มเติม ให้ดู [เพิ่มเอกสารแนบไปยังคำขอที่มีอยู่](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)</span><span class="sxs-lookup"><span data-stu-id="3906d-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="3906d-162">เพิ่มรหัสเหตุผลไปยังการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="3906d-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="3906d-163">รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="3906d-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="3906d-164">กฎการยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="3906d-164">Carry forward rules</span></span> 

<span data-ttu-id="3906d-165">คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="3906d-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="3906d-166">ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน</span><span class="sxs-lookup"><span data-stu-id="3906d-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="3906d-167">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)</span><span class="sxs-lookup"><span data-stu-id="3906d-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="3906d-168">ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3906d-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="3906d-169">คุณสามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ไม่ได้รับชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="3906d-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="3906d-170">การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น</span><span class="sxs-lookup"><span data-stu-id="3906d-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="3906d-171">คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="3906d-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="3906d-172">เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="3906d-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="3906d-173">ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="3906d-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="3906d-174">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="3906d-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="3906d-175">ตั้งค่าคอนฟิกชื่อของระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="3906d-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="3906d-176">ตัวเลือกใหม่จะพร้อมใช้งานใน **พารามิเตอร์ทรัพยากรบุคคล** เพื่อปรับปรุงชื่อของพื้นที่ทำงานแบบบริการตนเองของพนักงานเป็นบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="3906d-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="3906d-177">เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3906d-177">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="3906d-178">เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3906d-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="3906d-179">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3906d-179">See also</span></span>

[<span data-ttu-id="3906d-180">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="3906d-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="3906d-181">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="3906d-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="3906d-182">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="3906d-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="3906d-183">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="3906d-183">Manage features</span></span>](hr-admin-manage-features.md)