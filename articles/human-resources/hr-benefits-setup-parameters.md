---
title: ตั้งค่าพารามิเตอร์การจัดการสวัสดิการและการบริการตนเองของพนักงานสำหรับบริษัททั้งหมด
description: ตั้งค่าคอนฟิกพารามิเตอร์สำหรับการจัดการสวัสดิการและการบริการตนเองของพนักงานใน Microsoft Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: 5e241475c9652ab2dafe6886479e9c0a93711aca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466771"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="5a748-103">ตั้งค่าพารามิเตอร์การจัดการสวัสดิการและการบริการตนเองของพนักงานสำหรับบริษัททั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5a748-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5a748-104">ก่อนที่คุณจะสามารถตั้งค่าแผนสวัสดิการใน Microsoft Dynamics 365 Human Resources คุณจำเป็นต้องตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5a748-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="5a748-105">พารามิเตอร์เหล่านี้จะกำหนดค่าเริ่มต้น รหัสเหตุผล และตัวเลือกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5a748-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="5a748-106">ตั้งค่าคอนฟิกพารามิเตอร์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="5a748-106">Configure general parameters</span></span>

1. <span data-ttu-id="5a748-107">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ที่ใช้ร่วมกันของทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="5a748-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="5a748-108">ในแท็บ **การจัดการสวัสดิการ** ระบุค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5a748-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="5a748-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5a748-109">Field</span></span> | <span data-ttu-id="5a748-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5a748-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5a748-111">**ประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="5a748-111">**Country/region**</span></span> | <span data-ttu-id="5a748-112">ฟิลด์ **ประเทศ/ภูมิภาค** จะระบุดลำดับการแสดงผลของรหัสไปรษณีย์/รัฐ</span><span class="sxs-lookup"><span data-stu-id="5a748-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="5a748-113">ประเทศที่ถูกเลือกจะแสดงเป็นอันดับแรกในรายการแบบเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="5a748-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="5a748-114">**รหัสเหตุผลการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="5a748-114">**Enrollment reason code**</span></span> | <span data-ttu-id="5a748-115">การเลือกรหัสเหตุผลเริ่มต้นจะใช้เมื่อมีแผนของพนักงานถูกสร้างขึ้นในระหว่างการประมวลผลการลงทะเบียนที่เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="5a748-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="5a748-116">**รหัสเหตุผลการยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="5a748-116">**Cancellation reason code**</span></span> | <span data-ttu-id="5a748-117">รหัสเหตุผลจะใช้เมื่อมีการยกเลิกแผนสิทธิประโยชน์พนักงาน</span><span class="sxs-lookup"><span data-stu-id="5a748-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="5a748-118">กล่องโต้ตอบจะแสดงขึ้นในระหว่างกระบวนการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="5a748-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="5a748-119">ผู้ใช้สามารถเปลี่ยน **รหัสเหตุผลการยกเลิก** ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="5a748-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="5a748-120">**รหัสเหตุผลการเปิดใหม่**</span><span class="sxs-lookup"><span data-stu-id="5a748-120">**Reopen reason code**</span></span> | <span data-ttu-id="5a748-121">รหัสเหตุผลจะใช้เมื่อมีการเปิดใช้แผนสิทธิประโยชน์พนักงานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="5a748-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="5a748-122">กล่องโต้ตอบจะแสดงขึ้นในระหว่างกระบวนการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="5a748-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="5a748-123">ผู้ใช้สามารถเปลี่ยน **รหัสเหตุผลการเปิดใช้อีกครั้ง** ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="5a748-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="5a748-124">**รหัสเหตุผลเหตุการณ์ของชีวิต**</span><span class="sxs-lookup"><span data-stu-id="5a748-124">**Life event reason code**</span></span> | <span data-ttu-id="5a748-125">รหัสเหตุผลจะใช้เมื่อเหตุการณ์ในชีวิตเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="5a748-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="5a748-126">**รหัสเหตุผลการเปลี่ยนแปลงอัตรา**</span><span class="sxs-lookup"><span data-stu-id="5a748-126">**Rate change reason code**</span></span> | <span data-ttu-id="5a748-127">รหัสเหตุผลจะใช้เมื่อมีการยกเลิกและเปิดใช้แผนสิทธิประโยชน์พนักงานอีกครั้งในระหว่างกระบวนการปรับปรุงอัตราการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5a748-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="5a748-128">ในส่วนนี้จะบ่งบอกว่ามีการเปลี่ยนแปลงในเรกคอร์ดใดโดยกระบวนการปรับปรุงอัตราการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5a748-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="5a748-129">**เงินเดือนสำหรับสวัสดิการต่อปี**</span><span class="sxs-lookup"><span data-stu-id="5a748-129">**Benefits annual salary**</span></span> | <span data-ttu-id="5a748-130">ช่วยให้คุณสามารถตั้งค่าจำนวน **เงินเดือนสำหรับสวัสดิการต่อปี** สำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5a748-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="5a748-131">ทรัพยากรบุคคลจะใช้จำนวน **เงินเดือนสำหรับสวัสดิการต่อปี** เมื่อกำหนดจำนวนเงินที่ครอบคลุม แทนที่จำนวนค่าตอบแทนคงที่แบบรายปี</span><span class="sxs-lookup"><span data-stu-id="5a748-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="5a748-132">**พนักงานใหม่ที่มีสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="5a748-132">**New hire eligible**</span></span> | <span data-ttu-id="5a748-133">ระบุว่าการจ้างงานใหม่สามารถทำได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5a748-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="5a748-134">**รอบระยะเวลาการลงทะเบียนของพนักงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="5a748-134">**New hire enrollment period**</span></span> | <span data-ttu-id="5a748-135">รอบระยะเวลาของเวลาที่อนุญาตให้มีการลงทะเบียนการจ้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="5a748-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="5a748-136">**หมายเหตุ** การตั้งค่านี้จะแทนที่รอบระยะเวลาการลงทะเบียนการจ้างงานใหม่ใดๆ ที่คุณกำหนดไว้ในแผนของกฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="5a748-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="5a748-137">**ความถี่การชำระเงินเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="5a748-137">**Default pay frequency**</span></span> | <span data-ttu-id="5a748-138">ความถี่ในการชำระค่าจ้างเริ่มต้นที่จะใช้ เมื่อมีการเพิ่มผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="5a748-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="5a748-139">**เปิดใช้งานเหตุการณ์ของชีวิตแล้ว**</span><span class="sxs-lookup"><span data-stu-id="5a748-139">**Life events enabled**</span></span> | <span data-ttu-id="5a748-140">เปิดใช้งานเหตุการณ์ในชีวิต</span><span class="sxs-lookup"><span data-stu-id="5a748-140">Enables life events.</span></span> |
   | <span data-ttu-id="5a748-141">**ซ่อนฟอร์มสวัสดิการมรดก**</span><span class="sxs-lookup"><span data-stu-id="5a748-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="5a748-142">อนุญาตให้คุณซ่อนแบบฟอร์มสิทธิประโยชน์แบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="5a748-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="5a748-143">**การตรวจสอบสิทธิประโยชน์**</span><span class="sxs-lookup"><span data-stu-id="5a748-143">**Benefit verification**</span></span> | <span data-ttu-id="5a748-144">ข้อความที่ใช้ตรวจสอบจะใช้ระหว่างการเช็คเอาท์ผลประโยชน์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="5a748-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="5a748-145">**เลือกผู้ถูกกำหนดอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="5a748-145">**Auto select designees**</span></span> | <span data-ttu-id="5a748-146">ระบุว่าจะเลือกผู้อยู่ในอุปการะและผู้รับผลประโยชน์โดยอัตโนมัติตามสิทธิ์ของตนสำหรับตัวเลือกแผนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5a748-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="5a748-147">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5a748-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="5a748-148">ตั้งค่าคอนฟิกพารามิเตอร์การบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5a748-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="5a748-149">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="5a748-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="5a748-150">ในแท็บ **การจัดการสวัสดิการ** ระบุค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5a748-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="5a748-151">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5a748-151">Field</span></span> | <span data-ttu-id="5a748-152">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5a748-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5a748-153">**การตรวจสอบสิทธิประโยชน์**</span><span class="sxs-lookup"><span data-stu-id="5a748-153">**Benefit verification**</span></span> | <span data-ttu-id="5a748-154">ข้อความที่ใช้ตรวจสอบจะใช้ระหว่างการเช็คเอาท์ผลประโยชน์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="5a748-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="5a748-155">**เลือกผู้ถูกกำหนดอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="5a748-155">**Auto select designees**</span></span> | <span data-ttu-id="5a748-156">ระบุว่าจะเลือกผู้อยู่ในอุปการะและผู้รับผลประโยชน์โดยอัตโนมัติตามสิทธิ์ของตนสำหรับตัวเลือกแผนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5a748-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="5a748-157">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5a748-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]