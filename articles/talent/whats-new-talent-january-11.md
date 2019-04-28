---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (11 มกราคม 2019)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a89ba455acbed9724da6826ac4d41c6a481490
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "856149"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a><span data-ttu-id="92bea-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (11 มกราคม 2019)</span><span class="sxs-lookup"><span data-stu-id="92bea-103">What's new or changed in Dynamics 365 for Talent Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92bea-104">**สร้าง 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="92bea-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="92bea-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="92bea-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="92bea-106">การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="92bea-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="92bea-107">ตรวจสอบคำขอลางานโดยการคาดการณ์ยอดดุลที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="92bea-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="92bea-108">การเปลี่ยนแปลงในการนำออกใช้นี้ช่วยให้พนักงานสามารถร้องขอเวลาลางานในอนาคตโดยไม่ต้องลบออกจากยอดคงเหลือปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92bea-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="92bea-109">ลำดับงานมาตรฐานจะใช้สำหรับคำขอในอนาคตใด ๆ</span><span class="sxs-lookup"><span data-stu-id="92bea-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="92bea-110">สำหรับข้อมูลเพิ่มเติม อ่านที่ [เวลาหยุดพักคงค้างตามชั่วโมงที่ทำงาน](leave-accrue-hours-worked.md)</span><span class="sxs-lookup"><span data-stu-id="92bea-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="92bea-111">ดูยอดดุลการลาที่คาดการณ์ใน ESS and People</span><span class="sxs-lookup"><span data-stu-id="92bea-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="92bea-112">คุณลักษณะนี้ทำให้สามารถดูยอดดุลสำหรับรอบระยะเวลาการลางานในอนาคตของ HR ผู้จัดการ และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="92bea-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="92bea-113">พนักงานสามารถดูยอดดุลในอนาคตในพื้นที่ทำงาน **ระบบพนักงานบริการตนเอง** และ HR มีสิทธิ์เข้าถึงข้อมูลเดียวกันโดยใช้พื้นที่ทำงาน **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="92bea-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="92bea-114">การแจ้งเตือนสำหรับการเปลี่ยนแปลงยอดดุลการลา</span><span class="sxs-lookup"><span data-stu-id="92bea-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="92bea-115">ยอดดุลการลาจะแสดงยอดดุลปัจจุบันของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="92bea-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="92bea-116">ยอดดุลในอนาคตจะพร้อมใช้งานในพื้นที่ทำงาน **ระบบพนักงานบริการตนเอง** และ **บุคคล** ด้วยการป้อน "เป็นวันที่" เพื่อคำนวณยอดดุลที่คาดการณ์</span><span class="sxs-lookup"><span data-stu-id="92bea-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="92bea-117">มีการเพิ่มการนำทางเพื่อดูยอดดุลที่คาดการณ์ไว้ในพื้นที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="92bea-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="92bea-118">บัตร **เวลาหยุดพัก** บนพื้นที่ทำงาน **ระบบพนักงานบริการตนเอง**</span><span class="sxs-lookup"><span data-stu-id="92bea-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="92bea-119">บัตร **การลางานและการขาดงาน** บนพื้นที่ทำงาน **ระบบบริการตนเองของผู้จัดการ**</span><span class="sxs-lookup"><span data-stu-id="92bea-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="92bea-120">หน้า **การลางานและการขาดงาน** บนพื้นที่ทำงาน **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="92bea-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="92bea-121">อนุญาตให้มีทศนิยมสำหรับแผนค่าตอบแทนผันแปร (แผนเงินสด)</span><span class="sxs-lookup"><span data-stu-id="92bea-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="92bea-122">รางวัลเงินสดผันแปรและแผนมีความยืดหยุ่นมากขึ้นสำหรับยอดเงินและการแทนที่ค่าด้วยจำนวนทศนิยม</span><span class="sxs-lookup"><span data-stu-id="92bea-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="92bea-123">ไม่สามารถเปลี่ยนแปลงวันที่ในการลงทะเบียนค่าตอบแทนผันแปรหลังจากบันทึกแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="92bea-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="92bea-124">การเปลี่ยนแปลงนี้อนุญาตให้อัพเดต (ขยาย หรือกำหนดวันหมดอายุ) วันที่สิ้นสุดของแผนหลังจากที่บันทึกแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="92bea-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="92bea-125">นอกจากนี้คุณยังสามารถเรียกใช้หรือยกเลิกการเรียกใช้ที่ขึ้นอยู่กับวันที่เริ่มต้นและวันที่สิ้นสุดของแผน</span><span class="sxs-lookup"><span data-stu-id="92bea-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="92bea-126">ข้อมูลค่าจ้างพร้อมใช้งานเมื่อมีการกำหนดบทบาทความปลอดภัยของผู้ดูแลค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="92bea-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="92bea-127">มีการอัพเดตบทบาทผู้ดูแลค่าจ้างให้มีสิทธิเข้าถึงข้อมูลค่าจ้างในระหว่างกระบวนการคำขอ</span><span class="sxs-lookup"><span data-stu-id="92bea-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="92bea-128">การบริการตนเองของพนักงาน | ลำดับชั้นของตำแหน่งที่เลื่อนจากไทล์ล้มเหลวในการเรียกโหนดหลัก</span><span class="sxs-lookup"><span data-stu-id="92bea-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="92bea-129">มีการเปลี่ยนแปลงเพื่อขจัดข้อผิดพลาดที่เกิดขึ้นเมื่อมีการเพิ่มลำดับชั้นของตำแหน่งไปยังพื้นที่ทำงานใหม่และนำทางภายในโครงสร้างองค์กร</span><span class="sxs-lookup"><span data-stu-id="92bea-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="92bea-130">ข้อความการตรวจสอบใหม่เมื่อลำดับหมายเลขบุคลากรมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="92bea-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="92bea-131">มีการเปลี่ยนแปลงเพื่ออธิบายว่ามีปัญหาใดเมื่อคุณจ้างพนักงานและหมายเลขบุคลากรถัดไปมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="92bea-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="92bea-132">พื้นที่ทำงานพนักงานบริการตนเองถูกเลือกเป็นหน้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="92bea-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="92bea-133">เมื่อมีการเลือกพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน** เป็นหน้าเริ่มต้นเริ่มแรกสำหรับผู้ใช้ และผู้ใช้นั้นๆ ไม่ได้ได้รับการกำหนดบทบาทพนักงาน ระบบจะเปลี่ยนเส้นทางไปยังแดชบอร์ดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="92bea-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="92bea-134">รหัสเหตุผลการสิ้นสุดการจ้างจะปรับปรุงเรกคอร์ดการมอบหมายตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="92bea-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="92bea-135">ในตอนนี้รหัสเหตุผลการสิ้นสุดการจ้างจะปรับปรุงการมอบหมายตำแหน่งงานขณะเลิกว่าจ้างพนักงานและสิ้นสุดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="92bea-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
