---
title: ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน
description: 'ขั้นตอนนี้สาธิตว่าผู้ปฏิบัติงานสามารถลงทะเบียนในสวัสดิการอันเดียวหรือมากกว่านั้นได้อย่างไร ตลอดจนผู้ปฏิบัติงานหลายคนสามารถลงทะเบียนได้ในสวัสดิการ '
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 13e32c9bc77470d6b8e157e7a7805d3d72850478
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114410"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="f7efd-103">ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f7efd-103">Enroll and remove benefits from workers</span></span>



<span data-ttu-id="f7efd-104">ขั้นตอนนี้สาธิตว่าผู้ปฏิบัติงานสามารถลงทะเบียนในสวัสดิการอันเดียวหรือมากกว่านั้นได้อย่างไร ตลอดจนผู้ปฏิบัติงานหลายคนสามารถลงทะเบียนได้ในสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="f7efd-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="f7efd-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="f7efd-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="f7efd-106">การลงทะเบียนผู้ปฏิบัติงานคนเดียวในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="f7efd-107">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7efd-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="f7efd-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f7efd-109">คลิก สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-109">Click Benefits.</span></span>
4. <span data-ttu-id="f7efd-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f7efd-110">Click New.</span></span>
5. <span data-ttu-id="f7efd-111">ในฟิลด์สวัสดิการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f7efd-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="f7efd-112">ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f7efd-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="f7efd-113">ในฟิลด์วันที่สิ้นสุดความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f7efd-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="f7efd-114">ขยายส่วนผู้รับผลประโยชน์ ถ้าหากผู้รับผลประโยชน์จำเป็นต้องเพิ่มเข้าไปในสวัสดีการ </span><span class="sxs-lookup"><span data-stu-id="f7efd-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="f7efd-115">คุณสามารถเพิ่มผู้อยู่ในอุปการะจากหน้านี้ถ้าเกี่ยวข้องกับตัวสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="f7efd-116">นอกจากนี้คุณยังสามารถแก้ไขรายละเอียดของการลงทะเบียนสวัสดิการ หรือลบการลงทะเบียนบนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="f7efd-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="f7efd-117">เมื่อคุณเสร็จสิ้นการทำการเปลี่ยนแปลงกับการลงทะเบียนสวัสดิการ ปิดหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f7efd-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="f7efd-118">การลงทะเบียนผู้ปฏิบัติงานหลายรายในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="f7efd-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7efd-119">Close the page.</span></span>
2. <span data-ttu-id="f7efd-120">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7efd-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="f7efd-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7efd-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f7efd-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f7efd-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f7efd-124">คลิก ลงทะเบียนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="f7efd-125">ในฟิลด์สวัสดิการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f7efd-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="f7efd-126">ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f7efd-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="f7efd-127">ในฟิลด์วันที่สิ้นสุดความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f7efd-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="f7efd-128">คลิกลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7efd-128">Click Enroll.</span></span>
11. <span data-ttu-id="f7efd-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7efd-129">Close the page.</span></span>
12. <span data-ttu-id="f7efd-130">ไปที่ฝ่ายบุคคล > สวัสดิการ > การลงทะเบียน > ผลการลงทะเบียนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="f7efd-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="f7efd-131">ค้นหาบันทึกผลสวัสดิการที่กำลังมองหาอยู่</span><span class="sxs-lookup"><span data-stu-id="f7efd-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="f7efd-132">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7efd-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="f7efd-133">หน้านี้จะช่วยให้คุณดูพนักงานที่ได้ลงทะเบียนในสวัสดิการและพนักงานที่ยังไม่ได้ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7efd-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

