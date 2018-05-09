--- 
title: "สร้างสวัสดิการใหม่"
description: "งานนี้จะแสดงวิธีการสร้างองค์ประกอบของสวัสดิการที่จะใช้เมื่อสร้างสวัสดิการใหม่ "
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f1bc9617570bcaec2d4948a76e7a23bc5f5b1f84
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-new-benefit"></a><span data-ttu-id="5231c-103">สร้างสวัสดิการใหม่</span><span class="sxs-lookup"><span data-stu-id="5231c-103">Create a new benefit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5231c-104">งานนี้จะแสดงวิธีการสร้างองค์ประกอบของสวัสดิการที่จะใช้เมื่อสร้างสวัสดิการใหม่ </span><span class="sxs-lookup"><span data-stu-id="5231c-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="5231c-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="5231c-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="5231c-106">งานนี้มีไว้สำหรับผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5231c-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="5231c-107">สร้างองค์ประกอบของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5231c-107">Create benefit elements</span></span>
1. <span data-ttu-id="5231c-108">ไปที่ ทรัพยากรบุคคล > การตั้งค่า > การตั้งค่า > องค์ประกอบของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5231c-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="5231c-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5231c-109">Click New.</span></span>
3. <span data-ttu-id="5231c-110">ในฟิลด์ชนิด ให้ป้อนชื่อของประเภทของสวัสดิการที่คุณกำลังสร้าง</span><span class="sxs-lookup"><span data-stu-id="5231c-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="5231c-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5231c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5231c-112">ในฟิลด์การลงทะเบียนที่เกิดขึ้นพร้อมกัน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="5231c-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="5231c-113">เพื่อจำกัดความสามารถของพนักงานในการลงทะเบียนในหลายแผนการรักษาพยาบาล ให้เลือกลงทะเบียนหนึ่งรายการต่อชนิด</span><span class="sxs-lookup"><span data-stu-id="5231c-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="5231c-114">ในฟิลด์ประเภทค่าจ้าง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="5231c-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="5231c-115">คลิกที่แท็บแผน</span><span class="sxs-lookup"><span data-stu-id="5231c-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="5231c-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5231c-116">Click New.</span></span>
9. <span data-ttu-id="5231c-117">ในฟิลด์แผน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5231c-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="5231c-118">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5231c-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="5231c-119">ในฟิลด์ชนิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5231c-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="5231c-120">ในฟิลด์ผลกระทบของค่าจ้าง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="5231c-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="5231c-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5231c-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="5231c-122">สร้างสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5231c-122">Create a benefit</span></span>
1. <span data-ttu-id="5231c-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5231c-123">Close the page.</span></span>
2. <span data-ttu-id="5231c-124">ไปที่ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5231c-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="5231c-125">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5231c-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="5231c-126">ในฟิลด์แผนงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5231c-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="5231c-127">ในฟิลด์ตัวเลือก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5231c-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="5231c-128">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="5231c-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="5231c-129">คลิกที่สร้างสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5231c-129">Click Create benefit.</span></span>


