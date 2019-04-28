---
title: การวิเคราะห์ผลลัพธ์ของแบบสอบถาม
description: 'สถิติแบบสอบถามสามารถใช้ในการคำนวณค่าเฉลี่ย ยอดรวม และเปอร์เซ็นต์ ที่ขึ้นอยู่กับชุดของข้อมูลทางประชากรศาสตร์ '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d8f9c2fcf0be117f8fcde5113c0d42f11786679
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "858594"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="525d8-103">การวิเคราะห์ผลลัพธ์ของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="525d8-103">Analyzing questionnaire results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="525d8-104">สถิติแบบสอบถามสามารถใช้ในการคำนวณค่าเฉลี่ย ยอดรวม และเปอร์เซ็นต์ ที่ขึ้นอยู่กับชุดของข้อมูลทางประชากรศาสตร์ </span><span class="sxs-lookup"><span data-stu-id="525d8-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="525d8-105">เริ่มต้นขั้นตอนนี้โดยไปที่แบบสอบถาม > ดูและวิเคราะห์ผลลัพธ์ > สถิติแบบสอบถาม </span><span class="sxs-lookup"><span data-stu-id="525d8-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="525d8-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="525d8-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="525d8-107">สร้าเรกคอร์ดสถิติแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="525d8-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="525d8-108">ไปที่สถิติแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="525d8-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="525d8-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="525d8-109">Click New.</span></span>
3. <span data-ttu-id="525d8-110">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="525d8-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="525d8-111">ในฟิลด์สถิติ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="525d8-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="525d8-112">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="525d8-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="525d8-113">ในฟิลด์แบบสอบถาม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="525d8-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="525d8-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="525d8-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="525d8-115">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="525d8-115">Click the General tab.</span></span>
    * <span data-ttu-id="525d8-116">กดเลือกถ้าคุณต้องการรวมผลลัพธ์ที่ไม่ระบุชื่อหรือผลลัพธ์จากผู้ปฏิบัติงาน ผู้ติดต่อ และผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="525d8-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="525d8-117">เลือกหรือยกเลิกกล่องผู้ปฏิบัติงานกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="525d8-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="525d8-118">ถ้าคุณใช้ในการดูผลลัพธ์โดยเรียงตามอายุงานหรือตามอายุ ให้ระบุช่วงที่คุณต้องการใช้สำหรับการจัดกลุ่มผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="525d8-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="525d8-119">เมื่อป้อน 5 สำหรับช่วงอายุจะเป็นการจัดกลุ่มผลลัพธ์ตามช่วงอายุห้าปี</span><span class="sxs-lookup"><span data-stu-id="525d8-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="525d8-120">ในฟิลด์อายุ ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="525d8-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="525d8-121">กดเลือกถ้าคุณต้องการรันการคำนวณสำหรับทั้งแบบสอบถาม สำหรับกลุ่มผลคะแนนแต่ละกลุ่ม สำหรับแต่ละคำถาม หรือ สำหรับแต่ละแถวคำถาม</span><span class="sxs-lookup"><span data-stu-id="525d8-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="525d8-122">เลือกวิธีการที่คุณต้องการจัดกลุ่มผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="525d8-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="525d8-123">ตัวอย่างเช่น ถ้าคุณคำนวณคะแนนเฉลี่ยสำหรับแต่ละคำถาม คุณอาจต้องการดูคำถามที่ถูกจัดกลุ่มตามกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="525d8-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="525d8-124">เลือกข้อมูลที่ใช้เป็นพื้นฐานสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="525d8-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="525d8-125">ตัวอย่างเช่น ถ้าคุณต้องการดูเปอร์เซ็นต์เฉลี่ยที่ได้รับในแบบสอบถามระหว่างพนักงานของคุณเทียบกับจำนวนเฉลี่ยของคะแนนที่ได้รับระหว่างพนักงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="525d8-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="525d8-126">คลิก แท็บการกำหนดช่วง</span><span class="sxs-lookup"><span data-stu-id="525d8-126">Click the Range tab.</span></span>
    * <span data-ttu-id="525d8-127">ใช้ช่วงเพื่อจำกัดชุดผลลัพธ์เพื่อให้ตรงกับเกณฑ์เงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="525d8-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="525d8-128">คลิก การจัดกลุ่มโดยแท็บ</span><span class="sxs-lookup"><span data-stu-id="525d8-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="525d8-129">ใช้การจัดกลุ่มเพื่อกำหนดว่าควรแสดงผลลัพธ์อย่างไร</span><span class="sxs-lookup"><span data-stu-id="525d8-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="525d8-130">ตัวอย่างเช่น จัดกลุ่มผลลัพธ์แรกตามเพศ แล้วตามจึงด้วยอายุ</span><span class="sxs-lookup"><span data-stu-id="525d8-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="525d8-131">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="525d8-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="525d8-132">คุณสามารถย้ายการจัดกลุ่มไปด้านที่เลือก และวางไว้ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="525d8-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="525d8-133">ดำเนินการคำนวณสถิติ</span><span class="sxs-lookup"><span data-stu-id="525d8-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="525d8-134">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="525d8-134">Click Execute.</span></span>
    * <span data-ttu-id="525d8-135">เลือกฟังก์ชันการคำนวณที่คุณต้องการดำเนินการในผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="525d8-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="525d8-136">ตัวอย่างเช่น คำนวณเปอร์เซ็นต์เฉลี่ยผ่านแบบสอบถามสำหรับการจัดกลุ่มที่เลือก หรือคะแนนรวมระหว่างกลุ่มผลคะแนนสำหรับการจัดกลุ่มที่เลือก</span><span class="sxs-lookup"><span data-stu-id="525d8-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="525d8-137">เลือกหรือล้าง กล่องกาเครื่องหมายการลบการค้นหาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="525d8-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="525d8-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="525d8-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="525d8-139">ดูผลลัพธ์ของการรันสถิติแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="525d8-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="525d8-140">คลิกผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="525d8-140">Click Result.</span></span>
2. <span data-ttu-id="525d8-141">คลิกผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="525d8-141">Click Result.</span></span>
3. <span data-ttu-id="525d8-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="525d8-142">Close the page.</span></span>

