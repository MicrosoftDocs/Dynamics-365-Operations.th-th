---
title: ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน
description: 'ขั้นตอนนี้สาธิตว่าผู้ปฏิบัติงานสามารถลงทะเบียนในสวัสดิการอันเดียวหรือมากกว่านั้นได้อย่างไร ตลอดจนผู้ปฏิบัติงานหลายคนสามารถลงทะเบียนได้ในสวัสดิการ '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92da6d24f3fc4282de5673a8155b6ab6316e55aa
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510439"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="c00e5-103">ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c00e5-103">Enroll and remove benefits from workers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c00e5-104">ขั้นตอนนี้สาธิตว่าผู้ปฏิบัติงานสามารถลงทะเบียนในสวัสดิการอันเดียวหรือมากกว่านั้นได้อย่างไร ตลอดจนผู้ปฏิบัติงานหลายคนสามารถลงทะเบียนได้ในสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="c00e5-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="c00e5-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c00e5-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="c00e5-106">การลงทะเบียนผู้ปฏิบัติงานคนเดียวในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="c00e5-107">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="c00e5-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="c00e5-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c00e5-109">คลิก สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-109">Click Benefits.</span></span>
4. <span data-ttu-id="c00e5-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c00e5-110">Click New.</span></span>
5. <span data-ttu-id="c00e5-111">ในฟิลด์สวัสดิการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c00e5-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="c00e5-112">ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c00e5-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="c00e5-113">ในฟิลด์วันที่สิ้นสุดความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c00e5-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="c00e5-114">ขยายส่วนผู้รับผลประโยชน์ ถ้าหากผู้รับผลประโยชน์จำเป็นต้องเพิ่มเข้าไปในสวัสดีการ </span><span class="sxs-lookup"><span data-stu-id="c00e5-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="c00e5-115">คุณสามารถเพิ่มผู้อยู่ในอุปการะจากหน้านี้ถ้าเกี่ยวข้องกับตัวสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="c00e5-116">นอกจากนี้คุณยังสามารถแก้ไขรายละเอียดของการลงทะเบียนสวัสดิการ หรือลบการลงทะเบียนบนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="c00e5-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="c00e5-117">เมื่อคุณเสร็จสิ้นการทำการเปลี่ยนแปลงกับการลงทะเบียนสวัสดิการ ปิดหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c00e5-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="c00e5-118">การลงทะเบียนผู้ปฏิบัติงานหลายรายในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="c00e5-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c00e5-119">Close the page.</span></span>
2. <span data-ttu-id="c00e5-120">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="c00e5-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="c00e5-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c00e5-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c00e5-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c00e5-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c00e5-124">คลิก ลงทะเบียนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="c00e5-125">ในฟิลด์สวัสดิการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c00e5-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="c00e5-126">ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c00e5-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="c00e5-127">ในฟิลด์วันที่สิ้นสุดความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c00e5-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="c00e5-128">คลิกลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="c00e5-128">Click Enroll.</span></span>
11. <span data-ttu-id="c00e5-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c00e5-129">Close the page.</span></span>
12. <span data-ttu-id="c00e5-130">ไปที่ฝ่ายบุคคล > สวัสดิการ > การลงทะเบียน > ผลการลงทะเบียนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c00e5-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="c00e5-131">ค้นหาบันทึกผลสวัสดิการที่กำลังมองหาอยู่</span><span class="sxs-lookup"><span data-stu-id="c00e5-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="c00e5-132">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c00e5-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="c00e5-133">หน้านี้จะช่วยให้คุณดูพนักงานที่ได้ลงทะเบียนในสวัสดิการและพนักงานที่ยังไม่ได้ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="c00e5-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

