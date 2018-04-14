--- 
title: "ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน"
description: "ขั้นตอนนี้สาธิตว่าผู้ปฏิบัติงานสามารถลงทะเบียนในสวัสดิการอันเดียวหรือมากกว่านั้นได้อย่างไร ตลอดจนผู้ปฏิบัติงานหลายคนสามารถลงทะเบียนได้ในสวัสดิการ "
author: kherr75
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 844582904f7d3c14f6d5aa425a3c9d8234c01568
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="d67db-103">ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="d67db-103">Enroll and remove benefits from workers</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d67db-104">ขั้นตอนนี้สาธิตว่าผู้ปฏิบัติงานสามารถลงทะเบียนในสวัสดิการอันเดียวหรือมากกว่านั้นได้อย่างไร ตลอดจนผู้ปฏิบัติงานหลายคนสามารถลงทะเบียนได้ในสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="d67db-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="d67db-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="d67db-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="d67db-106">การลงทะเบียนผู้ปฏิบัติงานคนเดียวในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d67db-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="d67db-107">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="d67db-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="d67db-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d67db-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d67db-109">คลิก สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d67db-109">Click Benefits.</span></span>
4. <span data-ttu-id="d67db-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d67db-110">Click New.</span></span>
5. <span data-ttu-id="d67db-111">ในฟิลด์สวัสดิการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d67db-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="d67db-112">ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d67db-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="d67db-113">ในฟิลด์วันที่สิ้นสุดความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d67db-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="d67db-114">ขยายส่วนผู้รับผลประโยชน์ ถ้าหากผู้รับผลประโยชน์จำเป็นต้องเพิ่มเข้าไปในสวัสดีการ </span><span class="sxs-lookup"><span data-stu-id="d67db-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="d67db-115">คุณสามารถเพิ่มผู้อยู่ในอุปการะจากหน้านี้ถ้าเกี่ยวข้องกับตัวสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d67db-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="d67db-116">นอกจากนี้คุณยังสามารถแก้ไขรายละเอียดของการลงทะเบียนสวัสดิการ หรือลบการลงทะเบียนบนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="d67db-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="d67db-117">เมื่อคุณเสร็จสิ้นการทำการเปลี่ยนแปลงกับการลงทะเบียนสวัสดิการ ปิดหน้านี้</span><span class="sxs-lookup"><span data-stu-id="d67db-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="d67db-118">การลงทะเบียนผู้ปฏิบัติงานหลายรายในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d67db-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="d67db-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d67db-119">Close the page.</span></span>
2. <span data-ttu-id="d67db-120">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="d67db-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="d67db-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d67db-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d67db-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d67db-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d67db-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d67db-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d67db-124">คลิก ลงทะเบียนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d67db-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="d67db-125">ในฟิลด์สวัสดิการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d67db-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="d67db-126">ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d67db-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="d67db-127">ในฟิลด์วันที่สิ้นสุดความคุ้มครอง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d67db-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="d67db-128">คลิกลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="d67db-128">Click Enroll.</span></span>
11. <span data-ttu-id="d67db-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d67db-129">Close the page.</span></span>
12. <span data-ttu-id="d67db-130">ไปที่ฝ่ายบุคคล > สวัสดิการ > การลงทะเบียน > ผลการลงทะเบียนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d67db-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="d67db-131">ค้นหาบันทึกผลสวัสดิการที่กำลังมองหาอยู่</span><span class="sxs-lookup"><span data-stu-id="d67db-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="d67db-132">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d67db-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d67db-133">หน้านี้จะช่วยให้คุณดูพนักงานที่ได้ลงทะเบียนในสวัสดิการและพนักงานที่ยังไม่ได้ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="d67db-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>


