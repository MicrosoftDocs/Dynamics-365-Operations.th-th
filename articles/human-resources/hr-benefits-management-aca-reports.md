---
title: สร้างรายงานกฎหมายประกันสุขภาพในการจัดการสวัสดิการ
description: หัวข้อนี้อธิบายวิธีการจัดการสวัสดิการช่วยคุณในการติดตามข้อมูลที่รายงานบนฟอร์ม 1095-B และฟอร์ม 1095-C สำหรับข้อตกลงของนายจ้างด้านกฎหมายประกันสุขภาพ (ACA)
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a41195ea3b52a707ce9deae38f12eb90de2ff5aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805813"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="5f4cb-103">สร้างรายงาน ACA ในการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5f4cb-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5f4cb-104">การจัดการสวัสดิการช่วยคุณในการติดตามข้อมูลที่รายงานบนฟอร์ม 1095-B และฟอร์ม 1095-C สำหรับข้อตกลงของนายจ้างด้านกฎหมายประกันสุขภาพ (ACA)</span><span class="sxs-lookup"><span data-stu-id="5f4cb-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="5f4cb-105">เช่นเดียวกับความสามารถในการรายงาน ACA ในพื้นที่ทำงาน **สวัสดิการ** เก่า ฟังก์ชันนี้จะใช้กับนิติบุคคลในสหรัฐอเมริกาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5f4cb-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="5f4cb-106">เมื่อต้องการใช้ฟังก์ชันนี้ คุณต้องเปิด **การจัดการสวัสดิการขั้นสูง** ก่อน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="5f4cb-107">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการจัดการสวัสดิการที่สําคัญ โปรดดูที่ [เปิดใช้งานหรือปิดใช้งานการจัดการสวัสดิการ](hr-admin-manage-features.md#enable-or-disable-benefits-management)</span><span class="sxs-lookup"><span data-stu-id="5f4cb-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f4cb-108">คุณสามารถใช้การรายงาน ACA ได้จากพื้นที่ทำงาน **การจัดการสวัสดิการ** หรือพื้นที่ทำงาน **สวัสดิการ** เก่าเท่านั้น ไม่ใช่จากทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="5f4cb-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="5f4cb-109">ตัวอย่างเช่น ถ้าคุณสลับไปยังการจัดการสวัสดิการ การรายงาน ACA จะพร้อมใช้งานจากพื้นที่ทำงาน **การจัดการสวัสดิการ** เท่านั้นไม่ใช่จากพื้นที่ทำงาน **สวัสดิการ** เก่า</span><span class="sxs-lookup"><span data-stu-id="5f4cb-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="5f4cb-110">ถ้าคุณสลับไปยังการจัดการสวัสดิการในระหว่างปีการลงทะเบียน คุณต้องตั้งค่าคอนฟิกข้อมูลพนักงานอย่างถูกต้องตลอดปีในการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5f4cb-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="5f4cb-111">ด้วยวิธีนี้ คุณจึงมั่นใจว่าจะได้รับข้อมูลการรายงานที่ถูกต้องตลอดปี</span><span class="sxs-lookup"><span data-stu-id="5f4cb-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="5f4cb-112">การเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5f4cb-112">Getting started</span></span>

<span data-ttu-id="5f4cb-113">เมื่อต้องการติดตามข้อมูลฟอร์ม 1095 ก่อนอื่น ให้สร้างกลุ่มความครอบคลุมของชุดสินค้าประเภทชุดหนึ่งกลุ่มหรือมากกว่านั้น</span><span class="sxs-lookup"><span data-stu-id="5f4cb-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="5f4cb-114">กลุ่มเหล่านี้ระบุข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="5f4cb-115">ข้อเสนอความครอบคลุมที่มอบให้แก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="5f4cb-116">ส่วนแบ่งของพนักงานของค่าจ้างพิเศษรายเดือนที่มีต้นทุนต่ำสุด ถ้าต้นทุนสูงกว่าบรรทัดความยากจนของรัฐบาลกลาง</span><span class="sxs-lookup"><span data-stu-id="5f4cb-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="5f4cb-117">การรักษาข้อมูลส่วนบุคคลที่ใช้โดยนายจ้าง ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="5f4cb-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="5f4cb-118">มีกลุ่มความคุ้มครอง Affordable Care ช่วยให้คุณสามารถจัดการข้อมูลนี้ให้กับเรกคอร์ดพนักงานหลายเรกคอร์ดที่มีเงื่อนไขเหมือนกันได้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="5f4cb-119">คุณสามารถกําหนดกลุ่มให้กับพนักงานหนึ่งคนหรือมากกว่าได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="5f4cb-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="5f4cb-120">สร้างหรือแก้ไขกลุ่มความคุ้มครอง Affordable Care ใหม่</span><span class="sxs-lookup"><span data-stu-id="5f4cb-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="5f4cb-121">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ให้เลือก **ลุ่มความคุ้มครอง Affordable Care**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![การเลือกกลุ่มความคุ้มครอง Affordable Care](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="5f4cb-123">เลือก **สร้าง** เพื่อสร้างกลุ่มความคุ้มครอง Affordable Care หรือ **แก้ไข** เพื่อเปลี่ยนแปลงกลุ่มที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="5f4cb-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![การเลือกสร้างหรือแก้ไข](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="5f4cb-125">ตั้งค่าฟิลด์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-125">Set the following fields.</span></span>

    | <span data-ttu-id="5f4cb-126">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5f4cb-126">Field</span></span> | <span data-ttu-id="5f4cb-127">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5f4cb-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="5f4cb-128">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="5f4cb-128">Name</span></span> | <span data-ttu-id="5f4cb-129">ป้อนชื่อสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="5f4cb-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="5f4cb-130">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5f4cb-130">Description</span></span> | <span data-ttu-id="5f4cb-131">ป้อนคำอธิบายของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="5f4cb-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="5f4cb-132">ข้อเสนอความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5f4cb-132">Offer of coverage</span></span> | <span data-ttu-id="5f4cb-133">ความครอบคลุมที่เสนอให้แก่พนักงาน คู่สมรส หรือคู่ครอง และผู้อยู่ในอุปการะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="5f4cb-134">ค่าจ่ายร่วมของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-134">Employee share of cost</span></span> | <span data-ttu-id="5f4cb-135">จำนวนที่พนักงานรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="5f4cb-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="5f4cb-136">ข้อยกเว้นความรับผิดที่เกี่ยวข้องสำหรับส่วน 4980H</span><span class="sxs-lookup"><span data-stu-id="5f4cb-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="5f4cb-137">Safe Harbor หรือเปลี่ยนรหัสการปลดปล่อย 4980H</span><span class="sxs-lookup"><span data-stu-id="5f4cb-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="5f4cb-138">เดือนที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-138">Plan start month</span></span> | <span data-ttu-id="5f4cb-139">เลือกเดือนปฏิทินเมื่อปีแผนสวัสดิการของคุณเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5f4cb-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="5f4cb-140">กลุ่มมีผลบังคับใช้ตั้งแต่</span><span class="sxs-lookup"><span data-stu-id="5f4cb-140">Group valid from</span></span> | <span data-ttu-id="5f4cb-141">วันที่แรกที่เรกคอร์ดนี้มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="5f4cb-142">กลุ่มมีผลบังคับใช้ถึง</span><span class="sxs-lookup"><span data-stu-id="5f4cb-142">Group valid through</span></span> | <span data-ttu-id="5f4cb-143">วันที่สุดท้ายที่เรกคอร์ดนี้มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-143">The last date when this record is valid.</span></span> <span data-ttu-id="5f4cb-144">ถ้าไม่มีวันหมดอายุ ให้ป้อน **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-144">If there is no expiration date, enter **Never**.</span></span> |

    ![การสร้างกลุ่มความครอบคลุม](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="5f4cb-146">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="5f4cb-147">การกําหนดพนักงานหลายคนให้กับกลุ่มความคุ้มครอง Affordable Care</span><span class="sxs-lookup"><span data-stu-id="5f4cb-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="5f4cb-148">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ให้เลือก **ลุ่มความคุ้มครอง Affordable Care**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="5f4cb-149">เลือกกลุ่มที่จะกําหนดพนักงานให้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="5f4cb-150">เลือก **การมอบหมายโดยรวม**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-150">Select **Mass assignment**.</span></span>

    ![การเลือก การมอบหมายโดยรวม](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="5f4cb-152">เลือกพนักงานในรายการ แล้วเลือก **กําหนด**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-152">Select employees in the list, and then select **Assign**.</span></span>

    ![กําหนดพนักงานที่เลือกให้กลุ่ม](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="5f4cb-154">รักษาตัวเลือกความคุ้มครองหลายรุ่น</span><span class="sxs-lookup"><span data-stu-id="5f4cb-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="5f4cb-155">คุณสามารถรักษากลุ่มความคุ้มครองหลายรุ่น</span><span class="sxs-lookup"><span data-stu-id="5f4cb-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="5f4cb-156">เมื่อเกิดการเปลี่ยนแปลงบางอย่างในองค์กรหรือสวัสดิการที่เสนอ คุณสามารถรักษาข้อมูลล่าสุดของกลุ่มไว้ได้โดยไม่ต้องสร้างกลุ่มใหม่และมอบหมายพนักงานให้กับกลุ่มนั้นใหม่</span><span class="sxs-lookup"><span data-stu-id="5f4cb-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="5f4cb-157">หลังจากที่คุณได้สร้างกลุ่มความคุ้มครอง Affordable Care แล้ว คุณสามารถกําหนดพนักงานให้กลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="5f4cb-158">นอกจากนี้คุณยังสามารถกําหนดพนักงานแต่ละคนให้กับกลุ่มและระบุว่าข้อมูล ACA มีการติดตามและรายงานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5f4cb-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="5f4cb-159">หากคุณไม่ต้องติดตามและรายงานข้อมูล ACA ของพนักงาน คุณสามารถตั้งค่าตัวเลือก **รายงานความคุ้มครอง** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="5f4cb-160">ตัวอย่างเช่น คุณอาจมีพนักงานแบบชั่วคราวซึ่งไม่ต้องการการรายงาน ACA</span><span class="sxs-lookup"><span data-stu-id="5f4cb-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="5f4cb-161">การแทนที่ค่าเริ่มต้นของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-161">Override default values for an employee</span></span>

<span data-ttu-id="5f4cb-162">สำหรับพนักงานที่ถูกกำหนดกลุ่มความคุ้มครอง Affordable Care คุณสามารถเปลี่ยนแปลงตัวเลือกต่อไปนี้ในช่วงเดือนที่ต้องการค่าที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="5f4cb-163">ข้อเสนอความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5f4cb-163">Offer of coverage</span></span>
- <span data-ttu-id="5f4cb-164">ค่าจ่ายร่วมของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-164">Employee share of cost</span></span>
- <span data-ttu-id="5f4cb-165">ข้อยกเว้นความรับผิดที่เกี่ยวข้องสำหรับส่วน 4980H</span><span class="sxs-lookup"><span data-stu-id="5f4cb-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="5f4cb-166">ดูรายงาน ACA 2020 คุณต้องรายงานทั้งรหัสไปรษณีย์ของงานและรหัสไปรษณีย์ที่บ้านในแบบฟอร์ม 1095-C</span><span class="sxs-lookup"><span data-stu-id="5f4cb-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="5f4cb-167">โปรแกรมจะเติมค่าให้โดยอัตโนมัติ ตามที่ตั้งที่ใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="5f4cb-168">ถ้าสถานที่ใดสถานที่หนึ่งแตกต่างกันระหว่างส่วนใด ๆ ของปี คุณต้องแทนที่ค่า</span><span class="sxs-lookup"><span data-stu-id="5f4cb-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="5f4cb-169">ฟิลด์ **รหัสไปรษณีย์** (บรรทัด 17) ของรายงาน 1095-C เติมเฉพาะเมื่อรหัส **ข้อเสนอความคุ้มครอง** มี **1L** ถึง **1Q** ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="5f4cb-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="5f4cb-170">**1L, 1M หรือ 1N:** รหัสไปรษณีย์ที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="5f4cb-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="5f4cb-171">**1O, 1P, 1Q:** รหัสไปรษณีย์ของงานหลัก</span><span class="sxs-lookup"><span data-stu-id="5f4cb-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="5f4cb-172">หากต้องการป้อนข้อยกเว้นให้กับค่าใด ๆ ของกลุ่มความคุ้มครอง Affordable Care ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="5f4cb-173">ในพื้นที่ทำงาน **การจัดการบุคลากร** ให้เลือก **ลิงก์** แล้วเลือก **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="5f4cb-174">เลือกพนักงานในรายชื่อ</span><span class="sxs-lookup"><span data-stu-id="5f4cb-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="5f4cb-175">บนแท็บ **การจ้างงาน** ในส่วน **ข้อมูลเพิ่มเติม** ให้เลือก **ความคุ้มครอง Affordable Care**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![การเปลี่ยนตัวเลือกของพนักงานแต่ละคน](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="5f4cb-177">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-177">Select **Edit**.</span></span>
5. <span data-ttu-id="5f4cb-178">ให้เลือกกล่องกาเครื่องหมาย **แทนที่ค่าเริ่มต้น** และเปลี่ยนค่าอื่น ๆ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="5f4cb-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![การแทนที่ค่าเริ่มต้น](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="5f4cb-180">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="5f4cb-181">รายงานความคุ้มครองสุขภาพ</span><span class="sxs-lookup"><span data-stu-id="5f4cb-181">Report health care coverage</span></span>

<span data-ttu-id="5f4cb-182">คุณต้องติดตามความครอบคลุมของประกันสุขภาพที่สนับสนุนโดยนายจ้าง แบบประกันด้วยตนเองสำหรับพนักงานเต็มเวลาและพนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="5f4cb-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="5f4cb-183">รวมพนักงานแต่ละคนรวมทั้งผู้อยู่ในอุปการะไว้ในรายงาน 1095-C ในช่วงเดือนที่มีความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="5f4cb-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="5f4cb-184">เมื่อต้องการบ่งชี้ว่าต้องรายงานแผนสวัสดิการหรือไม่ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="5f4cb-185">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ให้เลือก **แผนสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="5f4cb-186">เลือกแผนสวัสดิการที่จะรายงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="5f4cb-187">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-187">Select **Edit**.</span></span>
4. <span data-ttu-id="5f4cb-188">ตั้งค่าตัวเลือก **รายงานภายใต้ Affordable Care Act** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![การรายงานความคุ้มครองสุขภาพ](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="5f4cb-190">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-190">Select **Save**.</span></span>

<span data-ttu-id="5f4cb-191">หากพนักงานเลือกความคุ้มครองของสุขภาพผู้อยู่ในอุปการะ รอบระยะเวลาความคุ้มครองผู้อยู่ในอุปการะจะกําหนดตามวันที่ที่ผู้อยู่ในอุปการะลงทะเบียนหรือลบออกไป</span><span class="sxs-lookup"><span data-stu-id="5f4cb-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="5f4cb-192">วันที่คุ้มครองผู้อยู่ในอุปการะจะถูกคํานวณโดยอัตโนมัติตามรอบระยะเวลาเมื่อผู้อยู่ในอุปการะมีสิทธิ์และใช้งานในแผนในระหว่างปีการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="5f4cb-193">สร้างแบบฟอร์ม 1095-B และ 1095-C</span><span class="sxs-lookup"><span data-stu-id="5f4cb-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="5f4cb-194">คุณยังสามารถสร้างแบบฟอร์ม ACA 1095-B และ 1095-C และกระจายให้กับพนักงานของคุณแต่ละคนได้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="5f4cb-195">นอกจากนี้คุณยังสามารถสร้างแบบฟอร์ม 1095-C และไฟล์ที่ส่ง 1094-C ที่สัมพันธ์กันไปยังสรรพากร (IRS) ทางอิเล็กทรอนิกส์ได้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="5f4cb-196">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ให้เลือก **แบบฟอร์ม ACA 1095-B** หรือ **แบบฟอร์ม ACA 1095-C**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="5f4cb-197">เปลี่ยนพารามิเตอร์ตามที่ต้องการ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f4cb-198">ถ้าคุณกำลังพิมพ์ฟอร์ม 1095-C สำหรับพนักงานมากกว่า 500 ราย คุณจะได้รับไฟล์ PDF มากกว่าหนึ่งไฟล์</span><span class="sxs-lookup"><span data-stu-id="5f4cb-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="5f4cb-199">ขอแนะนาว่าคุณควรเพิ่มฟิลด์ **ค่าของขนาดไฟล์สูงสุดเป็นเมกะไบต์** ในหน้า **พารามิเตอร์การจัดการเอกสาร** เป็น **150**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="5f4cb-200">(หากต้องการเปิดหน้าอย่างรวดเร็ว คุณสามารถใช้ฟิลด์การค้นหาบนแถบการนำทางได้)</span><span class="sxs-lookup"><span data-stu-id="5f4cb-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![การเปลี่ยนขนาดไฟล์สูงสุด](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="5f4cb-202">เมื่อต้องการตรวจสอบสถานะของรายงานและดูรายงาน ให้ใช้ฟิลด์การค้นหาบนแถบนําทางเพื่อเปิดหน้า **งานการรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![การค้นหาหน้างานการรายงานทางอิเล็กทรอนิกส์](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="5f4cb-204">เลือกรายงานที่จะดู แล้วเลือก **แสดงไฟล์**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-204">Select the report to view, and then select **Show files**.</span></span>

    ![การแสดงไฟล์](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="5f4cb-206">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-206">Select **Open**.</span></span>

    ![การเปิดไฟล์](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="5f4cb-208">จากแถบการแจ้งเตือนที่ปรากฏที่ด้านล่างของหน้าต่างเบราเซอร์ เปิดไฟล์รหัสไปรษณีย์ แล้วเลือกรายงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="5f4cb-209">คุณสามารถดูหรือพิมพ์ไฟล์ PDF ได้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-209">You can view or print the PDF file.</span></span>

    ![ตัวอย่างแบบฟอร์ม 1095-C](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="5f4cb-211">ดูข้อมูลความคุ้มครอง ACA</span><span class="sxs-lookup"><span data-stu-id="5f4cb-211">View ACA coverage information</span></span>

<span data-ttu-id="5f4cb-212">หน้า **ความคุ้มครอง Affordable Care ของผู้ปฏิบัติงาน** จะแสดงข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="5f4cb-213">พนักงานที่ได้รับมอบหมายให้กลุ่มความคุ้มครองแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="5f4cb-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="5f4cb-214">พนักงานที่ไม่ต้องรวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="5f4cb-215">ยกเลิกการมอบหมายพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-215">Unassigned employees</span></span>

<span data-ttu-id="5f4cb-216">เมื่อต้องการดูข้อมูลนี้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="5f4cb-217">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ให้เลือก **ลุ่มความคุ้มครอง Affordable Care ของผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="5f4cb-218">ในฟิลด์ **ชื่อกลุ่ม** ให้เลือกกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="5f4cb-218">In the **Group name** field, select a group.</span></span>

    ![การดูความคุ้มครอง ACA](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="5f4cb-220">ถ้ามีการแทนที่ค่าเริ่มต้นใด ๆ จากกลุ่มความคุ้มครอง Affordable Care เครื่องหมายดอกจันจะปรากฏขึ้นถัดจากค่าที่ถูกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5f4cb-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="5f4cb-221">ถ้าค่าสำหรับทั้งหมด 12 เดือนเหมือนกัน และไม่ได้ถูกแทนที่ มูลค่าจะปรากฏในคอลัมน์ **ทั้งหมด 12 เดือน**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="5f4cb-222">คุณสามารถดูพนักงานที่มีการเครื่องหมายเป็นไม่รายงาน ACA ได้ และผู้ที่ไม่ต้องการใช้แบบฟอร์ม 1095-C</span><span class="sxs-lookup"><span data-stu-id="5f4cb-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="5f4cb-223">ในฟิลด์ **กรองข้อมูลตาม** ให้เลือก **ไม่สามารถรายงาน ACA**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="5f4cb-224">คุณสามารถดูพนักงานที่ไม่ได้มอบหมายให้กับกลุ่ม หรือผู้ที่ถูกมอบหมายให้กับกลุ่มที่หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="5f4cb-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="5f4cb-225">ในฟิลด์ **กรองข้อมูลตาม** ให้เลือก **กลุ่มที่ไม่ได้กำหนดหรือหมดอายุ**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="5f4cb-226">ส่งออกเป็น Excel</span><span class="sxs-lookup"><span data-stu-id="5f4cb-226">Export to Excel</span></span>

<span data-ttu-id="5f4cb-227">หากต้องการส่งออกรายการใดๆ ให้ Microsoft Excel ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="5f4cb-228">เลือกปุ่ม **เปิดใน Microsoft Office**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="5f4cb-229">เลือก **ตารางชั่วคราวของทรัพยากรบุคคล HCM เพื่อการใช้งานภายใน**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="5f4cb-230">เลือก **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="5f4cb-231">ดูผู้อยู่ในอุปการะที่ต้องรายงานต่อ ACA</span><span class="sxs-lookup"><span data-stu-id="5f4cb-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="5f4cb-232">หากคุณต้องรายงานผู้อยู่ในอุปการะที่ครอบคลุม เนื่องจากคุณให้ความคุ้มครองในการประกันภัยตนเอง คุณสามารถดูผู้อยู่ในอุปการะที่ครอบคลุมภายใต้แผนสวัสดิการ ที่มีการทำเครื่องหมายเป็น **ACA ที่สามารถรายงาน** ได้</span><span class="sxs-lookup"><span data-stu-id="5f4cb-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="5f4cb-233">บนบานหน้าต่างการดำเนินการ เลือก **ดูการคุ้มครองผู้อยู่ในอุปการะ**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![การดูการคุ้มครองผู้อยู่ในอุปการะ](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="5f4cb-235">แสดงข้อมูลการคุ้มครองผู้อยู่ในอุปการะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5f4cb-235">Coverage information for the employee's dependents is shown.</span></span>

![ความคุ้มครองของผู้อยู่ในอุปการะ](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="5f4cb-237">หน้าแสดงเฉพาะแผนสวัสดิการที่ระบุว่า **ACA สามารถรายงาน** ได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5f4cb-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]