---
title: กำหนดและจัดการโปรแกรมสวัสดิการ
description: ทรัพยากรบุคคลให้ชุดของเครื่องมือที่สามารถถูกใช้เพื่อตั้งค่าและรักษาสวัสดิการ การหักลด และแผนค่าตอบแทนของผู้ปฏิบัติงานที่หน่วยงานนำเสนอ หรือประมวลผลสำหรับผู้ปฏิบัติงาน บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการตั้งค่าการจัดการสวัสดิการ
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b976bccf7f5da4483ec8a015f464db764b82a2f1
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197900"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="9512e-104">กำหนดและจัดการโปรแกรมสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9512e-104">Define and manage a benefits program</span></span>

<span data-ttu-id="9512e-105">ทรัพยากรบุคคลมีชุดของเครื่องมือที่สามารถถูกใช้เพื่อตั้งค่าและรักษาสวัสดิการ การหักลด และแผนค่าตอบแทนของผู้ปฏิบัติงานที่หน่วยงานนำเสนอหรือประมวลผลสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9512e-105">Human Resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="9512e-106">บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการตั้งค่าและการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9512e-106">This article provides information about how to set up and manage benefits.</span></span>

## <a name="benefit-setup"></a><span data-ttu-id="9512e-107">การตั้งค่าสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9512e-107">Benefit setup</span></span>

<span data-ttu-id="9512e-108">ก่อนที่ผู้ปฏิบัติงานจะสามารถถูกลงทะเบียนในสวัสดิการ คุณต้องสร้างองค์ประกอบของสวัสดิการแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="9512e-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="9512e-109">องค์ประกอบเหล่านี้รวมแผนสวัสดิการที่คล้ายกัน และกำหนดการตั้งค่าเริ่มต้น เช่น อัตราการหักลดและรายละเอียดทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="9512e-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="9512e-110">การตั้งค่าเหล่านี้หลายๆรายการสามารถถูกปรับปรุงได้ เมื่อผู้ปฏิบัติงานได้ถูกลงทะเบียนในสวัสดิการในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="9512e-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="9512e-111">สำหรับแผนสวัสดิการแต่ละแผน องค์กรสามารถเสนอตัวเลือกในการลงทะเบียนได้หลายตัวเลือก หรือผู้ปฏิบัติงานสามารถยกเว้นการลงทะเบียนในแผนได้</span><span class="sxs-lookup"><span data-stu-id="9512e-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="9512e-112">[![ขั้นตอนกระบวนการสวัสดิการ](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="9512e-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="9512e-113">องค์ประกอบของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9512e-113">Benefit elements</span></span>

<span data-ttu-id="9512e-114">ก่อนที่คุณจะเริ่มสร้างเพื่อสร้างสวัสดิการและการลงทะเบียนผู้ปฏิบัติงานในนั้น คุณต้องกำหนดองค์ประกอบที่สร้างสวัสดิการ: ชนิด แผน และตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="9512e-114">Before you begin to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="9512e-115">**ชนิด** – ชุดข้อมูลของแผนสำหรับสวัสดิการเฉพาะ เช่น การรักษาพยาบาลหรือที่จอดรถ</span><span class="sxs-lookup"><span data-stu-id="9512e-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="9512e-116">**แผน** – สวัสดิการเฉพาะที่ถูกระบุในสัญญาจากผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="9512e-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="9512e-117">**ตัวเลือก** – ระดับความครอบคลุม เช่น พนักงานเท่านั้นหรือพนักงานและคู่สมรส/หุ้นส่วน</span><span class="sxs-lookup"><span data-stu-id="9512e-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="9512e-118">สำหรับชนิดของสวัสดิการแต่ละชนิด เช่น การมองเห็นหรือทันตกรรม องค์กรสามารถเสนอแผนหนึ่งแผนขึ้นไปให้กับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9512e-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="9512e-119">สำหรับแผนแต่ละแผน องค์กรสามารถเสนอตัวเลือกที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="9512e-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="9512e-120">ตัวอย่างเช่น ผู้ปฏิบัติงานที่สามารถซื้อความครอบคลุมการประกันสุขภาพเงื่อนไขเพิ่มเติมที่หนึ่ง สอง หรือสามครั้งของเงินเดือนต่อปี</span><span class="sxs-lookup"><span data-stu-id="9512e-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="9512e-121">ชุดของแผนและตัวเลือกแต่ละชุดกลายเป็นสวัสดิการที่ผู้ปฏิบัติงานสามารถลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="9512e-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="9512e-122">[![รูปภาพสวัสดิการ](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="9512e-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="9512e-123">ความถูกต้องตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="9512e-123">Eligibility</span></span>
<span data-ttu-id="9512e-124">ปัจจัยหลายอย่างกำหนดสิทธิ์ของผู้ปฏิบัติงาน สำหรับชนิดต่างๆของสวัสดิการที่นายจ้างเสนอ</span><span class="sxs-lookup"><span data-stu-id="9512e-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="9512e-125">เมื่อคุณสร้างสวัสดิการใน Dynamics 365 Human Resources คุณสามารถตั้งค่าชนิดของสิทธิ์ที่ใช้กับสวัสดิการนั้น</span><span class="sxs-lookup"><span data-stu-id="9512e-125">When you create a benefit in Dynamics 365 Human Resources, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="9512e-126">คุณสามารถทำให้สวัสดิการพร้อมใช้งานกับผู้ปฏิบัติงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9512e-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="9512e-127">ตัวอย่างเช่น บริษัทบางแห่งเสนอบัตรผ่านการจอดรถให้กับพนักงานทั้งหมดให้เป็นสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9512e-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="9512e-128">เมื่อคุณสร้างสวัสดิการนี้ คุณตั้งค่าสิทธิ์เป็น **พนักงานทั้งหมดมีสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="9512e-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="9512e-129">สำหรับสวัสดิการอื่นๆ เช่น การอายัดเงินและการเก็บภาษี จะไม่มีการใช้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="9512e-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="9512e-130">เมื่อคุณสร้างชนิดของผลประโยชน์เหล่านี้ คุณตั้งค่าสิทธิ์เป็น **ข้ามกระบวนการของสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="9512e-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="9512e-131">ในตอนท้าย สิทธิ์ในสวัสดิการสามารถอ้างอิงตามกฎ</span><span class="sxs-lookup"><span data-stu-id="9512e-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="9512e-132">ตัวอย่างเช่น บริษัทเสนอชนิดสองชนิดของสวัสดิการการประกันสุขภาพให้กับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="9512e-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="9512e-133">พนักงานผู้บริหารมีสิทธิ์ในการได้รับแผนการประกันสุขภาพหนึ่งรายการ ในขณะที่พนักงานเต็มเวลาอื่นๆทั้งหมดมีสิทธิ์ในการได้รับแผนการประกันสุขภาพอื่น</span><span class="sxs-lookup"><span data-stu-id="9512e-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="9512e-134">ในทรัพยากรบุคคล คุณสามารถสร้างกฎการมีสิทธิ์ในสวัสดิการเพื่อค้นหาพนักงานผู้บริหาร และอีกกฎหนึ่งเพื่อค้นหาอื่นพนักงานเต็มเวลาอื่นทั้งหมด และจากนั้นใช้กฎเหล่านั้นกับสวัสดิการที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9512e-134">In Human Resources, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="9512e-135">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="9512e-135">Enrollment</span></span>
<span data-ttu-id="9512e-136">หลังจากที่คุณได้สร้างสวัสดิการที่องค์กรของคุณเสนอและกำหนดสิทธิ์ คุณสามารถลงทะเบียนผู้ปฏิบัติงานของคุณในสวัสดิการได้</span><span class="sxs-lookup"><span data-stu-id="9512e-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="9512e-137">คุณสามารถลงทะเบียนผู้ปฏิบัติงานเดี่ยวในสวัสดิการ หรือคุณสามารถลงทะเบียนผู้ปฏิบัติงานหลายรายในสวัสดิการหนึ่งรายการขึ้นไปในระหว่างกระบวนการเดี่ยว</span><span class="sxs-lookup"><span data-stu-id="9512e-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="9512e-138">บางครั้ง องค์กรหยุดการนำเสนอสวัสดิการบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="9512e-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="9512e-139">ในกรณีนี้ คุณต้องอัพเดสวัสดิการและผู้ปฏิบัติงานที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="9512e-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="9512e-140">วันหมดอายุของสวัสดิการโดยรวมทำให้คุณสามารถเปลี่ยนแปลงวันหมดอายุของทั้งสวัสดิการและการลงทะเบียนผู้ปฏิบัติงาน สำหรับสวัสดิการนั้นที่เวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="9512e-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="9512e-141">คุณยังสามารถเลือกผู้ปฏิบัติงานหลายรายที่ได้ลงทะเบียนในสวัสดิการ และเปลี่ยนวันที่สิ้นสุดของความครอบคลุมของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="9512e-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="9512e-142">ในทำนองเดียวกัน ส่วนขยายสวัสดิการโดยรวมทำให้คุณสามารถขยายวันหมดอายุของทั้งสวัสดิการและการลงทะเบียนผู้ปฏิบัติงานสำหรับสวัสดิการนั้น ถ้าคุณตัดสินใจที่จะเสนอสวัสดิการนานกว่าที่คุณได้วางแผนไว้ในตอนแรก</span><span class="sxs-lookup"><span data-stu-id="9512e-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>


