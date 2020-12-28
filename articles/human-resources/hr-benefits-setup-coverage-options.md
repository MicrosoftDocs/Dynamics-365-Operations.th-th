---
title: สร้างตัวเลือกความคุ้มครอง
description: ตัวเลือกความครอบคลุมใน Microsoft Dynamics 365 Human Resources คือระดับความครอบคลุมสำหรับการเลือกตั้งของผู้เข้าร่วมในแผนสวัสดิการหรือโปรแกรม
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8690dbe00c2316ccf745f5222c3cbaa9c3379f85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420810"
---
# <a name="create-coverage-options"></a><span data-ttu-id="3f548-103">สร้างตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="3f548-103">Create coverage options</span></span>

<span data-ttu-id="3f548-104">ตัวเลือกความครอบคลุมใน Microsoft Dynamics 365 Human Resources คือระดับความครอบคลุมสำหรับการเลือกตั้งของผู้เข้าร่วมในแผนสวัสดิการหรือโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="3f548-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="3f548-105">ตัวอย่างเช่น ความครอบคลุมอาจรวมถึง **เฉพาะพนักงาน** สำหรับแผนการรักษาพยาบาลหรือ **2 เท่าของเงินเดือน** สำหรับแผนประกันชีวิต</span><span class="sxs-lookup"><span data-stu-id="3f548-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="3f548-106">เมื่อกำหนดแล้ว คุณสามารถนำตัวเลือกความครอบคลุมสวัสดิการมาใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="3f548-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="3f548-107">คุณสามารถเชื่อมโยงตัวเลือกกับแผนหนึ่งแผนขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="3f548-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="3f548-108">หลังจากมีการกำหนดตัวเลือกความครอบคลุมแล้ว ให้แนบตัวเลือกความครอบคลุมเข้ากับชนิดของแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3f548-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="3f548-109">ชนิดของแผนจะถูกเชื่อมโยงกับแผนสิทธิประโยชน์หรือโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="3f548-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="3f548-110">ตัวเลือกความครอบคลุมที่เชื่อมโยงกับชนิดของแผนจะพร้อมใช้งานกับแผนทั้งหมดที่สร้างขึ้นโดยชนิดของแผนนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="3f548-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="3f548-111">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ตัวเลือกความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="3f548-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="3f548-112">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3f548-112">Select **New**.</span></span>

3. <span data-ttu-id="3f548-113">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3f548-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3f548-114">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="3f548-114">Field</span></span> | <span data-ttu-id="3f548-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3f548-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3f548-116">**ตัวเลือกความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="3f548-116">**Coverage option**</span></span> | <span data-ttu-id="3f548-117">ชื่อเฉพาะของตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="3f548-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="3f548-118">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="3f548-118">**Description**</span></span> | <span data-ttu-id="3f548-119">คำอธิบายเกี่ยวกับตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="3f548-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="3f548-120">**รหัสความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="3f548-120">**Coverage code**</span></span> | <span data-ttu-id="3f548-121">รหัสความคุ้มครองจะกำหนดยอดเงินต่ำสุดและสูงสุดสำหรับแต่ละสิทธิ์ที่คุ้มครองชนิดของบุคคล</span><span class="sxs-lookup"><span data-stu-id="3f548-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="3f548-122">รหัสความคุ้มครองจะระบุผู้ที่ได้รับการคุ้มครองหรือยอดเงินของความคุ้มครองที่ใช้ได้กับชนิดของแผน</span><span class="sxs-lookup"><span data-stu-id="3f548-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="3f548-123">คุณสามารถแสดงยอดเงินของความคุ้มครองเป็นเงินดอลลาร์หรือเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="3f548-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="3f548-124">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="3f548-124">For example:</span></span></br></br><span data-ttu-id="3f548-125">- **Emp + 1** – เพื่อให้เป็นไปตามเงื่อนไข พนักงานจะต้องเลือกผู้อยู่ในอุปการะหนึ่งราย (ถ้ามีการเลือกมากกว่าหนึ่งราย จะไม่สามารถดำเนินการได้อีกต่อไป)</span><span class="sxs-lookup"><span data-stu-id="3f548-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="3f548-126">- **Emp + ครอบครัว** – เพื่อความเหมาะสม พนักงานจะต้องเลือกผู้อยู่ในอุปการะอย่างน้อยสองราย</span><span class="sxs-lookup"><span data-stu-id="3f548-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="3f548-127">**จำนวนสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="3f548-127">**Maximum number**</span></span> | <span data-ttu-id="3f548-128">จำนวนของผู้อยู่ในอุปการะสูงสุด</span><span class="sxs-lookup"><span data-stu-id="3f548-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="3f548-129">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="3f548-129">**Status**</span></span> | <span data-ttu-id="3f548-130">สถานะของตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="3f548-130">The status of the coverage option.</span></span> <span data-ttu-id="3f548-131">ถ้าสถานะของตัวเลือกความคุ้มครองถูกตั้งค่าเป็นไม่ใช้งาน คุณจะไม่สามารถเลือกตัวเลือกความคุ้มครองบนชนิดของแผน</span><span class="sxs-lookup"><span data-stu-id="3f548-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="3f548-132">**เปอร์เซ็นต์**</span><span class="sxs-lookup"><span data-stu-id="3f548-132">**Percent**</span></span> | <span data-ttu-id="3f548-133">ยอดเงินเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="3f548-133">The percent amount.</span></span> <span data-ttu-id="3f548-134">ฟิลด์นี้จะใช้งานได้ก็ต่อเมื่อ % x เงินเดือนถูกเลือกในฟิลด์รหัสความคุ้มครองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3f548-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="3f548-135">**ตัวหาร**</span><span class="sxs-lookup"><span data-stu-id="3f548-135">**Divisor**</span></span> | <span data-ttu-id="3f548-136">ตัวหารที่จะใช้ในการคำนวณเมื่อคุณเลือกรหัสความคุ้มครอง % x เงินเดือน</span><span class="sxs-lookup"><span data-stu-id="3f548-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="3f548-137">**เปอร์เซ็นต์ต่ำสุด**</span><span class="sxs-lookup"><span data-stu-id="3f548-137">**Percent minimum**</span></span> | <span data-ttu-id="3f548-138">เปอร์เซ็นต์ต่ำสุดเมื่อคุณเลือกรหัสเปอร์เซ็นต์ความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="3f548-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="3f548-139">**เปอร์เซ็นต์สูงสุด**</span><span class="sxs-lookup"><span data-stu-id="3f548-139">**Percent maximum**</span></span> | <span data-ttu-id="3f548-140">เปอร์เซ็นต์สูงสุดเมื่อคุณเลือกรหัสเปอร์เซ็นต์ความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="3f548-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="3f548-141">ภายใต้ **ตัวเลือกสิทธิ์ของความสัมพันธ์ส่วนบุคคล** ให้แนบตัวเลือกสิทธิ์ของผู้ที่มีความสัมพันธ์ส่วนบุคคลที่เหมาะสมกับตัวเลือกความคุ้มครองแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="3f548-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="3f548-142">ภายใต้ **การบริการตนเอง** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3f548-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="3f548-143">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="3f548-143">Field</span></span> | <span data-ttu-id="3f548-144">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3f548-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3f548-145">**อนุญาตจำนวนเงินจ่ายสมทบของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="3f548-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="3f548-146">ระบุว่าจะอนุญาตให้พนักงานปรับเปลี่ยนยอดเงินสมทบของสิทธิประโยชน์ด้วยตนเองเมื่อพวกเขาเลือกสิทธิประโยชน์ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3f548-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="3f548-147">ถ้าคุณเลือกกล่องกาเครื่องหมายนี้ ระบบจะคำนวณพารามิเตอร์ของแผนสิทธิประโยชน์ตามยอดเงินสมทบที่พนักงานป้อนไว้ในการบริการสิทธิประโยชน์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="3f548-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="3f548-148">**อนุญาตจำนวนเงินของความคุ้มครองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="3f548-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="3f548-149">ระบุว่าจะอนุญาตให้พนักงานปรับเปลี่ยนยอดเงินที่คุ้มครองของสิทธิประโยชน์ด้วยตนเองเมื่อพวกเขาเลือกสิทธิประโยชน์ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3f548-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="3f548-150">ถ้าคุณเลือกกล่องกาเครื่องหมายนี้ ระบบจะคำนวณพารามิเตอร์ของแผนสิทธิประโยชน์ตามยอดความคุ้มครองที่พนักงานป้อนไว้ในการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="3f548-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="3f548-151">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3f548-151">Select **Save**.</span></span> 
