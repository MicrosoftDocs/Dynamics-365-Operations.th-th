---
title: ตั้งค่าคอนฟิกระบบบริการตนเองของพนักงาน
description: ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดในบริการตนเองของพนักงาน
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
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092671"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="f7332-103">ตั้งค่าคอนฟิกระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7332-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f7332-104">ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดในบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7332-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="f7332-105">แผนสิทธิประโยชน์ครอบคลุมผู้ใช้โดยตรงสำหรับแผนสิทธิประโยชน์ที่พวกเขามีสิทธิ์ที่จะลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7332-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="f7332-106">ตั้งค่าไทล์ศูนย์บทบาท</span><span class="sxs-lookup"><span data-stu-id="f7332-106">Set up a role center tile</span></span>

1. <span data-ttu-id="f7332-107">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="f7332-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f7332-108">เลือกแท็บ **การตั้งค่าไทล์ศูนย์บทบาท** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f7332-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f7332-109">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7332-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f7332-110">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="f7332-110">Field</span></span> | <span data-ttu-id="f7332-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f7332-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f7332-112">รหัสไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-112">Tile ID</span></span> | <span data-ttu-id="f7332-113">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f7332-114">ข้อความป้ายชื่อของไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-114">Tile label text</span></span> | <span data-ttu-id="f7332-115">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="f7332-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f7332-116">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f7332-116">Description</span></span> | <span data-ttu-id="f7332-117">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-117">A description of the tile.</span></span> |
   | <span data-ttu-id="f7332-118">ที่อยู่อินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="f7332-118">Internet address</span></span> | <span data-ttu-id="f7332-119">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7332-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f7332-120">ขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-120">Tile size</span></span> | <span data-ttu-id="f7332-121">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="f7332-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f7332-122">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f7332-122">Target</span></span> | <span data-ttu-id="f7332-123">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f7332-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f7332-124">รูปภาพพื้นหลังของไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-124">Tile background image</span></span> | <span data-ttu-id="f7332-125">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="f7332-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f7332-126">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="f7332-126">Start</span></span> | <span data-ttu-id="f7332-127">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f7332-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f7332-128">End</span><span class="sxs-lookup"><span data-stu-id="f7332-128">End</span></span> | <span data-ttu-id="f7332-129">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f7332-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f7332-130">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f7332-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="f7332-131">ตั้งค่าไทล์ของแผนสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="f7332-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="f7332-132">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="f7332-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f7332-133">เลือกแท็บ **การตั้งค่าไทล์ของแผนสิทธิประโยชน์** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f7332-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f7332-134">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7332-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f7332-135">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="f7332-135">Field</span></span> | <span data-ttu-id="f7332-136">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f7332-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f7332-137">รหัสไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-137">Tile ID</span></span> | <span data-ttu-id="f7332-138">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f7332-139">ข้อความป้ายชื่อของไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-139">Tile label text</span></span> | <span data-ttu-id="f7332-140">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="f7332-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f7332-141">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f7332-141">Description</span></span> | <span data-ttu-id="f7332-142">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-142">A description of the tile.</span></span> |
   | <span data-ttu-id="f7332-143">ที่อยู่อินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="f7332-143">Internet address</span></span> | <span data-ttu-id="f7332-144">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7332-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f7332-145">ขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-145">Tile size</span></span> | <span data-ttu-id="f7332-146">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="f7332-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f7332-147">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f7332-147">Target</span></span> | <span data-ttu-id="f7332-148">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f7332-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f7332-149">รูปภาพพื้นหลังของไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-149">Tile background image</span></span> | <span data-ttu-id="f7332-150">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="f7332-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f7332-151">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="f7332-151">Start</span></span> | <span data-ttu-id="f7332-152">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f7332-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f7332-153">End</span><span class="sxs-lookup"><span data-stu-id="f7332-153">End</span></span> | <span data-ttu-id="f7332-154">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f7332-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f7332-155">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f7332-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="f7332-156">ตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="f7332-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="f7332-157">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="f7332-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f7332-158">เลือกแท็บ **การตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f7332-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f7332-159">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7332-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f7332-160">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="f7332-160">Field</span></span> | <span data-ttu-id="f7332-161">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f7332-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f7332-162">รหัสไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-162">Tile ID</span></span> | <span data-ttu-id="f7332-163">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f7332-164">ข้อความป้ายชื่อของไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-164">Tile label text</span></span> | <span data-ttu-id="f7332-165">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="f7332-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f7332-166">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f7332-166">Description</span></span> | <span data-ttu-id="f7332-167">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-167">A description of the tile.</span></span> |
   | <span data-ttu-id="f7332-168">ที่อยู่อินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="f7332-168">Internet address</span></span> | <span data-ttu-id="f7332-169">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7332-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f7332-170">ขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-170">Tile size</span></span> | <span data-ttu-id="f7332-171">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="f7332-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f7332-172">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f7332-172">Target</span></span> | <span data-ttu-id="f7332-173">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f7332-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f7332-174">รูปภาพพื้นหลังของไทล์</span><span class="sxs-lookup"><span data-stu-id="f7332-174">Tile background image</span></span> | <span data-ttu-id="f7332-175">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="f7332-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f7332-176">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="f7332-176">Start</span></span> | <span data-ttu-id="f7332-177">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f7332-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f7332-178">End</span><span class="sxs-lookup"><span data-stu-id="f7332-178">End</span></span> | <span data-ttu-id="f7332-179">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f7332-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f7332-180">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f7332-180">Select **Save**.</span></span>
