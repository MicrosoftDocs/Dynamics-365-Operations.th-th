---
title: กำหนดพารามิเตอร์การจัดการสิทธิประโยชน์
description: ตั้งค่าคอนฟิกพารามิเตอร์สำหรับการจัดการสิทธิประโยชน์ใน Microsoft Dynamics 365 Human Resources
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010739"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="16e05-103">กำหนดพารามิเตอร์การจัดการสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="16e05-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="16e05-104">ก่อนที่คุณจะสามารถตั้งค่าการออกจากแผนใน Microsoft Dynamics 365 Human Resources คุณจำเป็นต้องตั้งค่าคอนฟิกพารามิเตอร์การจัดการสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="16e05-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="16e05-105">พารามิเตอร์เหล่านี้จะกำหนดค่าเริ่มต้น รหัสเหตุผล และตัวเลือกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="16e05-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="16e05-106">ตั้งค่าคอนฟิกพารามิเตอร์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="16e05-106">Configure general parameters</span></span>

1. <span data-ttu-id="16e05-107">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="16e05-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="16e05-108">ในแท็บ **ทั่วไป** ระบุค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="16e05-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="16e05-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="16e05-109">Field</span></span> | <span data-ttu-id="16e05-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="16e05-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="16e05-111">**ประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="16e05-111">**Country/region**</span></span> | <span data-ttu-id="16e05-112">ฟิลด์ **ประเทศ/ภูมิภาค** จะระบุดลำดับการแสดงผลของรหัสไปรษณีย์/รัฐ</span><span class="sxs-lookup"><span data-stu-id="16e05-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="16e05-113">ประเทศที่ถูกเลือกจะแสดงเป็นอันดับแรกในรายการแบบเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="16e05-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="16e05-114">**รหัสเหตุผลการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="16e05-114">**Enrollment reason code**</span></span> | <span data-ttu-id="16e05-115">การเลือกรหัสเหตุผลเริ่มต้นจะใช้เมื่อมีแผนของพนักงานถูกสร้างขึ้นในระหว่างการประมวลผลการลงทะเบียนที่เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="16e05-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="16e05-116">**รหัสเหตุผลการยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="16e05-116">**Cancellation reason code**</span></span> | <span data-ttu-id="16e05-117">รหัสเหตุผลจะใช้เมื่อมีการยกเลิกแผนสิทธิประโยชน์พนักงาน</span><span class="sxs-lookup"><span data-stu-id="16e05-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="16e05-118">กล่องโต้ตอบจะแสดงขึ้นในระหว่างกระบวนการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="16e05-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="16e05-119">ผู้ใช้สามารถเปลี่ยน **รหัสเหตุผลการยกเลิก** ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="16e05-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="16e05-120">**รหัสเหตุผลการเปิดใหม่**</span><span class="sxs-lookup"><span data-stu-id="16e05-120">**Reopen reason code**</span></span> | <span data-ttu-id="16e05-121">รหัสเหตุผลจะใช้เมื่อมีการเปิดใช้แผนสิทธิประโยชน์พนักงานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="16e05-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="16e05-122">กล่องโต้ตอบจะแสดงขึ้นในระหว่างกระบวนการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="16e05-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="16e05-123">ผู้ใช้สามารถเปลี่ยน **รหัสเหตุผลการเปิดใช้อีกครั้ง** ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="16e05-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="16e05-124">**รหัสเหตุผลเหตุการณ์ของชีวิต**</span><span class="sxs-lookup"><span data-stu-id="16e05-124">**Life event reason code**</span></span> | <span data-ttu-id="16e05-125">รหัสเหตุผลจะใช้เมื่อเหตุการณ์ในชีวิตเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="16e05-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="16e05-126">**รหัสเหตุผลการเปลี่ยนแปลงอัตรา**</span><span class="sxs-lookup"><span data-stu-id="16e05-126">**Rate change reason code**</span></span> | <span data-ttu-id="16e05-127">รหัสเหตุผลจะใช้เมื่อมีการยกเลิกและเปิดใช้แผนสิทธิประโยชน์พนักงานอีกครั้งในระหว่างกระบวนการปรับปรุงอัตราการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="16e05-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="16e05-128">ในส่วนนี้จะบ่งบอกว่ามีการเปลี่ยนแปลงในเรกคอร์ดใดโดยกระบวนการปรับปรุงอัตราการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="16e05-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="16e05-129">**พนักงานใหม่ที่มีสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="16e05-129">**New hire eligible**</span></span> | <span data-ttu-id="16e05-130">ระบุว่าการจ้างงานใหม่สามารถทำได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="16e05-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="16e05-131">**รอบระยะเวลาการลงทะเบียนของพนักงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="16e05-131">**New hire enrollment period**</span></span> | <span data-ttu-id="16e05-132">รอบระยะเวลาของเวลาที่อนุญาตให้มีการลงทะเบียนการจ้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="16e05-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="16e05-133">**หมายเหตุ** การตั้งค่านี้จะแทนที่รอบระยะเวลาการลงทะเบียนการจ้างงานใหม่ใดๆ ที่คุณกำหนดไว้ในแผนของกฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="16e05-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="16e05-134">**การปรับเงินเดือนประจำปี**</span><span class="sxs-lookup"><span data-stu-id="16e05-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="16e05-135">ระบุว่าจะคำนวณยอดเงินของ **สิทธิประโยชน์ของรายได้ประจำปี** ใน **รายละเอียดสิทธิประโยชน์สำหรับการจ้างงาน** โดยอัตโนมัติหรือไม่</span><span class="sxs-lookup"><span data-stu-id="16e05-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="16e05-136">ขึ้นอยู่กับ **อัตราค่าจ้างคงที่ของพนักงาน** **ค่าจ้างเฉลี่ยต่อชั่วโมง** และ **ความถี่ในการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="16e05-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="16e05-137">**ชั่วโมงเฉลี่ย** x **อัตราค่าจ้างคงที่** x **ความถี่ในการชำระเงิน** (# ของรอบระยะเวลาการชำระค่าจ้าง) = **สิทธิประโยชน์ของรายได้ประจำปี**</span><span class="sxs-lookup"><span data-stu-id="16e05-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="16e05-138">ถ้าค่าใดค่าหนึ่งในฟิลด์ **ชั่วโมงเฉลี่ย** **อัตราการจ่ายค่าจ้างคงที่** หรือ **ความถี่ในการชำระเงิน** มีการเปลี่ยนแปลง ระบบจะคำนวณยอด **สิทธิประโยชน์ของรายได้ประจำปี** ของพนักงานให้ใหม่โดยอัตโนมัติตามค่าที่เปลี่ยนไป</span><span class="sxs-lookup"><span data-stu-id="16e05-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="16e05-139">ระบบจะสร้างเรกคอร์ด **วันที่มีผลบังคับใช้** เพื่อระบุวันที่และเวลาที่มีการเปลี่ยนแปลงที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="16e05-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="16e05-140">คุณสามารถแก้ไขยอดเงิน **สิทธิประโยชน์ของรายได้ประจำปี** ด้วยตนเองได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="16e05-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="16e05-141">**เปิดใช้งานเหตุการณ์ของชีวิตแล้ว**</span><span class="sxs-lookup"><span data-stu-id="16e05-141">**Life events enabled**</span></span> | <span data-ttu-id="16e05-142">เปิดใช้งานเหตุการณ์ในชีวิต</span><span class="sxs-lookup"><span data-stu-id="16e05-142">Enables life events.</span></span> |
   | <span data-ttu-id="16e05-143">**ซ่อนฟอร์มสวัสดิการมรดก**</span><span class="sxs-lookup"><span data-stu-id="16e05-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="16e05-144">อนุญาตให้คุณซ่อนแบบฟอร์มสิทธิประโยชน์แบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="16e05-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="16e05-145">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="16e05-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="16e05-146">การตั้งค่าคอนฟิกพารามิเตอร์การบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="16e05-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="16e05-147">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="16e05-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="16e05-148">ในแท็บ **การบริการตนเองของพนักงาน** ให้ระบุค่าในฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="16e05-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="16e05-149">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="16e05-149">Field</span></span> | <span data-ttu-id="16e05-150">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="16e05-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="16e05-151">**การตรวจสอบสิทธิประโยชน์**</span><span class="sxs-lookup"><span data-stu-id="16e05-151">**Benefit verification**</span></span> | <span data-ttu-id="16e05-152">ข้อความที่ใช้ตรวจสอบจะใช้ระหว่างการเช็คเอาท์ผลประโยชน์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="16e05-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="16e05-153">**เลือกผู้ถูกกำหนดอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="16e05-153">**Auto select designees**</span></span> | <span data-ttu-id="16e05-154">ระบุว่าจะเลือกผู้อยู่ในอุปการะและผู้รับผลประโยชน์โดยอัตโนมัติตามสิทธิ์ของตนสำหรับตัวเลือกแผนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="16e05-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="16e05-155">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="16e05-155">Select **Save**.</span></span>
