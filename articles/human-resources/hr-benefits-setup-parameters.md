---
title: กำหนดพารามิเตอร์การจัดการสิทธิประโยชน์
description: ตั้งค่าคอนฟิกพารามิเตอร์สำหรับการจัดการสิทธิประโยชน์ใน Microsoft Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229774"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="a43e5-103">ตั้งค่าพารามิเตอร์การจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="a43e5-103">Set Benefits management parameters</span></span>

<span data-ttu-id="a43e5-104">ก่อนที่คุณจะสามารถตั้งค่าแผนการลางานใน Microsoft Dynamics 365 Human Resources คุณจำเป็นต้องตั้งค่าคอนฟิกพารามิเตอร์การจัดการสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="a43e5-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="a43e5-105">พารามิเตอร์เหล่านี้จะกำหนดค่าเริ่มต้น รหัสเหตุผล และตัวเลือกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a43e5-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="a43e5-106">ตั้งค่าคอนฟิกพารามิเตอร์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="a43e5-106">Configure general parameters</span></span>

1. <span data-ttu-id="a43e5-107">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="a43e5-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="a43e5-108">ในแท็บ **ทั่วไป** ระบุค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a43e5-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="a43e5-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a43e5-109">Field</span></span> | <span data-ttu-id="a43e5-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a43e5-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a43e5-111">**ประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="a43e5-111">**Country/region**</span></span> | <span data-ttu-id="a43e5-112">ฟิลด์ **ประเทศ/ภูมิภาค** จะระบุดลำดับการแสดงผลของรหัสไปรษณีย์/รัฐ</span><span class="sxs-lookup"><span data-stu-id="a43e5-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="a43e5-113">ประเทศที่ถูกเลือกจะแสดงเป็นอันดับแรกในรายการแบบเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="a43e5-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="a43e5-114">**รหัสเหตุผลการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="a43e5-114">**Enrollment reason code**</span></span> | <span data-ttu-id="a43e5-115">การเลือกรหัสเหตุผลเริ่มต้นจะใช้เมื่อมีแผนของพนักงานถูกสร้างขึ้นในระหว่างการประมวลผลการลงทะเบียนที่เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="a43e5-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="a43e5-116">**รหัสเหตุผลการยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="a43e5-116">**Cancellation reason code**</span></span> | <span data-ttu-id="a43e5-117">รหัสเหตุผลจะใช้เมื่อมีการยกเลิกแผนสิทธิประโยชน์พนักงาน</span><span class="sxs-lookup"><span data-stu-id="a43e5-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="a43e5-118">กล่องโต้ตอบจะแสดงขึ้นในระหว่างกระบวนการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a43e5-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="a43e5-119">ผู้ใช้สามารถเปลี่ยน **รหัสเหตุผลการยกเลิก** ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="a43e5-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="a43e5-120">**รหัสเหตุผลการเปิดใหม่**</span><span class="sxs-lookup"><span data-stu-id="a43e5-120">**Reopen reason code**</span></span> | <span data-ttu-id="a43e5-121">รหัสเหตุผลจะใช้เมื่อมีการเปิดใช้แผนสิทธิประโยชน์พนักงานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a43e5-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="a43e5-122">กล่องโต้ตอบจะแสดงขึ้นในระหว่างกระบวนการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a43e5-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="a43e5-123">ผู้ใช้สามารถเปลี่ยน **รหัสเหตุผลการเปิดใช้อีกครั้ง** ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="a43e5-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="a43e5-124">**รหัสเหตุผลเหตุการณ์ของชีวิต**</span><span class="sxs-lookup"><span data-stu-id="a43e5-124">**Life event reason code**</span></span> | <span data-ttu-id="a43e5-125">รหัสเหตุผลจะใช้เมื่อเหตุการณ์ในชีวิตเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a43e5-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="a43e5-126">**รหัสเหตุผลการเปลี่ยนแปลงอัตรา**</span><span class="sxs-lookup"><span data-stu-id="a43e5-126">**Rate change reason code**</span></span> | <span data-ttu-id="a43e5-127">รหัสเหตุผลจะใช้เมื่อมีการยกเลิกและเปิดใช้แผนสิทธิประโยชน์พนักงานอีกครั้งในระหว่างกระบวนการปรับปรุงอัตราการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a43e5-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="a43e5-128">ในส่วนนี้จะบ่งบอกว่ามีการเปลี่ยนแปลงในเรกคอร์ดใดโดยกระบวนการปรับปรุงอัตราการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a43e5-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="a43e5-129">**พนักงานใหม่ที่มีสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="a43e5-129">**New hire eligible**</span></span> | <span data-ttu-id="a43e5-130">ระบุว่าการจ้างงานใหม่สามารถทำได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a43e5-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="a43e5-131">**รอบระยะเวลาการลงทะเบียนของพนักงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="a43e5-131">**New hire enrollment period**</span></span> | <span data-ttu-id="a43e5-132">รอบระยะเวลาของเวลาที่อนุญาตให้มีการลงทะเบียนการจ้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="a43e5-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="a43e5-133">**หมายเหตุ** การตั้งค่านี้จะแทนที่รอบระยะเวลาการลงทะเบียนการจ้างงานใหม่ใดๆ ที่คุณกำหนดไว้ในแผนของกฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a43e5-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="a43e5-134">**เปิดใช้งานเหตุการณ์ของชีวิตแล้ว**</span><span class="sxs-lookup"><span data-stu-id="a43e5-134">**Life events enabled**</span></span> | <span data-ttu-id="a43e5-135">เปิดใช้งานเหตุการณ์ในชีวิต</span><span class="sxs-lookup"><span data-stu-id="a43e5-135">Enables life events.</span></span> |
   | <span data-ttu-id="a43e5-136">**ซ่อนฟอร์มสวัสดิการมรดก**</span><span class="sxs-lookup"><span data-stu-id="a43e5-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="a43e5-137">อนุญาตให้คุณซ่อนแบบฟอร์มสิทธิประโยชน์แบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="a43e5-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="a43e5-138">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a43e5-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="a43e5-139">การตั้งค่าคอนฟิกพารามิเตอร์การบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="a43e5-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="a43e5-140">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="a43e5-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="a43e5-141">ในแท็บ **การบริการตนเองของพนักงาน** ให้ระบุค่าในฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a43e5-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="a43e5-142">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a43e5-142">Field</span></span> | <span data-ttu-id="a43e5-143">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a43e5-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a43e5-144">**การตรวจสอบสิทธิประโยชน์**</span><span class="sxs-lookup"><span data-stu-id="a43e5-144">**Benefit verification**</span></span> | <span data-ttu-id="a43e5-145">ข้อความที่ใช้ตรวจสอบจะใช้ระหว่างการเช็คเอาท์ผลประโยชน์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a43e5-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="a43e5-146">**เลือกผู้ถูกกำหนดอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="a43e5-146">**Auto select designees**</span></span> | <span data-ttu-id="a43e5-147">ระบุว่าจะเลือกผู้อยู่ในอุปการะและผู้รับผลประโยชน์โดยอัตโนมัติตามสิทธิ์ของตนสำหรับตัวเลือกแผนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a43e5-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="a43e5-148">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a43e5-148">Select **Save**.</span></span>
