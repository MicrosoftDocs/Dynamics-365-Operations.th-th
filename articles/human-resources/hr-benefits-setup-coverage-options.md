---
title: สร้างตัวเลือกความคุ้มครอง
description: ตัวเลือกความคุ้มครองใน Microsoft Dynamics 365 Human Resources เป็นระดับความคุ้มครองสำหรับการเลือกผู้มีส่วนร่วมในแผนสิทธิประโยชน์หรือโปรแกรม เช่น แผนการรักษาพยาบาลสำหรับพนักงานเท่านั้น หรือ 2 เท่าเงินของเดือนสำหรับแผนประกันชีวิต
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092717"
---
# <a name="create-coverage-options"></a><span data-ttu-id="8a541-103">สร้างตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="8a541-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="8a541-104">ตัวเลือกความคุ้มครองใน Microsoft Dynamics 365 Human Resources เป็นระดับความคุ้มครองสำหรับการเลือกผู้มีส่วนร่วมในแผนสิทธิประโยชน์หรือโปรแกรม เช่น แผนการรักษาพยาบาลสำหรับพนักงานเท่านั้น หรือ 2 เท่าเงินของเดือนสำหรับแผนประกันชีวิต</span><span class="sxs-lookup"><span data-stu-id="8a541-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="8a541-105">เมื่อกำหนดได้แล้ว ผลประโยชน์ของตัวเลือกความคุ้มครองจะใช้งานได้อีกครั้งและคุณสามารถเชื่อมโยงตัวเลือกกับหนึ่งแผนหรือมากกว่าได้</span><span class="sxs-lookup"><span data-stu-id="8a541-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="8a541-106">เมื่อมีการกำหนดตัวเลือกความคุ้มครองแล้ว ให้แนบตัวเลือกความคุ้มครองเข้ากับชนิดของแผนสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="8a541-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="8a541-107">ชนิดของแผนจะถูกเชื่อมโยงกับแผนสิทธิประโยชน์หรือโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="8a541-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="8a541-108">ตัวเลือกความคุ้มครองที่เชื่อมโยงกับชนิดของแผนจะพร้อมใช้งานกับแผนทั้งหมดที่สร้างขึ้นโดยชนิดของแผนนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="8a541-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="8a541-109">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ตัวเลือกความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="8a541-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="8a541-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8a541-110">Select **New**.</span></span>

3. <span data-ttu-id="8a541-111">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8a541-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="8a541-112">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="8a541-112">Field</span></span> | <span data-ttu-id="8a541-113">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8a541-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8a541-114">**ตัวเลือกความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="8a541-114">**Coverage option**</span></span> | <span data-ttu-id="8a541-115">ชื่อเฉพาะของตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="8a541-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="8a541-116">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="8a541-116">**Description**</span></span> | <span data-ttu-id="8a541-117">คำอธิบายเกี่ยวกับตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="8a541-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="8a541-118">**รหัสความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="8a541-118">**Coverage code**</span></span> | <span data-ttu-id="8a541-119">รหัสความคุ้มครองจะกำหนดยอดเงินต่ำสุดและสูงสุดสำหรับแต่ละสิทธิ์ที่คุ้มครองชนิดของบุคคล</span><span class="sxs-lookup"><span data-stu-id="8a541-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="8a541-120">รหัสความคุ้มครองจะระบุผู้ที่ได้รับการคุ้มครองหรือยอดเงินของความคุ้มครองที่ใช้ได้กับชนิดของแผน</span><span class="sxs-lookup"><span data-stu-id="8a541-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="8a541-121">คุณสามารถแสดงยอดเงินของความคุ้มครองเป็นเงินดอลลาร์หรือเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="8a541-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="8a541-122">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="8a541-122">For example:</span></span></br></br><span data-ttu-id="8a541-123">- **Emp + 1** – เพื่อให้เป็นไปตามเงื่อนไข พนักงานจะต้องเลือกผู้อยู่ในอุปการะหนึ่งราย (ถ้ามีการเลือกมากกว่าหนึ่งราย จะไม่สามารถดำเนินการได้อีกต่อไป)</span><span class="sxs-lookup"><span data-stu-id="8a541-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="8a541-124">- **Emp + ครอบครัว** – เพื่อความเหมาะสม พนักงานจะต้องเลือกผู้อยู่ในอุปการะอย่างน้อยสองราย</span><span class="sxs-lookup"><span data-stu-id="8a541-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="8a541-125">**จำนวนสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="8a541-125">**Maximum number**</span></span> | <span data-ttu-id="8a541-126">จำนวนของผู้อยู่ในอุปการะสูงสุด</span><span class="sxs-lookup"><span data-stu-id="8a541-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="8a541-127">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="8a541-127">**Status**</span></span> | <span data-ttu-id="8a541-128">สถานะของตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="8a541-128">The status of the coverage option.</span></span> <span data-ttu-id="8a541-129">ถ้าสถานะของตัวเลือกความคุ้มครองถูกตั้งค่าเป็นไม่ใช้งาน คุณจะไม่สามารถเลือกตัวเลือกความคุ้มครองบนชนิดของแผน</span><span class="sxs-lookup"><span data-stu-id="8a541-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="8a541-130">**เปอร์เซ็นต์**</span><span class="sxs-lookup"><span data-stu-id="8a541-130">**Percent**</span></span> | <span data-ttu-id="8a541-131">ยอดเงินเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="8a541-131">The percent amount.</span></span> <span data-ttu-id="8a541-132">ฟิลด์นี้จะใช้งานได้ก็ต่อเมื่อ % x เงินเดือนถูกเลือกในฟิลด์รหัสความคุ้มครองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8a541-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="8a541-133">**ตัวหาร**</span><span class="sxs-lookup"><span data-stu-id="8a541-133">**Divisor**</span></span> | <span data-ttu-id="8a541-134">ตัวหารที่จะใช้ในการคำนวณเมื่อคุณเลือกรหัสความคุ้มครอง % x เงินเดือน</span><span class="sxs-lookup"><span data-stu-id="8a541-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="8a541-135">**เปอร์เซ็นต์ต่ำสุด**</span><span class="sxs-lookup"><span data-stu-id="8a541-135">**Percent minimum**</span></span> | <span data-ttu-id="8a541-136">เปอร์เซ็นต์ต่ำสุดเมื่อคุณเลือกรหัสเปอร์เซ็นต์ความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="8a541-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="8a541-137">**เปอร์เซ็นต์สูงสุด**</span><span class="sxs-lookup"><span data-stu-id="8a541-137">**Percent maximum**</span></span> | <span data-ttu-id="8a541-138">เปอร์เซ็นต์สูงสุดเมื่อคุณเลือกรหัสเปอร์เซ็นต์ความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="8a541-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="8a541-139">ภายใต้ **ตัวเลือกสิทธิ์ของความสัมพันธ์ส่วนบุคคล** ให้แนบตัวเลือกสิทธิ์ของผู้ที่มีความสัมพันธ์ส่วนบุคคลที่เหมาะสมกับตัวเลือกความคุ้มครองแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8a541-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="8a541-140">ภายใต้ **การบริการตนเอง** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8a541-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="8a541-141">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="8a541-141">Field</span></span> | <span data-ttu-id="8a541-142">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8a541-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8a541-143">**อนุญาตจำนวนเงินจ่ายสมทบของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="8a541-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="8a541-144">ระบุว่าจะอนุญาตให้พนักงานปรับเปลี่ยนยอดเงินสมทบของสิทธิประโยชน์ด้วยตนเองเมื่อพวกเขาเลือกสิทธิประโยชน์ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8a541-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="8a541-145">ถ้าคุณเลือกกล่องกาเครื่องหมายนี้ ระบบจะคำนวณพารามิเตอร์ของแผนสิทธิประโยชน์ตามยอดเงินสมทบที่พนักงานป้อนไว้ในการบริการสิทธิประโยชน์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="8a541-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="8a541-146">**อนุญาตจำนวนเงินของความคุ้มครองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="8a541-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="8a541-147">ระบุว่าจะอนุญาตให้พนักงานปรับเปลี่ยนยอดเงินที่คุ้มครองของสิทธิประโยชน์ด้วยตนเองเมื่อพวกเขาเลือกสิทธิประโยชน์ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8a541-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="8a541-148">ถ้าคุณเลือกกล่องกาเครื่องหมายนี้ ระบบจะคำนวณพารามิเตอร์ของแผนสิทธิประโยชน์ตามยอดความคุ้มครองที่พนักงานป้อนไว้ในการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="8a541-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="8a541-149">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8a541-149">Select **Save**.</span></span> 
