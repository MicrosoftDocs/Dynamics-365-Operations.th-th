---
title: กำหนดพารามิเตอร์การจัดการสิทธิประโยชน์
description: ตั้งค่าคอนฟิกพารามิเตอร์สำหรับการจัดการสิทธิประโยชน์ใน Microsoft Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
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
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599367"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="a37ad-103">ตั้งค่าพารามิเตอร์การจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="a37ad-103">Set Benefits management parameters</span></span>

<span data-ttu-id="a37ad-104">ก่อนที่คุณจะสามารถตั้งค่าแผนการลางานใน Microsoft Dynamics 365 Human Resources คุณจำเป็นต้องตั้งค่าคอนฟิกพารามิเตอร์การจัดการสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="a37ad-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="a37ad-105">พารามิเตอร์เหล่านี้จะกำหนดค่าเริ่มต้น รหัสเหตุผล และตัวเลือกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a37ad-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="a37ad-106">ตั้งค่าคอนฟิกพารามิเตอร์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="a37ad-106">Configure general parameters</span></span>

1. <span data-ttu-id="a37ad-107">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ที่ใช้ร่วมกันของทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="a37ad-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="a37ad-108">ในแท็บ **ทั่วไป** ระบุค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a37ad-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="a37ad-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a37ad-109">Field</span></span> | <span data-ttu-id="a37ad-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a37ad-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a37ad-111">**ประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="a37ad-111">**Country/region**</span></span> | <span data-ttu-id="a37ad-112">ฟิลด์ **ประเทศ/ภูมิภาค** จะระบุดลำดับการแสดงผลของรหัสไปรษณีย์/รัฐ</span><span class="sxs-lookup"><span data-stu-id="a37ad-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="a37ad-113">ประเทศที่ถูกเลือกจะแสดงเป็นอันดับแรกในรายการแบบเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="a37ad-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="a37ad-114">**รหัสเหตุผลการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="a37ad-114">**Enrollment reason code**</span></span> | <span data-ttu-id="a37ad-115">การเลือกรหัสเหตุผลเริ่มต้นจะใช้เมื่อมีแผนของพนักงานถูกสร้างขึ้นในระหว่างการประมวลผลการลงทะเบียนที่เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="a37ad-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="a37ad-116">**รหัสเหตุผลการยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="a37ad-116">**Cancellation reason code**</span></span> | <span data-ttu-id="a37ad-117">รหัสเหตุผลจะใช้เมื่อมีการยกเลิกแผนสิทธิประโยชน์พนักงาน</span><span class="sxs-lookup"><span data-stu-id="a37ad-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="a37ad-118">กล่องโต้ตอบจะแสดงขึ้นในระหว่างกระบวนการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a37ad-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="a37ad-119">ผู้ใช้สามารถเปลี่ยน **รหัสเหตุผลการยกเลิก** ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="a37ad-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="a37ad-120">**รหัสเหตุผลการเปิดใหม่**</span><span class="sxs-lookup"><span data-stu-id="a37ad-120">**Reopen reason code**</span></span> | <span data-ttu-id="a37ad-121">รหัสเหตุผลจะใช้เมื่อมีการเปิดใช้แผนสิทธิประโยชน์พนักงานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a37ad-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="a37ad-122">กล่องโต้ตอบจะแสดงขึ้นในระหว่างกระบวนการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a37ad-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="a37ad-123">ผู้ใช้สามารถเปลี่ยน **รหัสเหตุผลการเปิดใช้อีกครั้ง** ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="a37ad-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="a37ad-124">**รหัสเหตุผลเหตุการณ์ของชีวิต**</span><span class="sxs-lookup"><span data-stu-id="a37ad-124">**Life event reason code**</span></span> | <span data-ttu-id="a37ad-125">รหัสเหตุผลจะใช้เมื่อเหตุการณ์ในชีวิตเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a37ad-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="a37ad-126">**รหัสเหตุผลการเปลี่ยนแปลงอัตรา**</span><span class="sxs-lookup"><span data-stu-id="a37ad-126">**Rate change reason code**</span></span> | <span data-ttu-id="a37ad-127">รหัสเหตุผลจะใช้เมื่อมีการยกเลิกและเปิดใช้แผนสิทธิประโยชน์พนักงานอีกครั้งในระหว่างกระบวนการปรับปรุงอัตราการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a37ad-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="a37ad-128">ในส่วนนี้จะบ่งบอกว่ามีการเปลี่ยนแปลงในเรกคอร์ดใดโดยกระบวนการปรับปรุงอัตราการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a37ad-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="a37ad-129">**เงินเดือนสำหรับสวัสดิการต่อปี**</span><span class="sxs-lookup"><span data-stu-id="a37ad-129">**Benefits annual salary**</span></span> | <span data-ttu-id="a37ad-130">ช่วยให้คุณสามารถตั้งค่าจำนวน **เงินเดือนสำหรับสวัสดิการต่อปี** สำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="a37ad-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="a37ad-131">ทรัพยากรบุคคลจะใช้จำนวน **เงินเดือนสำหรับสวัสดิการต่อปี** เมื่อกำหนดจำนวนเงินที่ครอบคลุม แทนที่จำนวนค่าตอบแทนคงที่แบบรายปี</span><span class="sxs-lookup"><span data-stu-id="a37ad-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="a37ad-132">**พนักงานใหม่ที่มีสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="a37ad-132">**New hire eligible**</span></span> | <span data-ttu-id="a37ad-133">ระบุว่าการจ้างงานใหม่สามารถทำได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a37ad-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="a37ad-134">**รอบระยะเวลาการลงทะเบียนของพนักงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="a37ad-134">**New hire enrollment period**</span></span> | <span data-ttu-id="a37ad-135">รอบระยะเวลาของเวลาที่อนุญาตให้มีการลงทะเบียนการจ้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="a37ad-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="a37ad-136">**หมายเหตุ** การตั้งค่านี้จะแทนที่รอบระยะเวลาการลงทะเบียนการจ้างงานใหม่ใดๆ ที่คุณกำหนดไว้ในแผนของกฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a37ad-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="a37ad-137">**ความถี่การชำระเงินเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="a37ad-137">**Default pay frequency**</span></span> | <span data-ttu-id="a37ad-138">ความถี่ในการชำระค่าจ้างเริ่มต้นที่จะใช้ เมื่อมีการเพิ่มผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="a37ad-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="a37ad-139">**เปิดใช้งานเหตุการณ์ของชีวิตแล้ว**</span><span class="sxs-lookup"><span data-stu-id="a37ad-139">**Life events enabled**</span></span> | <span data-ttu-id="a37ad-140">เปิดใช้งานเหตุการณ์ในชีวิต</span><span class="sxs-lookup"><span data-stu-id="a37ad-140">Enables life events.</span></span> |
   | <span data-ttu-id="a37ad-141">**ซ่อนฟอร์มสวัสดิการมรดก**</span><span class="sxs-lookup"><span data-stu-id="a37ad-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="a37ad-142">อนุญาตให้คุณซ่อนแบบฟอร์มสิทธิประโยชน์แบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="a37ad-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="a37ad-143">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a37ad-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="a37ad-144">การตั้งค่าคอนฟิกพารามิเตอร์การบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="a37ad-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="a37ad-145">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="a37ad-145">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="a37ad-146">ในแท็บ **การบริการตนเองของพนักงาน** ให้ระบุค่าในฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a37ad-146">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="a37ad-147">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a37ad-147">Field</span></span> | <span data-ttu-id="a37ad-148">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a37ad-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a37ad-149">**การตรวจสอบสิทธิประโยชน์**</span><span class="sxs-lookup"><span data-stu-id="a37ad-149">**Benefit verification**</span></span> | <span data-ttu-id="a37ad-150">ข้อความที่ใช้ตรวจสอบจะใช้ระหว่างการเช็คเอาท์ผลประโยชน์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a37ad-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="a37ad-151">**เลือกผู้ถูกกำหนดอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="a37ad-151">**Auto select designees**</span></span> | <span data-ttu-id="a37ad-152">ระบุว่าจะเลือกผู้อยู่ในอุปการะและผู้รับผลประโยชน์โดยอัตโนมัติตามสิทธิ์ของตนสำหรับตัวเลือกแผนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a37ad-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="a37ad-153">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a37ad-153">Select **Save**.</span></span>
