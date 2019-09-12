---
title: การจัดการข้อบกพร่อง
description: หัวข้อนี้จะอธิบายถึงการวิเคราะห์การจัดการข้อบกพร่องของสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 48c90a8b776cc16804de8e20ada7d8ca347fa5b9
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874750"
---
# <a name="fault-management"></a><span data-ttu-id="c5c89-103">การจัดการข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c5c89-104">ในการจัดการสินทรัพย์ คุณสามารถใช้โปรแกรมออกแบบข้อบกพร่องเพื่อตั้งค่าอาการข้อบกพร่อง พื้นที่ข้อบกพร่อง และชนิดข้อบกพร่องในชนิดสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="c5c89-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="c5c89-105">ด้วยวิธีนี้ คุณสามารถจัดการข้อบกพร่องที่ตรวจพบในสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="c5c89-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="c5c89-106">นอกจากนี้ สาเหตุของข้อบกพร่อง เเละคำเเนะนำสำหรับการเเก้ไขข้อบกพร่องสามารถลงทะเบียนได้ในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="c5c89-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="c5c89-107">กระบวนการสำหรับการลงทะเบียนข้อบกพร่อง และการจัดการประกอบด้วยขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c5c89-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="c5c89-108">สร้างรายการของอาการข้อบกพร่อง พื้นที่ข้อบกพร่อง เเละชนิดข้อบกพร่องที่อาจเกิดขึ้นบนชนิดสินทรัพย์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c5c89-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="c5c89-109">ในโปรแกรมออกแบบข้อบกพร่อง ตั้งค่าอาการ พื้นที่ข้อบกพร่อง และชนิดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="c5c89-110">ต่อไปนี้เป็นตัวอย่างที่ช่วยให้คุณเข้าใจความแตกต่างระหว่างอาการข้อบกพร่อง พื้นที่ข้อบกพร่อง และชนิดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="c5c89-111">**อาการข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="c5c89-112">แรงดันไฟฟ้าที่ไม่สมดุล</span><span class="sxs-lookup"><span data-stu-id="c5c89-112">Unbalanced voltages</span></span>
- <span data-ttu-id="c5c89-113">ลัดวงจร</span><span class="sxs-lookup"><span data-stu-id="c5c89-113">Short circuit</span></span>
- <span data-ttu-id="c5c89-114">เสียง</span><span class="sxs-lookup"><span data-stu-id="c5c89-114">Noise</span></span>
- <span data-ttu-id="c5c89-115">รั่ว</span><span class="sxs-lookup"><span data-stu-id="c5c89-115">Leak</span></span>
- <span data-ttu-id="c5c89-116">การสั่นสะเทือน</span><span class="sxs-lookup"><span data-stu-id="c5c89-116">Vibrations</span></span>

<span data-ttu-id="c5c89-117">**พื้นที่ข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-117">**Fault areas:**</span></span>

- <span data-ttu-id="c5c89-118">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c5c89-118">Electrical</span></span>
- <span data-ttu-id="c5c89-119">เชิงกล</span><span class="sxs-lookup"><span data-stu-id="c5c89-119">Mechanical</span></span>
- <span data-ttu-id="c5c89-120">ไฮดรอลิก</span><span class="sxs-lookup"><span data-stu-id="c5c89-120">Hydraulic</span></span>
- <span data-ttu-id="c5c89-121">นิวเมติก</span><span class="sxs-lookup"><span data-stu-id="c5c89-121">Pneumatic</span></span>

<span data-ttu-id="c5c89-122">**ชนิดข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-122">**Fault types:**</span></span>

- <span data-ttu-id="c5c89-123">สเตเตอร์หลักผิดพลาดในการหมุน</span><span class="sxs-lookup"><span data-stu-id="c5c89-123">Faulty main stator winding</span></span>
- <span data-ttu-id="c5c89-124">ไดโอดผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="c5c89-124">Faulty diode</span></span>
- <span data-ttu-id="c5c89-125">ขดลวดสกปรก</span><span class="sxs-lookup"><span data-stu-id="c5c89-125">Dirty windings</span></span>
- <span data-ttu-id="c5c89-126">ตัวสร้างที่บกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-126">Defective generator</span></span>
- <span data-ttu-id="c5c89-127">เซ็นเซอร์ที่บกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="c5c89-128">สร้างอาการข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-128">Create fault symptoms</span></span>

<span data-ttu-id="c5c89-129">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างรายการของอาการที่สามารถใช้ในโปรแกรมออกแบบข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="c5c89-130">เลือก **การจัดการสินทรัพย์** \> **ตั้งต่า** \> **ข้อบกพร่อง** \> **อาการข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="c5c89-131">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c5c89-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c5c89-132">ในฟิล์ด **อาการข้อบกพร่อง** ป้อนชื่อสำหรับอาการข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="c5c89-133">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c5c89-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c5c89-134">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c5c89-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="c5c89-135">สร้างพื้นที่ข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-135">Create fault areas</span></span>

<span data-ttu-id="c5c89-136">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างรายการของอาการ หรือสถานที่ที่สามารถใช้ในโปรแกรมออกแบบข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="c5c89-137">เลือก **การจัดการสินทรัพย์** \> **ตั้งต่า** \> **ข้อบกพร่อง** \> **พื้นที่ข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="c5c89-138">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c5c89-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c5c89-139">ในฟิล์ด **พื้นที่ข้อบกพร่อง** ป้อนชื่อสำหรับพื้นที่ข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="c5c89-140">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c5c89-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c5c89-141">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c5c89-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="c5c89-142">สร้างชนิดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-142">Create fault types</span></span>

<span data-ttu-id="c5c89-143">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างรายการชนิดข้อบกพร่องที่สามารถใช้ในโปรแกรมออกแบบข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="c5c89-144">เลือก **การจัดการสินทรัพย์** \> **ตั้งต่า** \> **ข้อบกพร่อง** \> **ชนิดข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="c5c89-145">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c5c89-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c5c89-146">ในฟิลด์ **ชนิดข้อบกพร่อง** ให้ป้อนชื่อสำหรับชนิดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="c5c89-147">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c5c89-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c5c89-148">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c5c89-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="c5c89-149">ตั้งค่าโปรเเกรมออกแบบข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-149">Set up the fault designer</span></span>

<span data-ttu-id="c5c89-150">ในโปรแกรมออกแบบข้อบกพร่อง คุณตั้งค่าข้อมูลบกพร่องบนชนิดสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="c5c89-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="c5c89-151">เลือก **การจัดการสินทรัพย์** \> **ตั้งต่า** \> **ข้อบกพร่อง** \> **โปรเเกรมออกเเบบข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="c5c89-152">ในบานหน้าต่างด้านซ้าย เลือกชนิดของสินทรัพย์เพื่อตั้งค่าเรกคอร์ดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="c5c89-153">บนแท็บด่วน **อาการข้อบกพร่อง** เลือก **เพิ่มรายการ** เเละจากนั่น ในฟิล์ด **อาการข้อบกพร่อง** เลือกอาการข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="c5c89-154">บนแท็บด่วน **พื้นที่ข้อบกพร่อง** เลือก **เพิ่มรายการ** เเละจากนั่น ในฟิล์ด **พื้นที่ข้อบกพร่อง** เลือกพื้นที่ข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="c5c89-155">บนแท็บด่วน **ชนิดข้อบกพร่อง** เลือก **เพิ่มรายการ** เเละจากนั่น ในฟิล์ด **ชนิดข้อบกพร่อง** เลือกชนิดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="c5c89-156">เมื่อต้องการสร้างชุดของอาการข้อบกพร่อง พื้นที่ และชนิดอย่างรวดเร็วสำหรับการเลือกชนิดสินทรัพย์ เลือก **สร้างชุดข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="c5c89-157">ฟังก์ชันนี้มีประโยชน์ถ้าคุณเพิ่มอาการข้อบกพร่อง พื้นที่ และชนิดต่างๆหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c5c89-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="c5c89-158">เป็นการง่ายที่จะลบรายการสำหรับชุดใดๆที่ไม่เกี่ยวข้องกับชนิดสินทรัพย์กว่าการสร้างรายการใหม่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c5c89-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c5c89-159">เมื่อต้องการคัดลอกการตั้งค่าของอาการข้อบกพร่อง พื้นที่ และชนิดจากสินทรัพย์ชนิดหนึ่งไปยังชนิดสินทรัพย์ที่่เลือก เลือก **คัดลอกจากชนิดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="c5c89-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="c5c89-160">เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="c5c89-160">Select **Save** to save your changes.</span></span>

![รูปที่ 1](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="c5c89-162">สร้างสาเหตุข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-162">Create fault causes</span></span>

<span data-ttu-id="c5c89-163">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างรายการของสาเหตุข้อบกพร่องที่ทราบซึ่งสามารถเพิ่มเข้าไปในใบสั่งงาน หรือคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c5c89-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="c5c89-164">เลือก **การจัดการสินทรัพย์** \> **ตั้งต่า** \> **ข้อบกพร่อง** \> **สาเหตุข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="c5c89-165">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c5c89-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c5c89-166">ในฟิลด์ **สาเหตุข้อบกพร่อง** ให้ป้อนชื่อสำหรับสาเหตุข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="c5c89-167">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c5c89-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c5c89-168">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c5c89-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="c5c89-169">สร้างการเเก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="c5c89-169">Create fault remedies</span></span>

<span data-ttu-id="c5c89-170">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างรายการของคำเเนะนำสำหรับการเเก้ไข เเละซ่อมเเซมซึ่งสามารถเพิ่มเข้าไปในใบสั่งงาน หรือคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c5c89-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="c5c89-171">เลือก **การจัดการสินทรัพย์** \> **ตั้งต่า** \> **ข้อบกพร่อง** \> **การเเก้ไขข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="c5c89-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="c5c89-172">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c5c89-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c5c89-173">ในฟิล์ด **การแก้ไขข้อบกพร่อง** ป้อนชื่อสำหรับการแก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="c5c89-174">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c5c89-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c5c89-175">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c5c89-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="c5c89-176">คุณสามารถเปลี่ยนชื่อของอาการข้อผิดพลาด พื้นที่ ชนิด สาเหตุ และการเเก้ไขของคุณตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="c5c89-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="c5c89-177">การเปลี่ยนแปลงชื่อจะสะท้อนให้เห็นโดยอัตโนมัติในการลงทะเบียนข้อบกพร่องที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c5c89-177">The name changes are automatically reflected in the related fault registrations.</span></span>
