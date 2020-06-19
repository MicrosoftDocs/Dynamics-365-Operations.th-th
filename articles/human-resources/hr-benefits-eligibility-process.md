---
title: กระบวนการการมีสิทธิ์ในสวัสดิการ
description: 'กระบวนงานนี้แสดงว่ากระบวนงานการมีสิทธิ์ในสวัสดิการทำงานอย่างไร '
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: d23dcf4a16979b14ddf58b54e812f21e6698dfc7
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430819"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="8f7c4-103">กระบวนการการมีสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="8f7c4-103">Benefit eligibility process</span></span>

<span data-ttu-id="8f7c4-104">กระบวนงานนี้แสดงว่ากระบวนงานการมีสิทธิ์ในสวัสดิการทำงานอย่างไร </span><span class="sxs-lookup"><span data-stu-id="8f7c4-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="8f7c4-105">เมื่อกระบวนการเสร็จสมบูรณ์ คุณสามารถดูผลลัพธ์ </span><span class="sxs-lookup"><span data-stu-id="8f7c4-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="8f7c4-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="8f7c4-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8f7c4-107">ไปที่ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="8f7c4-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="8f7c4-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8f7c4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8f7c4-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8f7c4-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8f7c4-110">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8f7c4-110">Click Edit.</span></span>
5. <span data-ttu-id="8f7c4-111">ในฟิลด์กฎการมีคุณสมบัติที่เหมาะสม กรุณาเลือก 'ตามกฎ'</span><span class="sxs-lookup"><span data-stu-id="8f7c4-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="8f7c4-112">ในฟิลด์ชนิดกฎ กรุณาเลือกกฏนโยบายของสวัสดิการที่ต้องการในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="8f7c4-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="8f7c4-113">ในบานหน้าต่างการดำเนินการ คลิกสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="8f7c4-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="8f7c4-114">คลิก สร้างการตั้งค่าคอนฟิกเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="8f7c4-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="8f7c4-115">ในฟิลด์เหตุการณ์ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8f7c4-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="8f7c4-116">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8f7c4-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="8f7c4-117">ในฟิลด์ชนิดเหตุการณ์ ให้เลือก 'เปิดการลงทะเบียน'</span><span class="sxs-lookup"><span data-stu-id="8f7c4-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="8f7c4-118">ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="8f7c4-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="8f7c4-119">ในฟิลด์วันที่เริ่มต้นรอบเวลาการลงทะเบียน ให้ระบุวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="8f7c4-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="8f7c4-120">เติมตัวเลขลงในช่องจำนวนวันที่จะลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="8f7c4-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="8f7c4-121">คลิก สร้างเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="8f7c4-121">Click Create event.</span></span>
16. <span data-ttu-id="8f7c4-122">คลิก เพิ่มในแท็บด่วนผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="8f7c4-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="8f7c4-123">ในการนำเสนอโดยฟิลด์ชนิด เลือก 'พนักงาน'</span><span class="sxs-lookup"><span data-stu-id="8f7c4-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="8f7c4-124">ในฟิลด์นิติบุคคล ให้เลือก 'นิติบุคคลปัจจุบัน'</span><span class="sxs-lookup"><span data-stu-id="8f7c4-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="8f7c4-125">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="8f7c4-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="8f7c4-126">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8f7c4-126">Click OK.</span></span>
21. <span data-ttu-id="8f7c4-127">คลิกกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="8f7c4-127">Click Process.</span></span>
22. <span data-ttu-id="8f7c4-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8f7c4-128">Click OK.</span></span>
23. <span data-ttu-id="8f7c4-129">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="8f7c4-129">Refresh the page.</span></span>
24. <span data-ttu-id="8f7c4-130">คลิกแสดงผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="8f7c4-130">Click Show results.</span></span>
25. <span data-ttu-id="8f7c4-131">เปิด สถานะตัวกรองคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="8f7c4-131">Open Status column filter.</span></span>
26. <span data-ttu-id="8f7c4-132">เรียงลำดับจาก ก ถึง ฮ</span><span class="sxs-lookup"><span data-stu-id="8f7c4-132">Sort A to Z</span></span>

