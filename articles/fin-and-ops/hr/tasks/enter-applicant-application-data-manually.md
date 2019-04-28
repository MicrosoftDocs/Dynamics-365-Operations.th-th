---
title: ป้อนข้อมูลผู้สมัครและแอพลิเคชันด้วยตนเอง
description: 'ขั้นตอนนี้แสดงวิธีการรักษาข้อมูลเกี่ยวกับผู้สมัครและใบสมัครของผู้สมัคร '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea61e3c1d76ade6e0d694b4b521e4be76fc8799d
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "855878"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="b2e2f-103">ป้อนข้อมูลผู้สมัครและแอพลิเคชันด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b2e2f-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2e2f-104">ขั้นตอนนี้แสดงวิธีการรักษาข้อมูลเกี่ยวกับผู้สมัครและใบสมัครของผู้สมัคร </span><span class="sxs-lookup"><span data-stu-id="b2e2f-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="b2e2f-105">คุณสามารถป้อน และรักษาข้อมูลส่วนบุคคล วันนัดสัมภาษณ์ และเวลา การอ้างอิง ความสามารถ และคำขอที่พักสำหรับผู้สมัคร </span><span class="sxs-lookup"><span data-stu-id="b2e2f-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="b2e2f-106">คุณสามารถปรับปรุงสถานะใบสมัครของผู้สมัครงาน และสร้างจดหมายหรือข้อความอีเมลเพื่อสื่อสารกับผู้สมัคร </span><span class="sxs-lookup"><span data-stu-id="b2e2f-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="b2e2f-107">เมื่อคุณสร้างเรกคอร์ดผู้สมัคร เรกคอร์ดบุคคลสำหรับผู้สมัครจะถูกสร้างขึ้นในสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="b2e2f-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="b2e2f-108">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="b2e2f-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="b2e2f-109">สร้างเรกคอร์ดผู้สมัครใหม่</span><span class="sxs-lookup"><span data-stu-id="b2e2f-109">Create a new applicant record</span></span>
1. <span data-ttu-id="b2e2f-110">ไปที่ทรัพยากรบุคคล > การสรรหาบุคคลากร > ผู้สมัคร > ผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b2e2f-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="b2e2f-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b2e2f-111">Click New.</span></span>
3. <span data-ttu-id="b2e2f-112">ในฟิลด์ชื่อแรก ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2e2f-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="b2e2f-113">ในฟิลด์นามสกุล ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2e2f-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="b2e2f-114">คุณสามารถป้อนข้อมูลผู้สมัครเพิ่มเติมถ้าพร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="b2e2f-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="b2e2f-115">ตัวอย่างเช่น ข้อมูลสามารถรวมถึง ระดับการศึกษาสูงสุดของผู้สมัคร ตำแหน่งงานปัจจุบัน หรือนายจ้างก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b2e2f-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="b2e2f-116">สลับการขยายของส่วนของข้อมูลผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="b2e2f-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="b2e2f-117">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b2e2f-117">Click Add.</span></span>
7. <span data-ttu-id="b2e2f-118">ในฟิลด์คำอธิบาย ให้พิมพ์อีเมลที่ใช้ในการสื่อสาร</span><span class="sxs-lookup"><span data-stu-id="b2e2f-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="b2e2f-119">ในฟิลด์ชนิด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b2e2f-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="b2e2f-120">ในฟิลด์หมายเลข/ที่อยู่ผู้ติดต่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2e2f-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="b2e2f-121">ที่อยู่ของอีเมลนี้จะใช้ในการสร้างข้อความอีเมลสื่อสารกับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b2e2f-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="b2e2f-122">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b2e2f-122">Click Add.</span></span>
11. <span data-ttu-id="b2e2f-123">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2e2f-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="b2e2f-124">ในฟิลด์หมายเลข/ที่อยู่ผู้ติดต่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2e2f-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="b2e2f-125">ข้อมูลส่วนตัวของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b2e2f-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="b2e2f-126">คุณสามารถป้อนข้อมูลส่วนบุคคลเพิ่มเติมสำหรับผู้สมัคร ถ้าจำเป็น </span><span class="sxs-lookup"><span data-stu-id="b2e2f-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="b2e2f-127">ตัวอย่างเช่น ซึ่งสามารถรวมถึงวันเกิด เชื้อชาติ เพศ หรือสถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="b2e2f-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="b2e2f-128">ในบานหน้าต่างการดำเนินการ คลิก ความสามารถ</span><span class="sxs-lookup"><span data-stu-id="b2e2f-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="b2e2f-129">คุณสามารถป้อนโพรไฟล์ความสามารถของผู้สมัคร รวมทั้งทักษะของพวกเขา ประสบการณ์ทำงาน การศึกษา แบบทดสอบ หรือประกาศนียบัตร</span><span class="sxs-lookup"><span data-stu-id="b2e2f-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="b2e2f-130">ข้อมูลนี้สามารถใช้วางแผนทักษะของผู้สมัครเพื่อทักษะที่เชื่อมโยงกับงานกำหนดไว้ในข้อมูลของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="b2e2f-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="b2e2f-131">สร้างใบสมัครสำหรับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b2e2f-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="b2e2f-132">คลิก ใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="b2e2f-132">Click Applications.</span></span>
2. <span data-ttu-id="b2e2f-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b2e2f-133">Click New.</span></span>
3. <span data-ttu-id="b2e2f-134">ในฟิลด์โครงการสรรหาบุคลากร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b2e2f-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b2e2f-135">โดยการเลือกโครงการสรรหาบุคลากร ผู้สมัครจะเชื่อมโยงกับการเปิดเฉพาะที่รวมอยู่ในโครงการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="b2e2f-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="b2e2f-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b2e2f-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b2e2f-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b2e2f-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2e2f-138">โดยค่าเริ่มต้น งานและแผนกขึ้นอยู่กับโครงการสรรหาบุคลากรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b2e2f-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="b2e2f-139">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b2e2f-139">Click Save.</span></span>
    * <span data-ttu-id="b2e2f-140">หลังจากบันทึกแอพลิเคชัน คุณสามารถแนบเอกสาร รวมทั้งของประสบการณ์ของผู้สมัคร รางวัล และจดหมายปะหน้า</span><span class="sxs-lookup"><span data-stu-id="b2e2f-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

