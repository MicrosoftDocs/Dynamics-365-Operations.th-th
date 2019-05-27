---
title: การจัดการการลางานและการขาดงาน
description: หัวข้อนี้แสดงภาพรวมของโมดูลการจัดการการลางานและการขาดงาน
author: andreabichsel
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebfaeb0696d7200ddf3c715f96a259b91db08e7a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519196"
---
# <a name="leave-and-absence-management"></a><span data-ttu-id="70f09-103">การจัดการการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="70f09-103">Leave and absence management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70f09-104">โมดูล **การจัดการการลางานและการขาดงาน** มีกรอบงานแบบยืดหยุ่นสำหรับการกำหนดกระบวนการจัดการการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="70f09-104">The **Leave and absence management** module offers a flexible framework for defining the absence management process.</span></span> <span data-ttu-id="70f09-105">คุณสามารถสร้างแผนการลางานและการขาดงานเพื่อกำหนดการลาหยุดที่คงค้างหรืออนุญาตให้ลาหยุดของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="70f09-105">Leave and absence plans can be created to determine how employees accrue or are granted time off.</span></span> <span data-ttu-id="70f09-106">หลังจากที่พนักงานลงทะเบียนในแผน พวกเขาสามารถส่งคำขอเวลาหยุดพักเพื่อขออนุมัติโดยผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="70f09-106">After employees are enrolled in a plan, they can submit time-off requests for approval by managers.</span></span> <span data-ttu-id="70f09-107">การติดตามการลางานให้ทั้งผู้จัดการระดับต้นและผู้จัดการฝ่ายทรัพยากรบุคคล (HR) สามารถดูว่าบุคคลใดบ้างที่ลาหยุด และจำนวนการลาหยุดที่พวกเขาเหลืออยู่</span><span class="sxs-lookup"><span data-stu-id="70f09-107">Leave tracking lets both first-level managers and Human Resources (HR) managers see who is taking time off and how much time off each employee still has.</span></span>  

<span data-ttu-id="70f09-108">การจัดการการลางานและการขาดงานมีคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="70f09-108">Leave and absence management provides the following features:</span></span> 

- <span data-ttu-id="70f09-109">**กำหนดชนิดการลางานและการหยุดงาน**</span><span class="sxs-lookup"><span data-stu-id="70f09-109">**Define leave and absence types.**</span></span>

    <span data-ttu-id="70f09-110">ชนิดการลางานกำหนดชนิดต่าง ๆ ของการขาดงานที่พนักงานสามารถรายงาน</span><span class="sxs-lookup"><span data-stu-id="70f09-110">Leave types define the various types of absences that employees can report.</span></span> <span data-ttu-id="70f09-111">เนื่องจากชนิดเหล่านี้จะกำหนดโดยผู้ใช้ ซึ่งอาจถูกทำให้เหมาะสมกับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="70f09-111">Because these types are user-defined, they can be tailored to your organization.</span></span> <span data-ttu-id="70f09-112">ชนิดการลางานทั่วไปบางอย่าง เช่น เวลาหยุดพักที่ชำระ (PTO) การลางาน ทุพพลภาพระยะสั้น การเข้าร่วมระบบยุติธรรม (ชนิดการลางานนี้ใช้เฉพาะกับสหรัฐ) และการสูญเสียญาติ</span><span class="sxs-lookup"><span data-stu-id="70f09-112">Some typical leave types include paid time off (PTO), leave, short-term disability, jury duty (this leave type is specific to the United States), and bereavement.</span></span> 

- <span data-ttu-id="70f09-113">**กำหนดแผนการลางานและการขาดงานที่จัดระดับให้เหมาะกับธุรกิจของคุณ**</span><span class="sxs-lookup"><span data-stu-id="70f09-113">**Define leave and absence plans that are tiered to fit your business.**</span></span>

    <span data-ttu-id="70f09-114">คุณสามารถกำหนดแผนการลางานและการขาดงานเพื่อให้มีการรับรู้เกิดขึ้นในความถี่ที่กำหนด เช่น รายปี รายเดือน หรือทุก ๆ ครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="70f09-114">Leave and absence plans can be defined so that accrual occurs at specific frequencies, such as annually, monthly, or semimonthly.</span></span> <span data-ttu-id="70f09-115">นอกจากนี้ยังสามารถกำหนดแผนเป็นเงินช่วยเหลือที่มีการรับรู้เดียวเกิดขึ้นในวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="70f09-115">Plans can also be defined as a grant, where a single accrual occurs on a specific date.</span></span> 

    <span data-ttu-id="70f09-116">แผนการลางานมักประกอบด้วยระดับที่บางกลุ่มของพนักงานได้รับผลประโยชน์เพิ่มเติม ตามจำนวนเวลาที่ได้เข้ากับองค์กร</span><span class="sxs-lookup"><span data-stu-id="70f09-116">Leave plans often contain tiers, where some groups of employees receive additional benefits, based on the amount of time that they have been with the organization.</span></span> <span data-ttu-id="70f09-117">ระดับที่ผู้ใช้กำหนดเหล่านี้จะเปิดใช้งานการลงทะเบียนโดยอัตโนมัติในจำนวนชั่วโมงของสวัสดิการเพิ่มเติม ตามเกณฑ์วันที่ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="70f09-117">These user-defined tiers enable automatic enrollment in additional benefit hours, based on the date criteria that are defined.</span></span> <span data-ttu-id="70f09-118">นอกจากนี้ยังสามารถกำหนดค่าแผนการลางานเพื่อเพิ่มจำนวนที่เหลือสูงสุดหรือลดยอดดุลต่ำสุด เพื่อป้องกันไม่ให้พนักงานใช้ชั่วโมงสวัสดิการมากกว่าที่ได้รับรู้</span><span class="sxs-lookup"><span data-stu-id="70f09-118">Leave plans can also be configured to enforce a maximum carry-over amount or a minimum balance, to prevent employees from using more benefit hours than they have accrued.</span></span> 

    <span data-ttu-id="70f09-119">แผนการลางานโดยทั่วไปรวมแผนที่มีการจัดระดับที่ให้สวัสดิการ 80 ชั่วโมงของ PTO กับพนักงานใหม่ และสวัสดิการ 120 ชั่วโมงหลังจากการบริการ 60 เดือน</span><span class="sxs-lookup"><span data-stu-id="70f09-119">Typical leave plans include tiered plans that grant a benefit of 80 hours of PTO to new employees but a benefit of 120 hours after 60 months of service.</span></span> <span data-ttu-id="70f09-120">แผนเพิ่มเติมอาจให้วันหยุดลอยตัวหรือสวัสดิการตามตำแหน่ง เช่น ชั่วโมงสวัสดิการเฉพาะผู้บริหาร</span><span class="sxs-lookup"><span data-stu-id="70f09-120">Additional plans might grant floating holidays or position-based benefits, such as executive-only benefit hours.</span></span>

- <span data-ttu-id="70f09-121">**ลงทะเบียนพนักงานในแผนการลางานและการขาดงานของแต่ละรายการ หรือโดยใช้การกำหนดโดยรวมที่เป็นไปตามเงื่อนไขของงาน**</span><span class="sxs-lookup"><span data-stu-id="70f09-121">**Enroll employees in leave and absence plans individually or through mass assignment that is based on job criteria.**</span></span>

    <span data-ttu-id="70f09-122">สามารถใช้ตัวกรองที่เกี่ยวข้องกับงานหลายอย่างเพื่อกำหนดกลุ่มของพนักงานกับแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="70f09-122">Several job-related filters can be used to assign a group of employees to a leave plan.</span></span> <span data-ttu-id="70f09-123">ผู้จัดการฝ่าย HR สามารถดูพนักงานเพื่อดูว่าแผนการลางานและการขาดงานใดที่พนักงานลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70f09-123">HR managers can view an employee to see what leave and absence plans the employee is enrolled in.</span></span> <span data-ttu-id="70f09-124">อีกทางหนึ่งคือ ผู้จัดการฝ่าย HR สามารถดูแผนทั้งหมดและการลงทะเบียนของพนักงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="70f09-124">Alternatively, HR managers can view all plans and the related employee enrollments.</span></span>

- <span data-ttu-id="70f09-125">**ระงับแผนการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="70f09-125">**Suspend leave and absence plans.**</span></span>

    <span data-ttu-id="70f09-126">แผนการลางานและการขาดงานอาจถูกระงับเพื่อปิดใช้งานและป้องกันไม่ให้มีการรับรู้เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="70f09-126">Leave and absence plans can be suspended to make them inactive and prevent additional accruals.</span></span> <span data-ttu-id="70f09-127">การรับรู้รายได้รายจ่ายจะถูกระงับสำหรับพนักงานเมื่อสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="70f09-127">Accruals are suspended for employees if their employment ends.</span></span>  

- <span data-ttu-id="70f09-128">**ปรับปรุงสิทธิประโยชน์และเงินช่วยเหลือ**</span><span class="sxs-lookup"><span data-stu-id="70f09-128">**Adjust entitlements and grants.**</span></span>

    <span data-ttu-id="70f09-129">พนักงานสามารถลงทะเบียนในแผนระดับสูงโดยใช้วันที่เฉพาะผู้ปฏิบัติงานเพื่อแทนที่ข้อเสนอแผนเริ่มต้นของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="70f09-129">An employee can be enrolled in a higher plan tier by using a worker-specific date to override the employee's default plan offering.</span></span> <span data-ttu-id="70f09-130">พนักงานสามารถได้รับการปรับปรุงด้วยตนเองของยอดดุลการลางานและการขาดงาน ณ เวลาที่ลงทะเบียนแผน หรือ HR สามารถทำการปรับปรุงด้วยตนเองได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="70f09-130">Employees can receive a manual adjustment to their leave and absence balance at the time of plan enrollment, or HR can make a manual adjustment at any time.</span></span> 

- <span data-ttu-id="70f09-131">**ใช้ลำดับงานกับคำขอเวลาหยุดพัก**</span><span class="sxs-lookup"><span data-stu-id="70f09-131">**Apply a workflow to time-off requests.**</span></span>

     <span data-ttu-id="70f09-132">ลำดับงานอาจเป็นแบบกำหนดเองและนำไปใช้กับคำขอเวลาหยุดพักเพื่อตอบสนองความต้องการขององค์กร</span><span class="sxs-lookup"><span data-stu-id="70f09-132">A workflow can be customized and applied to time-off requests to meet the organization’s requirements.</span></span>  

- <span data-ttu-id="70f09-133">**ติดตามยอดดุลการลางานของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="70f09-133">**Track employee absence balances.**</span></span>

    <span data-ttu-id="70f09-134">พนักงาน ผู้จัดการของตน และ HR สามารถดูยอดดุลการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="70f09-134">Employees, their manager, and HR can view leave and absence balances.</span></span> <span data-ttu-id="70f09-135">HR สามารถใช้รายงานแบบโต้ตอบเพื่อติดตามการลงทะเบียนแผนและยอดดุลเวลาหยุดพักโดยเรียงตามชนิด</span><span class="sxs-lookup"><span data-stu-id="70f09-135">HR can use interactive reports to track plan enrollments and time-off balances by type.</span></span> 

- <span data-ttu-id="70f09-136">**ส่งคำขอเวลาหยุดพัก**</span><span class="sxs-lookup"><span data-stu-id="70f09-136">**Submit time-off requests.**</span></span>

    <span data-ttu-id="70f09-137">พนักงานสามารถส่งคำขอเวลาหยุดพักโดยเทียบกับชั่วโมงที่พร้อมใช้งานของตน</span><span class="sxs-lookup"><span data-stu-id="70f09-137">Employees can submit time-off requests against their available hours.</span></span> <span data-ttu-id="70f09-138">คำขอสามารถเป็นคำขอวันเดียวแบบง่ายหรือคำขอหลายวันที่มีชนิดการลางานและการขาดงานหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="70f09-138">Requests can be simple single-day requests or multiple-day requests that include multiple leave and absence types.</span></span> <span data-ttu-id="70f09-139">ถ้าลำดับงานไม่ได้เปิดใช้งาน คำขอจะได้รับอนุมัติโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="70f09-139">If a workflow isn't enabled, the requests are automatically approved.</span></span> <span data-ttu-id="70f09-140">ถ้ามีการเปิดใช้งานลำดับงาน การอนุมัติอาจเป็นแบบอัตโนมัติ หรืออาจต้องลงชื่อออกจากระบบ โดยขึ้นอยู่กับการตั้งค่าคอนฟิกลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="70f09-140">If a workflow is enabled, the approval can be automatic, or it can require sign-off, depending on the workflow configuration.</span></span>
