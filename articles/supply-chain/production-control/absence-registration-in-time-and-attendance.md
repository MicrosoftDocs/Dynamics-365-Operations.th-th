---
title: การลงทะเบียนการขาดงานในเวลาและการเข้างาน
description: หัวข้อนี้อธิบายวิธีการจัดการการลงทะเบียนการขาดงานในเวลาและการเข้างาน
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12a61f23ac5a16000275e53d3901c8aea202bab0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966641"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="bb78b-103">การลงทะเบียนการขาดงานในเวลาและการเข้างาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb78b-104">หัวข้อนี้อธิบายแนวคิดสำหรับการขาดงาน และอธิบายวิธีการจัดการการขาดงานในเวลาและการเข้างาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="bb78b-105">การขาดงานที่ขึ้นอยู่กับชั่วโมงทำงานปกติ</span><span class="sxs-lookup"><span data-stu-id="bb78b-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="bb78b-106">ผู้ปฏิบัติงานจะถือว่าเป็นงานที่ขาดงานสำหรับชั่วโมงใดๆ ที่พวกเขาไม่ทำงานในระหว่างชั่วโมงการทำงานปกติของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="bb78b-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="bb78b-107">มีการกำหนดชั่วโมงทำงานปกติในโพรไฟล์เวลามาตรฐานของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="bb78b-108">ตัวอย่างเช่น ผู้ปฏิบัติงานทำงานในโพรไฟล์วันที่ตอกบัตรเข้าที่เวลา 7:00 น. และตอกบัตรออกที่เวลา 3:00 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="bb78b-109">ถ้าผู้ปฏิบัติงานตอกบัตรเข้าที่เวลา 9:00 น. เขาถือว่าขาดตั้งแต่ 7:00 น. ถึง 9:00 น. ในวันนั้น</span><span class="sxs-lookup"><span data-stu-id="bb78b-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="bb78b-110">ในกรณีนี้ ผู้ปฏิบัติงานที่จะได้รับพร้อมต์ให้ป้อนเหตุผลสำหรับการขาดงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="bb78b-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="bb78b-111">พวกเขาสามารถระบุเหตุผลได้ ด้วยการเลือกรหัสการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="bb78b-112">รหัสการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-112">Absence codes</span></span>

<span data-ttu-id="bb78b-113">รหัสการขาดงานกำหนดชนิดต่างๆ ของการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="bb78b-114">รหัสการขาดงานถูกกำหนดโดยบริษัท</span><span class="sxs-lookup"><span data-stu-id="bb78b-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="bb78b-115">กฎต่างๆ สามารถใช้ได้กับรหัสการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="bb78b-116">ตัวอย่างเช่น สามารถกำหนดรหัสการขาดงานเพื่อหัก หรือช่วยเหลือค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="bb78b-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="bb78b-117">ตัวอย่างเช่น บริษัทกำหนดรหัสการขาดงาน **ล่าช้า** ที่ผู้ปฏิบัติงานใช้ ถ้าพวกเขามาช้า และไม่มีเหตุผลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="bb78b-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="bb78b-118">นอกจากนี้ บริษัทยังกำหนดรหัสการขาดงาน **หลักสูตรภายใน** ที่ผู้ปฏิบัติงานใช้ สำหรับเวลาที่พวกเขาใช้ในการเข้าร่วมหลักสูตรภายใน</span><span class="sxs-lookup"><span data-stu-id="bb78b-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="bb78b-119">รหัสการขาดงานเหล่านี้สามารถถูกตั้งค่าได้เพื่อให้ **ล่าช้า** หักจากค่าจ้างของผู้ปฏิบัติงาน แต่ **หลักสูตรภายใน** ไม่หักจากค่าจ้างของผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="bb78b-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="bb78b-120">คุณสามารถตั้งค่ารหัสการขาดงานโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="bb78b-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="bb78b-121">รหัสการขาดงานเหล่านี้สามารถถูกใช้ในการคำนวณเวลาของผู้ปฏิบัติงาน เมื่อมีการลงทะเบียนการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="bb78b-122">โพรไฟล์เวลาของผู้ปฏิบัติงานกำหนดว่า จะใช้รหัสการขาดงานสำหรับเวลามาตรฐานหรือทำงานแบบยืดหยุ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="bb78b-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="bb78b-123">ตั้งค่าเวลามาตรฐาน และเวลาแบบยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="bb78b-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="bb78b-124">ตั้งค่าคอนฟิกพารามิเตอร์สำหรับเวลามาตรฐานและเวลาแบบยืดหยุ่น โดยใช้ตัวเลือก **แทรกการขาดงานอัตโนมัติ** และ **แทรก Flex อัตโนมัติ-** ในหน้า **พารามิเตอร์เวลาและการเข้างาน**</span><span class="sxs-lookup"><span data-stu-id="bb78b-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="bb78b-125">กลุ่มการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-125">Absence groups</span></span>

<span data-ttu-id="bb78b-126">รหัสการขาดงานถูกจัดกลุ่มเป็นกลุ่มการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="bb78b-127">คุณใช้กลุ่มการขาดงานเพื่อจัดกลุ่มรหัสการขาดงานที่มีลักษณะร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="bb78b-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="bb78b-128">ตัวอย่างประกอบด้วย รหัสการขาดงานสำหรับการขาดงานตามกฎหมายหรือการขาดงาน เนื่องจากการนัดหมายของแพทย์ การเข้าร่วมระบบยุติธรรม หรือลูกป่วย</span><span class="sxs-lookup"><span data-stu-id="bb78b-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="bb78b-129">การขาดงานที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="bb78b-129">Planned absence</span></span>

<span data-ttu-id="bb78b-130">หากคุณทราบว่า พนักงานจะขาดงานเป็นระยะเวลาหนึ่ง เช่น วันหยุดที่กำลังจะมาถึง คุณสามารถใช้การขาดงานที่วางแผนไว้ได้</span><span class="sxs-lookup"><span data-stu-id="bb78b-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="bb78b-131">คุณตั้งค่าการขาดงานที่วางแผนไว้ตามการตั้งค่าคอนฟิกรหัสการขาดงาน เพื่อให้พิจารณาการขาดงานที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="bb78b-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="bb78b-132">เมื่อคุณตั้งค่าการขาดงานที่วางแผนไว้ คุณไม่ได้ถูกพร้อมท์สำหรับรหัสการขาดงานในระหว่างรอบระยะเวลาการขาดงาน เมื่อมีการคำนวณการลงทะเบียนเวลาของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bb78b-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="bb78b-133">คุณสามารถกำหนดการขาดงานที่วางแผนไว้สำหรับผู้ปฏิบัติงานเดี่ยว หรือคุณสามารถกำหนดชุดงานเพื่อปรับปรุงการขาดงานที่วางแผนไว้จำนวนมากสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="bb78b-134">ตั้งค่าการขาดงานที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="bb78b-134">Set up planned absence</span></span>

1. <span data-ttu-id="bb78b-135">เลือก **ทรัพยากรบุคคล** &gt; **ผู้ปฏิบัติงาน** &gt; **พนักงาน** และเลือกพนักงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="bb78b-136">เลือก **เวลา** &gt; **การกำหนดเวลา** &gt; **การลงทะเบียนการขาดงานเวลา** และตั้งค่าการขาดงานที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="bb78b-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="bb78b-137">การขาดงานที่วางแผนไว้ที่หยุดชะงัก</span><span class="sxs-lookup"><span data-stu-id="bb78b-137">Interrupted planned absence</span></span>

<span data-ttu-id="bb78b-138">ถ้าคุณใช้ตัวเลือก **ขัดจังหวะ** เมื่อคุณตั้งค่าการขาดงานที่วางแผนไว้การขาดงานที่วางแผนไว้จะหยุดชะงักลง ถ้าผู้ปฏิบัติงานลงทะเบียนในระหว่างรอบระยะเวลาการขาดงานที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="bb78b-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="bb78b-139">การขาดงานที่วางแผนไว้จะถูกกำหนดเป็น **หยุดชะงัก** และจะไม่มีผลต่อการคำนวณในอนาคต</span><span class="sxs-lookup"><span data-stu-id="bb78b-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="bb78b-140">ตั้งค่าการขาดงานที่วางแผนไว้สำหรับการขัดจังหวะ</span><span class="sxs-lookup"><span data-stu-id="bb78b-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="bb78b-141">เปิดหน้า **การลงทะเบียนการขาดงานเวลา** ตามที่อธิบายไว้ในกระบวนงานสำหรับการตั้งค่าการขาดงานที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="bb78b-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="bb78b-142">เลือก **ขัดจังหวะ**</span><span class="sxs-lookup"><span data-stu-id="bb78b-142">Select **Interrupt**.</span></span>

<span data-ttu-id="bb78b-143">ตัวเลือก **ขัดจังหวะ** ใช้เมื่อมีการลงทะเบียนเวลาโดยใช้เทอร์มินัลการผลิตหรืออุปกรณ์การผลิต</span><span class="sxs-lookup"><span data-stu-id="bb78b-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="bb78b-144">ตัวเลือกไม่สามารถใช้ได้ ถ้ามีการป้อนการลงทะเบียนบนหน้าการคำนวณและการอนุมัติ หรือหน้า **บัตรลงเวลาอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="bb78b-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="bb78b-145">ตัวอย่างของการใช้การขาดงานในโพรไฟล์การทำงานแบบยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="bb78b-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="bb78b-146">ตัวอย่างสามรายการต่อไปนี้แสดงวิธีการคำนวณการขาดงานในโพรไฟล์ที่มีรอบระยะเวลาที่ทำงานแบบยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="bb78b-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="bb78b-147">ตัวอย่างใช้โพรไฟล์ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bb78b-147">The examples use the following profile.</span></span>

| <span data-ttu-id="bb78b-148">การตอกบัตรเข้า</span><span class="sxs-lookup"><span data-stu-id="bb78b-148">Clock-in</span></span> | <span data-ttu-id="bb78b-149">เวลามาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-149">Standard time</span></span>    | <span data-ttu-id="bb78b-150">ตัวแบ่ง</span><span class="sxs-lookup"><span data-stu-id="bb78b-150">Break</span></span>             | <span data-ttu-id="bb78b-151">เวลามาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-151">Standard time</span></span> | <span data-ttu-id="bb78b-152">การทำงานแบบยืดหยุ่นเวลา-</span><span class="sxs-lookup"><span data-stu-id="bb78b-152">Flex-</span></span>        | <span data-ttu-id="bb78b-153">การตอกบัตรออก</span><span class="sxs-lookup"><span data-stu-id="bb78b-153">Clock-out</span></span> | <span data-ttu-id="bb78b-154">การทำงานแบบยืดหยุ่นเวลา+</span><span class="sxs-lookup"><span data-stu-id="bb78b-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="bb78b-155">8 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-155">8 AM</span></span>     | <span data-ttu-id="bb78b-156">9 น. ถึง 11:30 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="bb78b-157">11:30 น. กับ 12 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="bb78b-158">12 น. ถึง 15 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-158">12 PM to 3 PM</span></span> | <span data-ttu-id="bb78b-159">15 น. ถึง 16 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-159">3 PM to 4 PM</span></span> | <span data-ttu-id="bb78b-160">16 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-160">4 PM</span></span>      | <span data-ttu-id="bb78b-161">16 น. ถึง 18 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="bb78b-162">ตัวอย่างที่ 1: การลงชื่อออกในระหว่างระยะเวลาทำงานแบบยืดหยุ่น-</span><span class="sxs-lookup"><span data-stu-id="bb78b-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="bb78b-163">ผู้ปฏิบัติงานตอกบัตรเข้าที่เวลา 8:00 น.และตอกบัตรออกที่เวลา 15:30 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="bb78b-164">ในกรณีนี้ เนื่องจากผู้ปฏิบัติงานตอกบัตรออกในระหว่างช่วงทำงานแบบยืดหยุ่น- ไม่มีการคำนวณการขาดงาน และเวลาครึ่งชั่วโมงจะถูกหักออกจากยอดดุลการทำงานแบบยืดหยุ่นของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="bb78b-165">ตัวอย่างที่ 2: การลงชื่อออกในระหว่างรอบระยะเวลามาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="bb78b-166">ผู้ปฏิบัติงานตอกบัตรเข้าที่เวลา 8:00 น.และตอกบัตรออกที่เวลา 14:30 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="bb78b-167">ในกรณีนี้ เนื่องจากผู้ปฏิบัติงานที่ตอกบัตรออกในระหว่างรอบระยะเวลามาตรฐาน การขาดงานถูกคำนวณตั้งแต่ 14:30 น. ถึง 16 น. และมีการลงทะเบียนรอบระยะเวลาการขาดงานเป็น 1.5 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="bb78b-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="bb78b-168">จำเป็นต้องใช้รหัสการขาดงานสำหรับรอบระยะเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="bb78b-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="bb78b-169">ตัวอย่างที่ 3: การลงชื่อออกในระหว่างระยะเวลาทำงานแบบยืดหยุ่น+</span><span class="sxs-lookup"><span data-stu-id="bb78b-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="bb78b-170">ผู้ปฏิบัติงานตอกบัตรเข้าที่เวลา 8:00 น.และตอกบัตรออกที่เวลา 16:30 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="bb78b-171">ในกรณีนี้ เนื่องจากผู้ปฏิบัติงานตอกบัตรออกในระหว่างช่วงทำงานแบบยืดหยุ่น+ ไม่มีการคำนวณการขาดงาน และเวลาครึ่งชั่วโมงจะถูกเพิ่มไปยังยอดดุลการทำงานแบบยืดหยุ่นของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="bb78b-172">การขาดงานในกระบวนการคำนวณและการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="bb78b-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="bb78b-173">การลงทะเบียนเวลาของผู้ปฏิบัติงานต้องถูกคำนวณและได้รับอนุมัติ ก่อนที่จะสามารถถูกโอนย้ายไปยังระบบค่าจ้างเป็นรายการค่าจ้างได้</span><span class="sxs-lookup"><span data-stu-id="bb78b-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="bb78b-174">ผู้อนุมัติสามารถเปลี่ยนการลงทะเบียนเวลาของผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="bb78b-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="bb78b-175">ผู้อนุมัติสามารถแม้กระทั่งเปลี่ยนการขาดงานใดๆ ที่ผู้ปฏิบัติงานได้ลงทะเบียนได้</span><span class="sxs-lookup"><span data-stu-id="bb78b-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="bb78b-176">ถ้าผู้อนุมัติป้อนรอบระยะเวลาที่มีรหัสการขาดงานด้วยตนเอง รหัสการขาดงานสำหรับรอบระยะเวลานั้นจะไม่ได้ถูกแทนที่โดยเรียงตามรหัสการขาดงานค่าเริ่มต้น จากพารามิเตอร์เวลาและการเข้างาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="bb78b-177">ตัวอย่างเช่น ผู้ปฏิบัติงานตอกบัตรเข้าที่เวลา 10 น. และเลือกรหัสการขาดงานที่บ่งชี้ว่า เธอล่าช้า</span><span class="sxs-lookup"><span data-stu-id="bb78b-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="bb78b-178">ภายหลัง ผู้ปฏิบัติงานแจ้งให้หัวหน้างานของเธอทราบว่า เธอมีการนัดหมายของแพทย์ตั้งแต่ 8 น.ถึง 10 น.</span><span class="sxs-lookup"><span data-stu-id="bb78b-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="bb78b-179">การนัดหมายของแพทย์ไม่ควรเป็นเหตุในการหักค่าจ้างของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="bb78b-180">ดังนั้น ในกรณีนี้ ผู้ควบคุมงานสามารถปรับปรุงเวลาสองชั่วโมงของการขาดงานตั้งแต่ 8 น. ถึง 10 น. ได้ โดยการป้อนรหัสการขาดงานที่ระบุการเจ็บป่วยเป็นเวลาสองชั่วโมงเหล่านั้นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bb78b-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="bb78b-181">คำนวณ และอนุมัติการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="bb78b-181">Calculate and approve absence</span></span>

- <span data-ttu-id="bb78b-182">เลือก **เวลา การเข้างาน** &gt; **ตรวจทาน และอนุมัติ** &gt; **อนุมัติหรือคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="bb78b-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>
