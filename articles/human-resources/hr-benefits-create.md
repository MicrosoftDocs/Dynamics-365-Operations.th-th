---
title: สร้างสวัสดิการใหม่
description: 'งานนี้จะแสดงวิธีการสร้างองค์ประกอบของสวัสดิการที่จะใช้เมื่อสร้างสวัสดิการใหม่ '
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: f9618e62e33655bfc1a0653cb767abe0094d1e79
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420721"
---
# <a name="create-a-new-benefit"></a><span data-ttu-id="e0da8-103">สร้างสวัสดิการใหม่</span><span class="sxs-lookup"><span data-stu-id="e0da8-103">Create a new benefit</span></span>

<span data-ttu-id="e0da8-104">งานนี้จะแสดงวิธีการสร้างองค์ประกอบของสวัสดิการที่จะใช้เมื่อสร้างสวัสดิการใหม่ </span><span class="sxs-lookup"><span data-stu-id="e0da8-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="e0da8-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e0da8-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="e0da8-106">งานนี้มีไว้สำหรับผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e0da8-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="e0da8-107">สร้างองค์ประกอบของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e0da8-107">Create benefit elements</span></span>
1. <span data-ttu-id="e0da8-108">ไปที่ ทรัพยากรบุคคล > การตั้งค่า > การตั้งค่า > องค์ประกอบของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e0da8-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="e0da8-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e0da8-109">Click New.</span></span>
3. <span data-ttu-id="e0da8-110">ในฟิลด์ชนิด ให้ป้อนชื่อของประเภทของสวัสดิการที่คุณกำลังสร้าง</span><span class="sxs-lookup"><span data-stu-id="e0da8-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="e0da8-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e0da8-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e0da8-112">ในฟิลด์การลงทะเบียนที่เกิดขึ้นพร้อมกัน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e0da8-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="e0da8-113">เพื่อจำกัดความสามารถของพนักงานในการลงทะเบียนในหลายแผนการรักษาพยาบาล ให้เลือกลงทะเบียนหนึ่งรายการต่อชนิด</span><span class="sxs-lookup"><span data-stu-id="e0da8-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="e0da8-114">ในฟิลด์ประเภทค่าจ้าง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e0da8-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="e0da8-115">คลิกที่แท็บแผน</span><span class="sxs-lookup"><span data-stu-id="e0da8-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="e0da8-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e0da8-116">Click New.</span></span>
9. <span data-ttu-id="e0da8-117">ในฟิลด์แผน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e0da8-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="e0da8-118">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e0da8-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="e0da8-119">ในฟิลด์ชนิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e0da8-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="e0da8-120">ในฟิลด์ผลกระทบของค่าจ้าง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e0da8-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="e0da8-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e0da8-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="e0da8-122">สร้างสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e0da8-122">Create a benefit</span></span>
1. <span data-ttu-id="e0da8-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e0da8-123">Close the page.</span></span>
2. <span data-ttu-id="e0da8-124">ไปที่ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e0da8-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="e0da8-125">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="e0da8-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="e0da8-126">ในฟิลด์แผนงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e0da8-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="e0da8-127">ในฟิลด์ตัวเลือก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e0da8-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="e0da8-128">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="e0da8-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="e0da8-129">คลิกที่สร้างสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e0da8-129">Click Create benefit.</span></span>

