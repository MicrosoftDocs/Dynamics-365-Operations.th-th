---
title: ประมวลผลการมีสิทธิ์ในการลงทะเบียน
description: บทความนี้อธิบายถึงวิธีการรันกระบวนการมีสิทธิ์ในการลงทะเบียน
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 69ea23e4051a6975a5892cd027777c5a88472509
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114473"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="51fc3-103">ประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-103">Process enrollment eligibility</span></span>

<span data-ttu-id="51fc3-104">บทความนี้อธิบายถึงวิธีการรันกระบวนการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="51fc3-105">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **กำลังประมวลผลการมีสิทธิ์ในการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="51fc3-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="51fc3-106">ในกล่องโต้ตอบ **ดำเนินการประมวลผลสวัสดิการการลงทะเบียน** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="51fc3-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="51fc3-107">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="51fc3-107">Field</span></span> | <span data-ttu-id="51fc3-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="51fc3-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="51fc3-109">**รอบระยะเวลาการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="51fc3-109">**Enrollment period**</span></span> | <span data-ttu-id="51fc3-110">รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="51fc3-111">**นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="51fc3-111">**Legal entity**</span></span> | <span data-ttu-id="51fc3-112">นิติบุคคลที่จะประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="51fc3-113">**ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="51fc3-113">**Worker**</span></span> | <span data-ttu-id="51fc3-114">ผู้ปฏิบัติงานที่จะประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="51fc3-115">ถ้าคุณปล่อยฟิลด์นี้ว่างไว้ การมีสิทธิ์ในการลงทะเบียนจะมีการดำเนินการสำหรับผู้ปฏิบัติงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="51fc3-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="51fc3-116">**แผนสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="51fc3-116">**Benefit plan**</span></span> | <span data-ttu-id="51fc3-117">แผนสวัสดิการที่จะประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="51fc3-118">ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="51fc3-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="51fc3-119">ป้อนข้อมูลสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="51fc3-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="51fc3-120">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="51fc3-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="51fc3-121">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="51fc3-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="51fc3-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="51fc3-122">Select **OK**.</span></span> <span data-ttu-id="51fc3-123">กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="51fc3-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="51fc3-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="51fc3-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="51fc3-125">ดูผลลัพธ์ของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="51fc3-125">View Process Results</span></span>

<span data-ttu-id="51fc3-126">บทความนี้อธิบายถึงวิธีการดูผลลัพธ์กระบวนการการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="51fc3-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="51fc3-127">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **ผลลัพธ์ของกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="51fc3-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="51fc3-128">ในแบบฟอร์ม **ผลลัพธ์ของกระบวนการ** จะมีการระบุฟิลด์ต่อไปนี้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="51fc3-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="51fc3-129">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="51fc3-129">Field</span></span> | <span data-ttu-id="51fc3-130">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="51fc3-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="51fc3-131">**รหัสกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="51fc3-131">**Process ID**</span></span> | <span data-ttu-id="51fc3-132">รหัสเฉพาะสำหรับชุดของผู้ปฏิบัติงาน นิติบุคคล และการรันกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="51fc3-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="51fc3-133">**ชนิดของกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="51fc3-133">**Process type**</span></span> | <span data-ttu-id="51fc3-134">ซึ่งระบุกระบวนการที่มีการรัน</span><span class="sxs-lookup"><span data-stu-id="51fc3-134">This identifies the process that was run.</span></span> <span data-ttu-id="51fc3-135">ตัวอย่างเช่น: การลงทะเบียน </span><span class="sxs-lookup"><span data-stu-id="51fc3-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="51fc3-136">**การประทับเวลา**</span><span class="sxs-lookup"><span data-stu-id="51fc3-136">**Time stamp**</span></span> | <span data-ttu-id="51fc3-137">เวลาที่มีการรันกระบวนการของการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="51fc3-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="51fc3-138">**นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="51fc3-138">**Legal entity**</span></span> | <span data-ttu-id="51fc3-139">นิติบุคคลที่ระบุในระหว่างกระบวนการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="51fc3-140">**ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="51fc3-140">**Worker**</span></span> | <span data-ttu-id="51fc3-141">ผู้ปฏิบัติงานที่ได้รับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="51fc3-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="51fc3-142">\*\*แผน</span><span class="sxs-lookup"><span data-stu-id="51fc3-142">\*\*Plan</span></span> | <span data-ttu-id="51fc3-143">แผนสวัสดิการที่มีความพยายามในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="51fc3-144">**กฎการมีสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="51fc3-144">**Eligibility rule**</span></span> | <span data-ttu-id="51fc3-145">กฎการมีสิทธิ์ที่ได้รับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="51fc3-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="51fc3-146">ถ้าพบข้อผิดพลาดก่อนที่จะมีการรันสิทธิ์ นี่จะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="51fc3-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="51fc3-147">ตัวอย่างเช่น ถ้ายังไม่ได้กำหนดค่าตอบแทนสำหรับผู้ปฏิบัติงาน กระบวนการการมีสิทธิ์จะไม่รันและฟิลด์นี้จะถูกปล่อยว่างไว้</span><span class="sxs-lookup"><span data-stu-id="51fc3-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="51fc3-148">**สถานะของผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="51fc3-148">**Result status**</span></span> | <span data-ttu-id="51fc3-149">การทำเช่นนี้จะเป็นมีสิทธิ์หรือไม่มีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="51fc3-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="51fc3-150">สถานะผลลัพธ์จะไม่สามารถใช้ได้ ถ้าผู้ปฏิบัติงานไม่ตรงกับเกณฑ์ของกฎการมีสิทธิ์ ถ้าผู้ปฏิบัติงานไม่มีข้อมูลที่จำเป็น เช่น ความถี่ในการชำระค่าจ้างหรือค่าตอบแทนคงที่ หรือหากมีข้อมูลที่ขาดหายไปในแผนสวัสดิการที่ทำให้ผู้ปฏิบัติงานไม่ได้ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="51fc3-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="51fc3-151">**ข้อความผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="51fc3-151">**Result message**</span></span> | <span data-ttu-id="51fc3-152">บ่งชี้ว่าเหตุใดผู้ปฏิบัติงานจึงไม่มีสิทธิ์สำหรับแผนสวัสดิการ หรือมีการส่งผ่านกฎการมีสิทธิ์ที่เหมาะสมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="51fc3-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

