---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (16 กันยายน 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 16 กันยายน 2020
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14a4c08b0d223bc7fd8044354f5976388af9176b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467468"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="c6c37-103">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (16 กันยายน 2020)</span><span class="sxs-lookup"><span data-stu-id="c6c37-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c6c37-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="c6c37-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c6c37-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3557</span><span class="sxs-lookup"><span data-stu-id="c6c37-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="c6c37-106">ตัวเลขในวงเล็บถัดจากลักษณะการทำงานบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุน Lifecycle Services (LCS) สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="c6c37-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="c6c37-107">รวมอยู่ในการนำออกใช้นี้</span><span class="sxs-lookup"><span data-stu-id="c6c37-107">Included in this release</span></span>

-  [<span data-ttu-id="c6c37-108">มุมมองที่บันทึกไว้ - ความพร้อมใช้งานทั่วไป</span><span class="sxs-lookup"><span data-stu-id="c6c37-108">Saved views - general availability</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="c6c37-109">- สำหรับข้อมูลเพิ่มเติม ดูที่ [มุมมองที่บันทึกไว้](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views)</span><span class="sxs-lookup"><span data-stu-id="c6c37-109">- For more information, see [Saved views](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views).</span></span> 

- <span data-ttu-id="c6c37-110">ฟอร์ม **การดำเนินการของตำแหน่ง** มีกริดมิติที่อัปเดตและกล่องโต้ตอบใหม่ (469495)</span><span class="sxs-lookup"><span data-stu-id="c6c37-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="c6c37-111">ถ้าคุณกำหนดให้ **จำกัดการเข้าถึงข้อมูลของผู้ปฏิบัติงาน** เป็นใช่ใน **การเข้าถึงขั้นสูง** ใน **พารามิเตอร์ที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล** แบบฟอร์มสวัสดิการจะแสดงเฉพาะผู้ปฏิบัติงานที่เหมาะสมเท่านั้น (393384)</span><span class="sxs-lookup"><span data-stu-id="c6c37-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="c6c37-112">ตัวเลือกการสร้างปฏิทินใหม่ในเอนทิตี **WorkCalendar** (477055):</span><span class="sxs-lookup"><span data-stu-id="c6c37-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="c6c37-113">- เวลาสิ้นสุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6c37-113">- Default ending time</span></span><br><span data-ttu-id="c6c37-114">-    เวลาเริ่มต้นตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6c37-114">-    Default starting time</span></span><br><span data-ttu-id="c6c37-115">- วันศุกร์คือวันทำงานใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6c37-115">-  Is Friday working day</span></span><br><span data-ttu-id="c6c37-116">- วันจันทร์คือวันทำงานใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6c37-116">-  Is Monday working day</span></span><br><span data-ttu-id="c6c37-117">- วันเสาร์คือวันทำงานใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6c37-117">-  Is Saturday working day</span></span><br><span data-ttu-id="c6c37-118">- วันอาทิตย์คือวันทำงานใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6c37-118">- Is Sunday working day</span></span><br><span data-ttu-id="c6c37-119">- วันพฤหัสบดีคือวันทำงานใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6c37-119">- Is Thursday working day</span></span><br><span data-ttu-id="c6c37-120">- วันอังคารคือวันทำงานใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6c37-120">- Is Tuesday working day</span></span><br><span data-ttu-id="c6c37-121">- วันพุธคือวันทำงานใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6c37-121">- Is Wednesday working day</span></span><br><span data-ttu-id="c6c37-122">- รหัสวันหยุดในปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="c6c37-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="c6c37-123">ขณะนี้เอนทิตี **LeaveBankTransactionV1** รวมรหัสเหตุผล (477823)</span><span class="sxs-lookup"><span data-stu-id="c6c37-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="c6c37-124">ขณะนี้คุณสามารถบันทึกการบันทึกงาน (492923)</span><span class="sxs-lookup"><span data-stu-id="c6c37-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="c6c37-125">ขณะนี้มีการเผยแพร่ข้อมูลจาก **HCMWorkerContactEntity** (427620) เสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6c37-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="c6c37-126">แท็บด่วน **ค่าตอบแทน** แสดงอยู่ในขณะนี้สำหรับผู้ปฏิบัติงานที่เป็นผู้รับเหมาในฟอร์ม **การดำเนินการของผู้ปฏิบัติ** (482494)</span><span class="sxs-lookup"><span data-stu-id="c6c37-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="c6c37-127">ฟิลด์ **ระดับ** และ **แผน** ขณะนี้เป็นข้อบังคับถ้าคุณตั้งค่า **ค่าตอบแทนคงที่**</span><span class="sxs-lookup"><span data-stu-id="c6c37-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="c6c37-128">ข้อความแสดงข้อผิดพลาดจะแสดงขึ้นถ้าคุณปล่อยฟิลด์เหล่านี้ว่างไว้ (482497)</span><span class="sxs-lookup"><span data-stu-id="c6c37-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="c6c37-129">ฟิลด์ **ชนิดของแผน** ใน **สวัสดิการ** เป็นรายการแบบหล่นลงในขณะนี้ (488768)</span><span class="sxs-lookup"><span data-stu-id="c6c37-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="c6c37-130">ขณะนี้ผู้ดูแลระบบได้รับการแจ้งเตือนถ้าฟิลด์ที่กำหนดเองถูกลบออกจากทรัพยากรบุคคล (481408)</span><span class="sxs-lookup"><span data-stu-id="c6c37-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="c6c37-131">ในระหว่างกระบวนการสิ้นสุดการจ้างงานของพนักงาน ทรัพยากรบุคคลจะปฏิบัติตามที่คาดไว้และไม่เปลี่ยนบริษัทที่เลือกหลังจากที่ปรากฏในการล็อก (479877)</span><span class="sxs-lookup"><span data-stu-id="c6c37-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="c6c37-132">ผู้จัดการไม่สามารถเพิ่มคอลัมน์หมายเลขผ่านการตั้งค่าส่วนบุคคล (485317) ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="c6c37-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="c6c37-133">ผู้จัดการไม่สามารถลบตัวกรองช่วงข้อมูลจากหมายเลขรหัสที่หมดอายุ (485321) ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="c6c37-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="c6c37-134">เมื่อฟิลด์ **รายงานไปยัง** ว่างเปล่า รายละเอียดตำแหน่งยังคงแสดงขึ้นเมื่อเลื่อนเมาส์ไปยังตำแหน่ง (433328)</span><span class="sxs-lookup"><span data-stu-id="c6c37-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="c6c37-135">ขณะนี้พนักงานสามารถดูข้อมูลแผนสวัสดิการในบริการตนเองของพนักงาน (481676)</span><span class="sxs-lookup"><span data-stu-id="c6c37-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="c6c37-136">ขณะนี้พนักงานสามารถดูหลักสูตรที่ลงทะเบียนแล้วทั้งหมด (429048)</span><span class="sxs-lookup"><span data-stu-id="c6c37-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="c6c37-137">ขณะนี้คุณสามารถจำกัดตัวเลือกการดูสำหรับหน้า **ใบรับรองของวิชาชีพ**</span><span class="sxs-lookup"><span data-stu-id="c6c37-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="c6c37-138">คุณสามารถจำกัดการดูตัวเลือกสำหรับนิติบุคคลปัจจุบันตามสถานะผู้ปฏิบัติงานและตามชนิดผู้ปฏิบัติงาน (451501)</span><span class="sxs-lookup"><span data-stu-id="c6c37-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="c6c37-139">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c6c37-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="c6c37-140">แอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="c6c37-140">Human Resources app in Teams</span></span>

<span data-ttu-id="c6c37-141">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c6c37-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="c6c37-142">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="c6c37-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="c6c37-143">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="c6c37-143">For more information, see:</span></span>

- <span data-ttu-id="c6c37-144">[การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 1</span><span class="sxs-lookup"><span data-stu-id="c6c37-144">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="c6c37-145">[แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="c6c37-145">[Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="c6c37-146">คุณลักษณะรุ่นพรีวิวของแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="c6c37-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="c6c37-147">**การแจ้งเตือน**: ผู้ส่งและผู้อนุมัติที่ส่งคำขอการลาหยุดจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="c6c37-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="c6c37-148">ผู้อนุมัติสามารถอนุมัติหรือปฏิเสธคำขอการลาหยุดได้</span><span class="sxs-lookup"><span data-stu-id="c6c37-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="c6c37-149">ผู้ส่งจะได้รับการแจ้งเตือนถ้าคำขอได้รับการอนุมัติหรือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="c6c37-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="c6c37-150">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="c6c37-150">For more information, see:</span></span>
   - <span data-ttu-id="c6c37-151">[การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2</span><span class="sxs-lookup"><span data-stu-id="c6c37-151">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="c6c37-152">[เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="c6c37-152">[Enable notifications for the Human Resources app in Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="c6c37-153">[เปิดหรือปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้แต่ละราย](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="c6c37-153">[Turn Teams notifications on or off for individual users](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="c6c37-154">[การแจ้งเตือนของ Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="c6c37-154">[Teams notifications](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="c6c37-155">[ดูปฏิทินการลางานของทีมของคุณ](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="c6c37-155">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="c6c37-156">**ปฏิทินการลาหยุดของผู้จัดการ**: ผู้จัดการสามารถดูการลาหยุดที่อนุมัติและที่ค้างอยู่สำหรับผู้ใต้บังคับบัญชาโดยตรงของตนในมุมมองปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="c6c37-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="c6c37-157">มุมมองนี้จะทำให้เข้าใจง่ายเมื่อสมาชิกในทีมของตนไม่มาทำงาน</span><span class="sxs-lookup"><span data-stu-id="c6c37-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="c6c37-158">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="c6c37-158">For more information, see:</span></span>
   - <span data-ttu-id="c6c37-159">[การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2</span><span class="sxs-lookup"><span data-stu-id="c6c37-159">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="c6c37-160">[ดูปฏิทินการลางานของทีมของคุณ](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) ในคู่มือ Human Resources</span><span class="sxs-lookup"><span data-stu-id="c6c37-160">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="c6c37-161">ตัวเลือกการตั้งค่าคอนฟิกเพื่อกำหนดตำแหน่งรายการงานที่กำหนดให้กับฉัน (477004)</span><span class="sxs-lookup"><span data-stu-id="c6c37-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="c6c37-162">ขณะนี้ตัวเลือกใหม่จะพร้อมใช้งานในการกำหนดตำแหน่งรายการของ **รายการงานที่กำหนดให้กับฉัน** ในคอลัมน์ทางด้านขวาของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="c6c37-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="c6c37-163">เมื่อมีการเปลี่ยนแปลงนี้ รายการงานและรายการสิ่งที่ต้องทำทั้งหมดแสดงในพื้นที่เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c6c37-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="c6c37-164">เปิดใช้งานฟังก์ชันนี้โดยการเปิด **พรีวิว - การปรับปรุงประสบการณ์ของลำดับงาน** ในการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="c6c37-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="c6c37-165">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดคุณลักษณะพรีวิว ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)</span><span class="sxs-lookup"><span data-stu-id="c6c37-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="c6c37-166">คุณลักษณะนี้จะส่งเสริมตัวเลือกลำดับงานที่จะปรากฏในแบบฟอร์มการดำเนินการด้านบุคลากร</span><span class="sxs-lookup"><span data-stu-id="c6c37-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="c6c37-167">ตัวเลือกลำดับงานจะปรากฎในแท็บด่วนการดำเนินการเพื่อให้สามารถเข้าถึงได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="c6c37-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="c6c37-168">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="c6c37-168">For more information, see:</span></span> 

- <span data-ttu-id="c6c37-169">[การปรับปรุงประสบการณ์การใช้งานลำดับงานการจัดการองค์กรและบุคลากร](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) ในแผน Dynamics 365 2020 การนำออกใช้เวฟ 2</span><span class="sxs-lookup"><span data-stu-id="c6c37-169">[Organization and personnel management workflow experience enhancements](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![รายการงานที่กำหนดให้กับฉัน](./media/hr-workflow-work-items-assigned-to-me.png)

![การเข้าถึงด่วนของรายการลำดับงาน](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="c6c37-172">ปฏิทินการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="c6c37-172">Leave and absence calendar</span></span>

<span data-ttu-id="c6c37-173">การนำออกใช้นี้มีตัวเลือกปฏิทินเพิ่มเติมสำหรับปฏิทินการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="c6c37-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="c6c37-174">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ดูทีมงานและปฏิทินของบริษัท](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar)</span><span class="sxs-lookup"><span data-stu-id="c6c37-174">For more information, see [View team and company calendars](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c6c37-175">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="c6c37-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="c6c37-176">เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="c6c37-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="c6c37-177">เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="c6c37-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="c6c37-178">รหัสเหตุผลของการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c6c37-178">Benefits management reason codes</span></span>

<span data-ttu-id="c6c37-179">รหัสเหตุผลของการจัดการสวัสดิการจะมีการรวมเข้ากับรหัสเหตุผลที่มีอยู่ใน Human Resources ในเร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="c6c37-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="c6c37-180">ถ้าคุณสร้างรหัสเหตุผลไว้ในการจัดการสวัสดิการที่มีอักขระเกินกว่า 15 ตัว คุณต้องเปลี่ยนชื่อของรหัสเหตุผลในแบบฟอร์ม **รหัสเหตุผล** ของการจัดการสวัสดิการเป็นอักขระ15 ตัวหรือน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="c6c37-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="c6c37-181">หลังจากที่คุณอัปเดตชื่อ รหัสเหตุผลจะปรากฏขึ้นภายใต้แบบฟอร์มรหัสเหตุผลที่มีอยู่ในการจัดการบุคลากร</span><span class="sxs-lookup"><span data-stu-id="c6c37-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="c6c37-182">การเปลี่ยนแปลงนี้จะพร้อมใช้งานในอนาคตและจะไม่มีผลกระทบต่อฟังก์ชันการทำงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="c6c37-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6c37-183">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="c6c37-183">See also</span></span>

[<span data-ttu-id="c6c37-184">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="c6c37-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="c6c37-185">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="c6c37-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="c6c37-186">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="c6c37-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="c6c37-187">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="c6c37-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]