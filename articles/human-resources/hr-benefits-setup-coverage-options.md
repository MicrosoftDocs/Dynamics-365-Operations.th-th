---
title: สร้างตัวเลือกความคุ้มครอง
description: ''
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010676"
---
# <a name="create-coverage-options"></a><span data-ttu-id="5c472-102">สร้างตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5c472-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5c472-103">ตัวเลือกความคุ้มครองใน Microsoft Dynamics 365 Human Resources เป็นระดับความคุ้มครองสำหรับการเลือกผู้มีส่วนร่วมในแผนสิทธิประโยชน์หรือโปรแกรม เช่น แผนการรักษาพยาบาลสำหรับพนักงานเท่านั้น หรือ 2 เท่าเงินของเดือนสำหรับแผนประกันชีวิต</span><span class="sxs-lookup"><span data-stu-id="5c472-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="5c472-104">เมื่อกำหนดได้แล้ว ผลประโยชน์ของตัวเลือกความคุ้มครองจะใช้งานได้อีกครั้งและคุณสามารถเชื่อมโยงตัวเลือกกับหนึ่งแผนหรือมากกว่าได้</span><span class="sxs-lookup"><span data-stu-id="5c472-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="5c472-105">เมื่อมีการกำหนดตัวเลือกความคุ้มครองแล้ว ให้แนบตัวเลือกความคุ้มครองเข้ากับชนิดของแผนสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="5c472-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="5c472-106">ชนิดของแผนจะถูกเชื่อมโยงกับแผนสิทธิประโยชน์หรือโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="5c472-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="5c472-107">ตัวเลือกความคุ้มครองที่เชื่อมโยงกับชนิดของแผนจะพร้อมใช้งานกับแผนทั้งหมดที่สร้างขึ้นโดยชนิดของแผนนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="5c472-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="5c472-108">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ตัวเลือกความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="5c472-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="5c472-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="5c472-109">Select **New**.</span></span>

3. <span data-ttu-id="5c472-110">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5c472-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5c472-111">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5c472-111">Field</span></span> | <span data-ttu-id="5c472-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5c472-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5c472-113">**ตัวเลือกความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="5c472-113">**Coverage option**</span></span> | <span data-ttu-id="5c472-114">ชื่อเฉพาะของตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5c472-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="5c472-115">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="5c472-115">**Description**</span></span> | <span data-ttu-id="5c472-116">คำอธิบายเกี่ยวกับตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5c472-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="5c472-117">**รหัสความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="5c472-117">**Coverage code**</span></span> | <span data-ttu-id="5c472-118">รหัสความคุ้มครองจะกำหนดยอดเงินต่ำสุดและสูงสุดสำหรับแต่ละสิทธิ์ที่คุ้มครองชนิดของบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c472-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="5c472-119">รหัสความคุ้มครองจะระบุผู้ที่ได้รับการคุ้มครองหรือยอดเงินของความคุ้มครองที่ใช้ได้กับชนิดของแผน</span><span class="sxs-lookup"><span data-stu-id="5c472-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="5c472-120">คุณสามารถแสดงยอดเงินของความคุ้มครองเป็นเงินดอลลาร์หรือเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="5c472-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="5c472-121">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="5c472-121">For example:</span></span></br></br><span data-ttu-id="5c472-122">- **Emp + 1** – เพื่อให้เป็นไปตามเงื่อนไข พนักงานจะต้องเลือกผู้อยู่ในอุปการะหนึ่งราย (ถ้ามีการเลือกมากกว่าหนึ่งราย จะไม่สามารถดำเนินการได้อีกต่อไป)</span><span class="sxs-lookup"><span data-stu-id="5c472-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="5c472-123">- **Emp + ครอบครัว** – เพื่อความเหมาะสม พนักงานจะต้องเลือกผู้อยู่ในอุปการะอย่างน้อยสองราย</span><span class="sxs-lookup"><span data-stu-id="5c472-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="5c472-124">**จำนวนสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="5c472-124">**Maximum number**</span></span> | <span data-ttu-id="5c472-125">จำนวนของผู้อยู่ในอุปการะสูงสุด</span><span class="sxs-lookup"><span data-stu-id="5c472-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="5c472-126">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="5c472-126">**Status**</span></span> | <span data-ttu-id="5c472-127">สถานะของตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5c472-127">The status of the coverage option.</span></span> <span data-ttu-id="5c472-128">ถ้าสถานะของตัวเลือกความคุ้มครองถูกตั้งค่าเป็นไม่ใช้งาน คุณจะไม่สามารถเลือกตัวเลือกความคุ้มครองบนชนิดของแผน</span><span class="sxs-lookup"><span data-stu-id="5c472-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="5c472-129">**เปอร์เซ็นต์**</span><span class="sxs-lookup"><span data-stu-id="5c472-129">**Percent**</span></span> | <span data-ttu-id="5c472-130">ยอดเงินเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="5c472-130">The percent amount.</span></span> <span data-ttu-id="5c472-131">ฟิลด์นี้จะใช้งานได้ก็ต่อเมื่อ % x เงินเดือนถูกเลือกในฟิลด์รหัสความคุ้มครองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5c472-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="5c472-132">**ตัวหาร**</span><span class="sxs-lookup"><span data-stu-id="5c472-132">**Divisor**</span></span> | <span data-ttu-id="5c472-133">ตัวหารที่จะใช้ในการคำนวณเมื่อคุณเลือกรหัสความคุ้มครอง % x เงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5c472-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="5c472-134">**เปอร์เซ็นต์ต่ำสุด**</span><span class="sxs-lookup"><span data-stu-id="5c472-134">**Percent minimum**</span></span> | <span data-ttu-id="5c472-135">เปอร์เซ็นต์ต่ำสุดเมื่อคุณเลือกรหัสเปอร์เซ็นต์ความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5c472-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="5c472-136">**เปอร์เซ็นต์สูงสุด**</span><span class="sxs-lookup"><span data-stu-id="5c472-136">**Percent maximum**</span></span> | <span data-ttu-id="5c472-137">เปอร์เซ็นต์สูงสุดเมื่อคุณเลือกรหัสเปอร์เซ็นต์ความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5c472-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="5c472-138">ภายใต้ **ตัวเลือกสิทธิ์ของความสัมพันธ์ส่วนบุคคล** ให้แนบตัวเลือกสิทธิ์ของผู้ที่มีความสัมพันธ์ส่วนบุคคลที่เหมาะสมกับตัวเลือกความคุ้มครองแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="5c472-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="5c472-139">ภายใต้ **การบริการตนเอง** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5c472-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="5c472-140">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5c472-140">Field</span></span> | <span data-ttu-id="5c472-141">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5c472-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5c472-142">**อนุญาตจำนวนเงินจ่ายสมทบของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="5c472-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="5c472-143">ระบุว่าจะอนุญาตให้พนักงานปรับเปลี่ยนยอดเงินสมทบของสิทธิประโยชน์ด้วยตนเองเมื่อพวกเขาเลือกสิทธิประโยชน์ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5c472-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="5c472-144">ถ้าคุณเลือกกล่องกาเครื่องหมายนี้ ระบบจะคำนวณพารามิเตอร์ของแผนสิทธิประโยชน์ตามยอดเงินสมทบที่พนักงานป้อนไว้ในการบริการสิทธิประโยชน์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="5c472-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="5c472-145">**อนุญาตจำนวนเงินของความคุ้มครองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="5c472-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="5c472-146">ระบุว่าจะอนุญาตให้พนักงานปรับเปลี่ยนยอดเงินที่คุ้มครองของสิทธิประโยชน์ด้วยตนเองเมื่อพวกเขาเลือกสิทธิประโยชน์ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5c472-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="5c472-147">ถ้าคุณเลือกกล่องกาเครื่องหมายนี้ ระบบจะคำนวณพารามิเตอร์ของแผนสิทธิประโยชน์ตามยอดความคุ้มครองที่พนักงานป้อนไว้ในการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5c472-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="5c472-148">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5c472-148">Select **Save**.</span></span> 
