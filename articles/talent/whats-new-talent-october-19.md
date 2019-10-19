---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent - Core HR (16 ตุลาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Talent - Core HR
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
ms.openlocfilehash: 13e89faa3f8470125010ccdb40a6f01c0a9c4fe7
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008788"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-19-2018"></a><span data-ttu-id="2bed7-103">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent: Core HR (19 ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="2bed7-103">What's new or changed in Dynamics 365 Talent: Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="2bed7-104">**สร้าง 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="2bed7-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="2bed7-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="2bed7-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="2bed7-106">อนุญาตให้ผู้จัดการสามารถอัพเดตคำขอการลาหยุดได้</span><span class="sxs-lookup"><span data-stu-id="2bed7-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="2bed7-107">คำขอการลาหยุดของพนักงานอาจจำเป็นต้องถูกปรับปรุง หลังจากที่อนุมัติโดยใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="2bed7-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="2bed7-108">ในหลายกรณี ผู้จัดการทำการปรับปรุงเหล่านี้ในนามของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="2bed7-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="2bed7-109">คุณลักษณะใหม่นี้มีความสามารถสำหรับผู้จัดการในการอัพเดตคำขอการลาหยุดหรือยกเลิกการลาหยุดในนามของพนักงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="2bed7-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="2bed7-110">ความสามารถนี้ถูกควบคุมโดยพารามิเตอร์ **ทำงานในนาม** ที่สามารถตั้งค่าในหน้า **พารามิเตอร์ทรัพยากรบุคคล** ได้</span><span class="sxs-lookup"><span data-stu-id="2bed7-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="2bed7-111">อนุญาตให้ HR สามารถอัพเดตคำขอการลาหยุดได้</span><span class="sxs-lookup"><span data-stu-id="2bed7-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="2bed7-112">คล้ายกับลักษณะการทำงานข้างต้น คำขอการลาหยุดของพนักงานอาจจำเป็นต้องถูกอัพเดตโดย HR หลังจากที่อนุมัติแล้วก่อนหน้านี้โดยใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="2bed7-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="2bed7-113">คุณลักษณะนี้มีความสามารถสำหรับผู้ใช้ HR เพื่ออัพเดตคำขอการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="2bed7-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="2bed7-114">มีการเปิดใช้งานความสามารถในพื้นที่ทำงาน **บุคลากร** และบนหน้า **ผู้ปฏิบัติงาน** โดยใช้ตัวเลือกใหม่ที่เรียกว่า **ดูเวลาหยุดพัก**</span><span class="sxs-lookup"><span data-stu-id="2bed7-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="2bed7-115">บนหน้าเหล่านั้น ผู้ใช้ HR สามารถดูคำขอ และอัพเดตธุรกรรมเวลาหยุดพัก ที่คล้ายคลึงกับวิธีที่ผู้จัดการสามารถทำการดำเนินการเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2bed7-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="2bed7-116">หน้าที่ด้านความปลอดภัยที่ควบคุมการเข้าถึงฟังก์ชันนี้คือ:</span><span class="sxs-lookup"><span data-stu-id="2bed7-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="2bed7-117">หน้าที่: รักษากระบวนการลางานและการขาดงานสำหรับผู้ปฏิบัติงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2bed7-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="2bed7-118">สิทธิ์: รักษาคำขอลางานและขาดงานสำหรับผู้ปฏิบัติงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2bed7-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="2bed7-119">การเปลี่ยนแปลงอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2bed7-119">Other changes</span></span>
<span data-ttu-id="2bed7-120">มีการทำการปรับปรุงต่อไปนี้ในรุ่นนี้:</span><span class="sxs-lookup"><span data-stu-id="2bed7-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="2bed7-121">การเปลี่ยนแปลงต่อการดำเนินการจ้างงานของผู้ปฏิบัติงานเพื่อให้พวกเขาไม่ "ติด" ในสถานะ **ลำดับงานเสร็จสมบูรณ์** อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="2bed7-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="2bed7-122">ขณะนี้ คุณสามารถสร้างเรกคอร์ดการจ้างงาน โดยไม่มีวันที่เริ่มต้นการจ้างงานได้</span><span class="sxs-lookup"><span data-stu-id="2bed7-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="2bed7-123">วันที่ลงทะเบียน Dynamics 365 Talent สำหรับหลักสูตรที่แสดงในระบบบริการตนเองของพนักงาน ตอนนี้ใช้ออฟเซ็ตโซนเวลาสำหรับวันที่</span><span class="sxs-lookup"><span data-stu-id="2bed7-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="2bed7-124">ไฟล์ Excel สามารถนำเข้าได้หลายครั้ง โดยไม่มีข้อผิดพลาดใดๆ โดยใช้ **เอนทิตีพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="2bed7-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="2bed7-125">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="2bed7-125">Known issue</span></span>

- <span data-ttu-id="2bed7-126">**ปัญหา**: เมื่อเพิ่มสิ่งที่แนบมาใหม่กับผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** จะกลายเป็นสีเทา</span><span class="sxs-lookup"><span data-stu-id="2bed7-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="2bed7-127">**วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่าก FactBoxes บนหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="2bed7-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="2bed7-128">ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2bed7-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="2bed7-129">(ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)</span><span class="sxs-lookup"><span data-stu-id="2bed7-129">(This issue will be fixed in the next platform update.)</span></span>
