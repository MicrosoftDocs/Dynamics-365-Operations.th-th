---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (23 กรกฎาคม 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 23 กรกฏาคม 2020
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 30662ccf7e37f7f1e131e3b18b5a770c53fea0d1
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711879"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="e7312-103">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (23 กรกฎาคม 2020)</span><span class="sxs-lookup"><span data-stu-id="e7312-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

<span data-ttu-id="e7312-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="e7312-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e7312-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3416</span><span class="sxs-lookup"><span data-stu-id="e7312-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="e7312-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="e7312-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="e7312-107">การลบมิติทางการเงินในตำแหน่งไม่ทำงานตามที่คาดไว้ (445476)</span><span class="sxs-lookup"><span data-stu-id="e7312-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="e7312-108">การลบมิติออกจากตำแหน่งลบตำแหน่งเดียวกันเหล่านั้นออกจาก Common Data Service ด้วย</span><span class="sxs-lookup"><span data-stu-id="e7312-108">Removing dimensions from a position now removes those same positions from Common Data Service.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="e7312-109">ตำแหน่งงานที่ไม่ได้อยู่ในลำดับชั้นแสดงตำแหน่งงานที่ไม่ได้ใช้งาน (397257)</span><span class="sxs-lookup"><span data-stu-id="e7312-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="e7312-110">ตำแหน่งที่ไม่ได้ใช้งานอยู่ (มีระยะเวลาหมดอายุ) ไม่แสดงลำดับชั้นของตำแหน่งเป็น **ตำแหน่งที่ไม่ได้อยู่ในลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="e7312-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="e7312-111">การตรวจสอบความถูกต้องที่เกิดขึ้นระหว่าง LeaveEnrollmentEntity และ HcmWorkerEntity ในการนำเข้ากรอบงานการจัดการข้อมูล (DMF) ทำให้เกิดการโหลดข้อมูลที่ช้าลง (442324)</span><span class="sxs-lookup"><span data-stu-id="e7312-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="e7312-112">การเปลี่ยนแปลงในรุ่นนี้เพิ่มประสิทธิภาพการทำงานของ **LeaveEnrollmentEntity**</span><span class="sxs-lookup"><span data-stu-id="e7312-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="e7312-113">ไม่สามารถตั้งค่าส่วนบุคคลในการบริหารองค์กร (447490)</span><span class="sxs-lookup"><span data-stu-id="e7312-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="e7312-114">ด้วยการเปลี่ยนแปลงนี้คุณสามารถกำหนดลิงค์ให้กับการ **การจัดการองค์กร**</span><span class="sxs-lookup"><span data-stu-id="e7312-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="e7312-115">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e7312-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="e7312-116">ฟิลด์บังคับ</span><span class="sxs-lookup"><span data-stu-id="e7312-116">Mandatory fields</span></span> 

<span data-ttu-id="e7312-117">ขณะนี้คุณสามารถทำให้ฟิลด์บังคับโดยใช้ความสามารถในการตั้งค่าส่วนบุคคลของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e7312-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="e7312-118">ลักษณะการทำงานนี้จำเป็นต้องใช้ **มุมมองที่บันทึกไว้**</span><span class="sxs-lookup"><span data-stu-id="e7312-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="e7312-119">โปรแกรมประบุกต์ Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="e7312-119">Human Resources application in Teams</span></span>

<span data-ttu-id="e7312-120">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e7312-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="e7312-121">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="e7312-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="e7312-122">สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841)</span><span class="sxs-lookup"><span data-stu-id="e7312-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="e7312-123">เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e7312-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="e7312-124">เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="e7312-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="e7312-125">เอนทิตี DMF อนุญาตให้คุณสามารถนำเข้าและส่งออกข้อมูลเพื่อให้ตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="e7312-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="e7312-126">แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e7312-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="e7312-127">แม่แบบส่งออกและนำเข้าข้อมูลตามลำดับตามการอ้างอิงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e7312-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="e7312-128">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="e7312-128">Buy and sell leave</span></span> 

<span data-ttu-id="e7312-129">บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="e7312-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="e7312-130">กระบวนการนี้มักจะมีการจัดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="e7312-130">This process is often managed manually.</span></span> <span data-ttu-id="e7312-131">คุณลักษณะนี้จะทำให้การจัดการนโยบายและการร้องขอสำหรับแผนก HR เป็นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e7312-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="e7312-132">ซึ่งช่วยลดขั้นตอนซ้ำซ้อนของกระบวนการการจัดการลางาน และช่วยกำจัดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="e7312-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="e7312-133">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="e7312-133">For more information, see:</span></span>

- [<span data-ttu-id="e7312-134">จัดการนโยบายซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="e7312-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="e7312-135">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="e7312-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="e7312-136">การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว</span><span class="sxs-lookup"><span data-stu-id="e7312-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="e7312-137">ลูกค้าสามารถประมวลผลการรับรู้สำหรับบริษัทเดียวหรือแผนการลางานและการขาดงานเดียว</span><span class="sxs-lookup"><span data-stu-id="e7312-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="e7312-138">ความสามารถนี้จะให้ความชัดเจนสำหรับกระบวนการรับรู้สำหรับลูกค้าที่มีปีของการลางานหรือนโยบายการรับรู้การลางานที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e7312-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="e7312-139">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรับรู้การลางานสำหรับแต่ละบริษัทหรือสำหรับแผนการลางานแต่ละแผน](hr-leave-and-absence-accrue.md)</span><span class="sxs-lookup"><span data-stu-id="e7312-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="e7312-140">เพิ่มเอกสารแนบไปยังคำขอเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="e7312-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="e7312-141">ความสามารถในการเพิ่มเอกสารแนบไปยังคำขอลางานที่ได้รับการอนุมัติ เป็นสิ่งสำคัญในสภาพแวดล้อม COVID-19 ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="e7312-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="e7312-142">ขณะนี้พนักงานสามารถเพิ่มเอกสารแนบเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="e7312-142">Employees can now add these attachments.</span></span> <span data-ttu-id="e7312-143">นอกจากนี้ ยังมีข้อมูลเชิงลึกเพิ่มเติมเกี่ยวกับวิธีการที่จะทำการปรับปรุงไปยังคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="e7312-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="e7312-144">สำหรับข้อมูลเพิ่มเติม ให้ดู [เพิ่มเอกสารแนบไปยังคำขอที่มีอยู่](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)</span><span class="sxs-lookup"><span data-stu-id="e7312-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="e7312-145">เพิ่มรหัสเหตุผลไปยังการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="e7312-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="e7312-146">รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="e7312-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="e7312-147">กฎการยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="e7312-147">Carry forward rules</span></span> 

<span data-ttu-id="e7312-148">คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="e7312-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="e7312-149">ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน</span><span class="sxs-lookup"><span data-stu-id="e7312-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="e7312-150">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)</span><span class="sxs-lookup"><span data-stu-id="e7312-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="e7312-151">ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="e7312-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="e7312-152">คุณสามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ไม่ได้รับชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e7312-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="e7312-153">การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น</span><span class="sxs-lookup"><span data-stu-id="e7312-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="e7312-154">คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="e7312-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="e7312-155">เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="e7312-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="e7312-156">ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="e7312-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="e7312-157">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="e7312-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="e7312-158">เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e7312-158">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="e7312-159">เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e7312-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="e7312-160">การเปลี่ยนแปลงแพลตฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="e7312-160">Platform changes</span></span>

<span data-ttu-id="e7312-161">Platform Update 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="e7312-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="e7312-162">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="e7312-162">See also</span></span>

[<span data-ttu-id="e7312-163">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="e7312-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="e7312-164">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="e7312-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="e7312-165">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="e7312-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="e7312-166">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e7312-166">Manage features</span></span>](hr-admin-manage-features.md)
