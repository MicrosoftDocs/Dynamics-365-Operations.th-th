---
title: ตั้งค่าข้อมูลการบาดเจ็บและการเจ็บป่วย
description: 'นายจ้างจำเป็นต้องทราบเมื่อพนักงานได้รับบาดเจ็บหรือมีการเจ็บป่วยที่เป็นผลมาจากอันตรายในสถานที่ทำงาน '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjurySetup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8e5276958cd0d95918f57c82c2a242a3f745f6c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467420"
---
# <a name="set-up-injury-and-illness-information"></a><span data-ttu-id="4ddd6-103">ตั้งค่าข้อมูลการบาดเจ็บและการเจ็บป่วย</span><span class="sxs-lookup"><span data-stu-id="4ddd6-103">Set up injury and illness information</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="4ddd6-104">นายจ้างจำเป็นต้องทราบเมื่อพนักงานได้รับบาดเจ็บหรือมีการเจ็บป่วยที่เป็นผลมาจากอันตรายในสถานที่ทำงาน </span><span class="sxs-lookup"><span data-stu-id="4ddd6-104">Employers need to know when their employees suffer injuries or illness resulting from hazards in the workplace.</span></span> <span data-ttu-id="4ddd6-105">คุณสามารถใช้หน้าการบาดเจ็บและการเจ็บป่วย เพื่อตั้งค่าข้อมูลที่ช่วยในการรายงานการบาดเจ็บหรือการเจ็บป่วยในสถานที่ทำงาน </span><span class="sxs-lookup"><span data-stu-id="4ddd6-105">You can use the injury and illness page to set up information that facilitates reporting work-place injuries or illnesses.</span></span> <span data-ttu-id="4ddd6-106">คุณสามารถตั้งค่าชนิดของการบาดเจ็บและการเจ็บป่วย รวมถึงชนิดการรักษาพยาบาล ต้นทุน และผลที่ได้ </span><span class="sxs-lookup"><span data-stu-id="4ddd6-106">You can set up types of injuries and illnesses, including types of treatments, costs, and outcomes.</span></span> <span data-ttu-id="4ddd6-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="4ddd6-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4ddd6-108">ไปที่ ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > การบาดเจ็บและการเจ็บป่วย > การตั้งค่าการบาดเจ็บและการเจ็บป่วย</span><span class="sxs-lookup"><span data-stu-id="4ddd6-108">Go to Human resources > Workers > Injury and illness > Injury and illness setup.</span></span>
2. <span data-ttu-id="4ddd6-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ddd6-109">Click New.</span></span>
3. <span data-ttu-id="4ddd6-110">ในฟิลด์ชนิดการบาดเจ็บและการเจ็บป่วย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-110">In the Injury or illness type field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-111">ตัวอย่าง: การแตกร้าว</span><span class="sxs-lookup"><span data-stu-id="4ddd6-111">Example: Fracture</span></span>  
4. <span data-ttu-id="4ddd6-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-113">ตัวอย่าง: กระดูกร้าว</span><span class="sxs-lookup"><span data-stu-id="4ddd6-113">Example: Bone fracture</span></span>  
5. <span data-ttu-id="4ddd6-114">คลิกแท็บอวัยวะ</span><span class="sxs-lookup"><span data-stu-id="4ddd6-114">Click the Body parts tab.</span></span>
6. <span data-ttu-id="4ddd6-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ddd6-115">Click New.</span></span>
7. <span data-ttu-id="4ddd6-116">ในฟิลด์อวัยวะ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-116">In the Body part field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-117">ตัวอย่าง: ข้อมือ</span><span class="sxs-lookup"><span data-stu-id="4ddd6-117">Example: Wrist</span></span>  
8. <span data-ttu-id="4ddd6-118">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-118">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-119">ตัวอย่าง: ข้อมือ</span><span class="sxs-lookup"><span data-stu-id="4ddd6-119">Example: Wrist</span></span>  
9. <span data-ttu-id="4ddd6-120">คลิกแท็บชนิดการรักษา</span><span class="sxs-lookup"><span data-stu-id="4ddd6-120">Click the Treatment types tab.</span></span>
10. <span data-ttu-id="4ddd6-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ddd6-121">Click New.</span></span>
11. <span data-ttu-id="4ddd6-122">ในฟิลด์ชนิดการรักษา ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-122">In the Treatment type field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-123">ตัวอย่าง: เข้าเฝือก</span><span class="sxs-lookup"><span data-stu-id="4ddd6-123">Example: Splint</span></span>  
12. <span data-ttu-id="4ddd6-124">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-124">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-125">ตัวอย่าง: ใส่เฝือก</span><span class="sxs-lookup"><span data-stu-id="4ddd6-125">Example: Put a splint on</span></span>  
13. <span data-ttu-id="4ddd6-126">คลิกแท็บชนิดของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4ddd6-126">Click the Cost types tab.</span></span>
14. <span data-ttu-id="4ddd6-127">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ddd6-127">Click New.</span></span>
15. <span data-ttu-id="4ddd6-128">ในฟิลด์ชนิดต้นทุน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-128">In the Cost type field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-129">ตัวอย่าง: X-rays</span><span class="sxs-lookup"><span data-stu-id="4ddd6-129">Example: X-rays</span></span>  
16. <span data-ttu-id="4ddd6-130">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-130">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-131">ตัวอย่าง: X-rays</span><span class="sxs-lookup"><span data-stu-id="4ddd6-131">Example: X-rays</span></span>  
17. <span data-ttu-id="4ddd6-132">คลิกแท็บชนิดของผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4ddd6-132">Click the Outcome types tab.</span></span>
18. <span data-ttu-id="4ddd6-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ddd6-133">Click New.</span></span>
19. <span data-ttu-id="4ddd6-134">ในฟิลด์ชนิดผลลัพธ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-134">In the Outcome type field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-135">ตัวอย่าง: การบำบัด</span><span class="sxs-lookup"><span data-stu-id="4ddd6-135">Example: Therapy</span></span>  
20. <span data-ttu-id="4ddd6-136">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4ddd6-136">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4ddd6-137">ตัวอย่าง: กายภาพบำบัด</span><span class="sxs-lookup"><span data-stu-id="4ddd6-137">Example: Physical therapy</span></span>  
21. <span data-ttu-id="4ddd6-138">คลิกแท็บระดับความรุนแรง</span><span class="sxs-lookup"><span data-stu-id="4ddd6-138">Click the Severity levels tab.</span></span>
    * <span data-ttu-id="4ddd6-139">สามารถสร้างระดับความรุนแรงที่กำหนดเองได้ </span><span class="sxs-lookup"><span data-stu-id="4ddd6-139">Customizable severity levels can be created.</span></span> <span data-ttu-id="4ddd6-140">ตัวอย่างเช่น: ความรุนแรง 1 อาจหมายถึง การบาดเจ็บเล็กน้อย ขณะที่ความรุนแรง 3 อาจบ่งชี้ถึงการบาดเจ็บร้ายแรง</span><span class="sxs-lookup"><span data-stu-id="4ddd6-140">For example: Severity 1 might mean a minor injury, where severity 3 might indicate a severe injury.</span></span>  
22. <span data-ttu-id="4ddd6-141">คลิกแท็บหน่วยงานรายงาน</span><span class="sxs-lookup"><span data-stu-id="4ddd6-141">Click the Reporting agencies tab.</span></span>
    * <span data-ttu-id="4ddd6-142">หน่วยงานรายงานคือหน่วยงานที่ต้องได้รับการรายงานเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="4ddd6-142">Reporting agencies are the agencies that the incident needs to be reported to.</span></span> <span data-ttu-id="4ddd6-143">เลือกกล่องกาเครื่องหมายค่าเริ่มต้นสำหรับหน่วยงานที่เป็นหน่วยงานค่าเริ่มต้นสำหรับการรายงานการบาดเจ็บและการเจ็บป่วย</span><span class="sxs-lookup"><span data-stu-id="4ddd6-143">Select the default check box for the agency that is the default agency for reporting injury and illnesses to.</span></span>  
23. <span data-ttu-id="4ddd6-144">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4ddd6-144">Click Save.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]