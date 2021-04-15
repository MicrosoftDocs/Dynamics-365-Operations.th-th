---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Human Resources (11 มิถุนายน 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 11 มิถุนายน 2020
author: andreabichsel
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 93858ede862c9a20d84952f9c4318acf07f1cabb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802346"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="46b53-103">มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Human Resources (11 มิถุนายน 2020)</span><span class="sxs-lookup"><span data-stu-id="46b53-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="46b53-104">บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="46b53-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="46b53-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3316</span><span class="sxs-lookup"><span data-stu-id="46b53-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="46b53-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="46b53-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="46b53-107">บางครั้งฟอร์มพนักงานที่มีประสิทธิภาพทำให้ปุ่มปิด (X) ของฟอร์มรองหยุดทำงาน (442369)</span><span class="sxs-lookup"><span data-stu-id="46b53-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="46b53-108">เมื่อมีการเปิดใช้งานฟอร์ม **ผู้ปฏิบัติงาน** ใหม่ ปุ่มปิด (**X**) บางครั้งไม่ทำงานบนฟอร์มรอง</span><span class="sxs-lookup"><span data-stu-id="46b53-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="46b53-109">ปัญหานี้ไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="46b53-109">This problem was intermittent.</span></span> <span data-ttu-id="46b53-110">คุณสามารถปิดฟอร์มได้ หลังจากที่ปล่อยและกลับมา</span><span class="sxs-lookup"><span data-stu-id="46b53-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="46b53-111">ตัวอย่างเช่น คุณสามารถเลือกรายการเมนูทางด้านซ้าย และนำทางกลับไปยังฟอร์ม **ผู้ปฏิบัติงาน** และจากนั้นปิด</span><span class="sxs-lookup"><span data-stu-id="46b53-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="46b53-112">การนำออกใช้ของสัปดาห์นี้แก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="46b53-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="46b53-113">เอนทิตีผู้ติดต่อส่วนบุคคลของผู้ปฏิบัติงานไม่ส่งออกผู้ติดต่อส่วนบุคคลที่มีชนิดความสัมพันธ์หลัก</span><span class="sxs-lookup"><span data-stu-id="46b53-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="46b53-114">ด้วยการนำออกใช้นี้ เอนทิตี **ผู้ติดต่อส่วนบุคคลของผู้ปฏิบัติงาน** จะส่งออกชนิดความสัมพันธ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="46b53-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="46b53-115">HcmPositionWorkerAssignmentV2Entity ควรเป็นส่วนหนึ่งของแพคเกจการรวมค่าจ้าง Ceridian ตามค่าเริ่มต้น (448506)</span><span class="sxs-lookup"><span data-stu-id="46b53-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="46b53-116">ด้วยการเปลี่ยนแปลงนี้ **HcmPositionWorkerAssignmentV2Entity** จะรวมอยู่ในแพคเกจการรวมค่าจ้าง Ceridian</span><span class="sxs-lookup"><span data-stu-id="46b53-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="46b53-117">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="46b53-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="46b53-118">การล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="46b53-118">Database logging</span></span>

<span data-ttu-id="46b53-119">คุณลักษณะการบันทึกฐานข้อมูลจะช่วยให้คุณสามารถกำหนดตารางและฟิลด์ที่จะตรวจสอบได้</span><span class="sxs-lookup"><span data-stu-id="46b53-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="46b53-120">นอกจากนี้ยังช่วยให้คุณสามารถกำหนดเหตุการณ์ที่ควรทริกเกอร์การติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="46b53-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="46b53-121">คุณสามารถใช้ความสามารถในการบันทึกฐานข้อมูลเพื่อดูการเปลี่ยนแปลงเหล่านี้เมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="46b53-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="46b53-122">สำหรับข้อมูลเพิ่มเติมให้ ดูที่ [ตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล](hr-admin-database-logging.md)</span><span class="sxs-lookup"><span data-stu-id="46b53-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="46b53-123">โปรแกรมประบุกต์ Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="46b53-123">Human Resources application in Teams</span></span>

<span data-ttu-id="46b53-124">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="46b53-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="46b53-125">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="46b53-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="46b53-126">สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841)</span><span class="sxs-lookup"><span data-stu-id="46b53-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="46b53-127">เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="46b53-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="46b53-128">เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="46b53-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="46b53-129">เอนทิตี DMF อนุญาตให้คุณสามารถนำเข้าและส่งออกข้อมูลเพื่อให้ตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="46b53-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="46b53-130">แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="46b53-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="46b53-131">แม่แบบส่งออกและนำเข้าข้อมูลตามลำดับตามการอ้างอิงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="46b53-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="46b53-132">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="46b53-132">Buy and sell leave</span></span> 

<span data-ttu-id="46b53-133">บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="46b53-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="46b53-134">กระบวนการนี้มักจะมีการจัดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="46b53-134">This process is often managed manually.</span></span> <span data-ttu-id="46b53-135">คุณลักษณะนี้จะทำให้การจัดการนโยบายและการร้องขอสำหรับแผนก HR เป็นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="46b53-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="46b53-136">ซึ่งช่วยลดขั้นตอนซ้ำซ้อนของกระบวนการการจัดการลางาน และช่วยกำจัดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="46b53-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="46b53-137">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="46b53-137">For more information, see:</span></span>

- [<span data-ttu-id="46b53-138">จัดการนโยบายซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="46b53-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="46b53-139">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="46b53-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="46b53-140">การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว</span><span class="sxs-lookup"><span data-stu-id="46b53-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="46b53-141">ลูกค้าสามารถประมวลผลการรับรู้สำหรับบริษัทเดียวหรือแผนการลางานและการขาดงานเดียว</span><span class="sxs-lookup"><span data-stu-id="46b53-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="46b53-142">ความสามารถนี้จะให้ความชัดเจนแก่กระบวนการรับรู้สำหรับลูกค้าที่มีปีของการลางานหรือนโยบายการรับรู้การลางานที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="46b53-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="46b53-143">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรับรู้การลางานสำหรับแต่ละบริษัทหรือสำหรับแผนการลางานแต่ละแผน](hr-leave-and-absence-accrue.md)</span><span class="sxs-lookup"><span data-stu-id="46b53-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="46b53-144">เพิ่มเอกสารแนบไปยังคำขอเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="46b53-144">Add attachments to time off requests</span></span>

<span data-ttu-id="46b53-145">ความสามารถในการเพิ่มเอกสารแนบไปยังคำขอลางานที่ได้รับการอนุมัติ เป็นสิ่งสำคัญในสภาพแวดล้อม COVID-19 ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="46b53-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="46b53-146">ขณะนี้พนักงานสามารถเพิ่มเอกสารแนบเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="46b53-146">Employees can now add these attachments.</span></span> <span data-ttu-id="46b53-147">นอกจากนี้ ยังมีข้อมูลเชิงลึกเพิ่มเติมเกี่ยวกับวิธีการที่จะทำการปรับปรุงไปยังคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="46b53-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="46b53-148">สำหรับข้อมูลเพิ่มเติม ให้ดู [เพิ่มเอกสารแนบไปยังคำขอที่มีอยู่](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)</span><span class="sxs-lookup"><span data-stu-id="46b53-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="46b53-149">เพิ่มรหัสเหตุผลไปยังการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="46b53-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="46b53-150">รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="46b53-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="46b53-151">กฎการยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="46b53-151">Carry forward rules</span></span> 

<span data-ttu-id="46b53-152">คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="46b53-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="46b53-153">ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน</span><span class="sxs-lookup"><span data-stu-id="46b53-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="46b53-154">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)</span><span class="sxs-lookup"><span data-stu-id="46b53-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="46b53-155">ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="46b53-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="46b53-156">คุณสามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ไม่ได้รับชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="46b53-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="46b53-157">การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น</span><span class="sxs-lookup"><span data-stu-id="46b53-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="46b53-158">คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="46b53-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="46b53-159">เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="46b53-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="46b53-160">ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="46b53-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="46b53-161">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="46b53-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="46b53-162">ความสามารถของแพลตฟอร์มใหม่</span><span class="sxs-lookup"><span data-stu-id="46b53-162">New platform capabilities</span></span> 

<span data-ttu-id="46b53-163">คุณจะสามารถทำให้ฟิลด์เป็นแบบบังคับโดยใช้การตั้งค่าส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="46b53-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="46b53-164">คุณลักษณะนี้จะกำหนดให้คุณเปิดใช้งาน **มุมมองที่บันทึกไว้**</span><span class="sxs-lookup"><span data-stu-id="46b53-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="46b53-165">ตั้งค่าคอนฟิกชื่อของระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="46b53-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="46b53-166">ตัวเลือกใหม่จะพร้อมใช้งานในพารามิเตอร์ทรัพยากรบุคคลเพื่อปรับปรุงชื่อของพื้นที่ทำงานแบบบริการตนเองของพนักงานเป็นบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="46b53-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="46b53-167">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="46b53-167">See also</span></span>

[<span data-ttu-id="46b53-168">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="46b53-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="46b53-169">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="46b53-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="46b53-170">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="46b53-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="46b53-171">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="46b53-171">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]