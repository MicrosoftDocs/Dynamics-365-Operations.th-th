---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Human Resources (11 มิถุนายน 2020)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Human Resources
author: Darinkramer
manager: AnnBe
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ec15c33cdb1abc32c28fd78822b06188dd0feac
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614297"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="1a270-103">มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Human Resources (11 มิถุนายน 2020)</span><span class="sxs-lookup"><span data-stu-id="1a270-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="1a270-104">บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="1a270-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1a270-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3316</span><span class="sxs-lookup"><span data-stu-id="1a270-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="1a270-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="1a270-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="1a270-107">บางครั้งฟอร์มพนักงานที่มีประสิทธิภาพทำให้ปุ่มปิด (X) ของฟอร์มรองหยุดทำงาน (442369)</span><span class="sxs-lookup"><span data-stu-id="1a270-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="1a270-108">เมื่อมีการเปิดใช้งานฟอร์ม **ผู้ปฏิบัติงาน** ใหม่ ปุ่มปิด (**X**) บางครั้งไม่ทำงานบนฟอร์มรอง</span><span class="sxs-lookup"><span data-stu-id="1a270-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="1a270-109">ปัญหานี้ไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="1a270-109">This problem was intermittent.</span></span> <span data-ttu-id="1a270-110">คุณสามารถปิดฟอร์มได้ หลังจากที่ปล่อยและกลับมา</span><span class="sxs-lookup"><span data-stu-id="1a270-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="1a270-111">ตัวอย่างเช่น คุณสามารถเลือกรายการเมนูทางด้านซ้าย และนำทางกลับไปยังฟอร์ม **ผู้ปฏิบัติงาน** และจากนั้นปิด</span><span class="sxs-lookup"><span data-stu-id="1a270-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="1a270-112">การนำออกใช้ของสัปดาห์นี้แก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="1a270-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="1a270-113">เอนทิตีผู้ติดต่อส่วนบุคคลของผู้ปฏิบัติงานไม่ส่งออกผู้ติดต่อส่วนบุคคลที่มีชนิดความสัมพันธ์หลัก</span><span class="sxs-lookup"><span data-stu-id="1a270-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="1a270-114">ด้วยการนำออกใช้นี้ เอนทิตี **ผู้ติดต่อส่วนบุคคลของผู้ปฏิบัติงาน** จะส่งออกชนิดความสัมพันธ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1a270-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="1a270-115">HcmPositionWorkerAssignmentV2Entity ควรเป็นส่วนหนึ่งของแพคเกจการรวมค่าจ้าง Ceridian ตามค่าเริ่มต้น (448506)</span><span class="sxs-lookup"><span data-stu-id="1a270-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="1a270-116">ด้วยการเปลี่ยนแปลงนี้ **HcmPositionWorkerAssignmentV2Entity** จะรวมอยู่ในแพคเกจการรวมค่าจ้าง Ceridian</span><span class="sxs-lookup"><span data-stu-id="1a270-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="1a270-117">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1a270-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="1a270-118">การล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a270-118">Database logging</span></span>

<span data-ttu-id="1a270-119">คุณลักษณะการบันทึกฐานข้อมูลจะช่วยให้คุณสามารถกำหนดตารางและฟิลด์ที่จะตรวจสอบได้</span><span class="sxs-lookup"><span data-stu-id="1a270-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="1a270-120">นอกจากนี้ยังช่วยให้คุณสามารถกำหนดเหตุการณ์ที่ควรทริกเกอร์การติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="1a270-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="1a270-121">คุณสามารถใช้ความสามารถในการบันทึกฐานข้อมูลเพื่อดูการเปลี่ยนแปลงเหล่านี้เมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="1a270-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="1a270-122">สำหรับข้อมูลเพิ่มเติมให้ ดูที่ [ตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล](hr-admin-database-logging.md)</span><span class="sxs-lookup"><span data-stu-id="1a270-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="1a270-123">โปรแกรมประบุกต์ Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="1a270-123">Human Resources application in Teams</span></span>

<span data-ttu-id="1a270-124">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1a270-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="1a270-125">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="1a270-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="1a270-126">สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841)</span><span class="sxs-lookup"><span data-stu-id="1a270-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="1a270-127">เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="1a270-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="1a270-128">เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="1a270-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="1a270-129">เอนทิตี DMF อนุญาตให้คุณสามารถนำเข้าและส่งออกข้อมูลเพื่อให้ตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="1a270-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="1a270-130">แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a270-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="1a270-131">แม่แบบส่งออกและนำเข้าข้อมูลตามลำดับตามการอ้างอิงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a270-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="1a270-132">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="1a270-132">Buy and sell leave</span></span> 

<span data-ttu-id="1a270-133">บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="1a270-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="1a270-134">กระบวนการนี้มักจะมีการจัดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1a270-134">This process is often managed manually.</span></span> <span data-ttu-id="1a270-135">คุณลักษณะนี้จะทำให้การจัดการนโยบายและการร้องขอสำหรับแผนก HR เป็นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="1a270-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="1a270-136">ซึ่งช่วยลดขั้นตอนซ้ำซ้อนของกระบวนการการจัดการลางาน และช่วยกำจัดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="1a270-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="1a270-137">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="1a270-137">For more information, see:</span></span>

- [<span data-ttu-id="1a270-138">จัดการนโยบายซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="1a270-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="1a270-139">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="1a270-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="1a270-140">การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว</span><span class="sxs-lookup"><span data-stu-id="1a270-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="1a270-141">ลูกค้าสามารถประมวลผลการรับรู้สำหรับบริษัทเดียวหรือแผนการลางานและการขาดงานเดียว</span><span class="sxs-lookup"><span data-stu-id="1a270-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="1a270-142">ความสามารถนี้จะให้ความชัดเจนแก่กระบวนการรับรู้สำหรับลูกค้าที่มีปีของการลางานหรือนโยบายการรับรู้การลางานที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="1a270-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="1a270-143">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรับรู้การลางานสำหรับแต่ละบริษัทหรือสำหรับแผนการลางานแต่ละแผน](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan)</span><span class="sxs-lookup"><span data-stu-id="1a270-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="1a270-144">เพิ่มเอกสารแนบไปยังคำขอเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="1a270-144">Add attachments to time off requests</span></span>

<span data-ttu-id="1a270-145">ความสามารถในการเพิ่มเอกสารแนบไปยังคำขอลางานที่ได้รับการอนุมัติ เป็นสิ่งสำคัญในสภาพแวดล้อม COVID-19 ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1a270-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="1a270-146">ขณะนี้พนักงานสามารถเพิ่มเอกสารแนบเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="1a270-146">Employees can now add these attachments.</span></span> <span data-ttu-id="1a270-147">นอกจากนี้ ยังมีข้อมูลเชิงลึกเพิ่มเติมเกี่ยวกับวิธีการที่จะทำการปรับปรุงไปยังคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="1a270-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="1a270-148">สำหรับข้อมูลเพิ่มเติม ให้ดู [เพิ่มเอกสารแนบไปยังคำขอที่มีอยู่](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)</span><span class="sxs-lookup"><span data-stu-id="1a270-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="1a270-149">เพิ่มรหัสเหตุผลไปยังการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="1a270-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="1a270-150">รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="1a270-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="1a270-151">กฎการยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="1a270-151">Carry forward rules</span></span> 

<span data-ttu-id="1a270-152">คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="1a270-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="1a270-153">ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน</span><span class="sxs-lookup"><span data-stu-id="1a270-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="1a270-154">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)</span><span class="sxs-lookup"><span data-stu-id="1a270-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="1a270-155">ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1a270-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="1a270-156">คุณสามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ไม่ได้รับชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1a270-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="1a270-157">การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น</span><span class="sxs-lookup"><span data-stu-id="1a270-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="1a270-158">คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="1a270-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="1a270-159">เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="1a270-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="1a270-160">ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="1a270-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="1a270-161">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="1a270-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="1a270-162">ความสามารถของแพลตฟอร์มใหม่</span><span class="sxs-lookup"><span data-stu-id="1a270-162">New platform capabilities</span></span> 

<span data-ttu-id="1a270-163">คุณจะสามารถทำให้ฟิลด์เป็นแบบบังคับโดยใช้การตั้งค่าส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="1a270-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="1a270-164">คุณลักษณะนี้จะกำหนดให้คุณเปิดใช้งาน **มุมมองที่บันทึกไว้**</span><span class="sxs-lookup"><span data-stu-id="1a270-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="1a270-165">ตั้งค่าคอนฟิกชื่อของระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1a270-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="1a270-166">ตัวเลือกใหม่จะพร้อมใช้งานในพารามิเตอร์ทรัพยากรบุคคลเพื่อปรับปรุงชื่อของพื้นที่ทำงานแบบบริการตนเองของพนักงานเป็นบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="1a270-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="1a270-167">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="1a270-167">See also</span></span>

[<span data-ttu-id="1a270-168">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="1a270-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="1a270-169">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="1a270-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="1a270-170">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="1a270-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="1a270-171">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="1a270-171">Manage features</span></span>](hr-admin-manage-features.md)