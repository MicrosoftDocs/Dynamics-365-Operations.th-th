---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (16 ตุลาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 51cfe8a92d1ac611e946934fe8ebbc99053788f1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "858364"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a><span data-ttu-id="b974d-103">มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (19 ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="b974d-103">What's new or changed in Dynamics 365 for Talent Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="b974d-104">**สร้าง 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="b974d-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="b974d-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="b974d-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="b974d-106">อนุญาตให้ผู้จัดการสามารถอัพเดตคำขอการลาหยุดได้</span><span class="sxs-lookup"><span data-stu-id="b974d-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="b974d-107">คำขอการลาหยุดของพนักงานอาจจำเป็นต้องถูกปรับปรุง หลังจากที่อนุมัติโดยใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="b974d-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="b974d-108">ในหลายกรณี ผู้จัดการทำการปรับปรุงเหล่านี้ในนามของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b974d-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="b974d-109">คุณลักษณะใหม่นี้มีความสามารถสำหรับผู้จัดการในการอัพเดตคำขอการลาหยุดหรือยกเลิกการลาหยุดในนามของพนักงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b974d-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="b974d-110">ความสามารถนี้ถูกควบคุมโดยพารามิเตอร์ **ทำงานในนาม** ที่สามารถตั้งค่าในหน้า **พารามิเตอร์ทรัพยากรบุคคล** ได้</span><span class="sxs-lookup"><span data-stu-id="b974d-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="b974d-111">อนุญาตให้ HR สามารถอัพเดตคำขอการลาหยุดได้</span><span class="sxs-lookup"><span data-stu-id="b974d-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="b974d-112">คล้ายกับลักษณะการทำงานข้างต้น คำขอการลาหยุดของพนักงานอาจจำเป็นต้องถูกอัพเดตโดย HR หลังจากที่อนุมัติแล้วก่อนหน้านี้โดยใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="b974d-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="b974d-113">คุณลักษณะนี้มีความสามารถสำหรับผู้ใช้ HR เพื่ออัพเดตคำขอการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="b974d-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="b974d-114">มีการเปิดใช้งานความสามารถในพื้นที่ทำงาน **บุคลากร** และบนหน้า **ผู้ปฏิบัติงาน** โดยใช้ตัวเลือกใหม่ที่เรียกว่า **ดูเวลาหยุดพัก**</span><span class="sxs-lookup"><span data-stu-id="b974d-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="b974d-115">บนหน้าเหล่านั้น ผู้ใช้ HR สามารถดูคำขอ และอัพเดตธุรกรรมเวลาหยุดพัก ที่คล้ายคลึงกับวิธีที่ผู้จัดการสามารถทำการดำเนินการเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b974d-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="b974d-116">หน้าที่ด้านความปลอดภัยที่ควบคุมการเข้าถึงฟังก์ชันนี้คือ:</span><span class="sxs-lookup"><span data-stu-id="b974d-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="b974d-117">หน้าที่: รักษากระบวนการลางานและการขาดงานสำหรับผู้ปฏิบัติงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b974d-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="b974d-118">สิทธิ์: รักษาคำขอลางานและขาดงานสำหรับผู้ปฏิบัติงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b974d-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="b974d-119">การเปลี่ยนแปลงอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b974d-119">Other changes</span></span>
<span data-ttu-id="b974d-120">มีการทำการปรับปรุงต่อไปนี้ในรุ่นนี้:</span><span class="sxs-lookup"><span data-stu-id="b974d-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="b974d-121">การเปลี่ยนแปลงต่อการดำเนินการจ้างงานของผู้ปฏิบัติงานเพื่อให้พวกเขาไม่ "ติด" ในสถานะ **ลำดับงานเสร็จสมบูรณ์** อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="b974d-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="b974d-122">ขณะนี้ คุณสามารถสร้างเรกคอร์ดการจ้างงาน โดยไม่มีวันที่เริ่มต้นการจ้างงานได้</span><span class="sxs-lookup"><span data-stu-id="b974d-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="b974d-123">วันที่ลงทะเบียน Dynamics 365 Talent สำหรับหลักสูตรที่แสดงไว้ในการบริการตนเองของพนักงาน ในขณะนี้ใช้ออฟเซ็ตโซนเวลาจนถึงวันที่</span><span class="sxs-lookup"><span data-stu-id="b974d-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="b974d-124">ไฟล์ Excel สามารถนำเข้าได้หลายครั้ง โดยไม่มีข้อผิดพลาดใดๆ โดยใช้ **เอนทิตีพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="b974d-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="b974d-125">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="b974d-125">Known issue</span></span>

- <span data-ttu-id="b974d-126">**ปัญหา**: เมื่อเพิ่มสิ่งที่แนบมาใหม่กับผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** จะกลายเป็นสีเทา</span><span class="sxs-lookup"><span data-stu-id="b974d-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="b974d-127">**วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่าก FactBoxes บนหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="b974d-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="b974d-128">ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b974d-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="b974d-129">(ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)</span><span class="sxs-lookup"><span data-stu-id="b974d-129">(This issue will be fixed in the next platform update.)</span></span>
