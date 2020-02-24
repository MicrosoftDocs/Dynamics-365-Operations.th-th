---
title: การตั้งค่าระบบบริการตนเองของพนักงาน
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010741"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="bb095-102">การตั้งค่าระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="bb095-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="bb095-103">ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดในบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="bb095-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="bb095-104">แผนสิทธิประโยชน์ครอบคลุมผู้ใช้โดยตรงสำหรับแผนสิทธิประโยชน์ที่พวกเขามีสิทธิ์ที่จะลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bb095-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="bb095-105">ตั้งค่าไทล์ศูนย์บทบาท</span><span class="sxs-lookup"><span data-stu-id="bb095-105">Set up a role center tile</span></span>

1. <span data-ttu-id="bb095-106">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="bb095-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="bb095-107">เลือกแท็บ **การตั้งค่าไทล์ศูนย์บทบาท** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bb095-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="bb095-108">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bb095-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bb095-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bb095-109">Field</span></span> | <span data-ttu-id="bb095-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb095-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bb095-111">รหัสไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-111">Tile ID</span></span> | <span data-ttu-id="bb095-112">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="bb095-113">ข้อความป้ายชื่อของไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-113">Tile label text</span></span> | <span data-ttu-id="bb095-114">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="bb095-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="bb095-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb095-115">Description</span></span> | <span data-ttu-id="bb095-116">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-116">A description of the tile.</span></span> |
   | <span data-ttu-id="bb095-117">ที่อยู่อินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="bb095-117">Internet address</span></span> | <span data-ttu-id="bb095-118">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="bb095-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="bb095-119">ขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-119">Tile size</span></span> | <span data-ttu-id="bb095-120">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="bb095-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="bb095-121">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="bb095-121">Target</span></span> | <span data-ttu-id="bb095-122">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bb095-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="bb095-123">รูปภาพพื้นหลังของไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-123">Tile background image</span></span> | <span data-ttu-id="bb095-124">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="bb095-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="bb095-125">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="bb095-125">Start</span></span> | <span data-ttu-id="bb095-126">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb095-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="bb095-127">End</span><span class="sxs-lookup"><span data-stu-id="bb095-127">End</span></span> | <span data-ttu-id="bb095-128">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb095-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="bb095-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="bb095-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="bb095-130">ตั้งค่าไทล์ของแผนสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="bb095-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="bb095-131">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="bb095-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="bb095-132">เลือกแท็บ **การตั้งค่าไทล์ของแผนสิทธิประโยชน์** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bb095-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="bb095-133">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bb095-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bb095-134">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bb095-134">Field</span></span> | <span data-ttu-id="bb095-135">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb095-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bb095-136">รหัสไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-136">Tile ID</span></span> | <span data-ttu-id="bb095-137">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="bb095-138">ข้อความป้ายชื่อของไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-138">Tile label text</span></span> | <span data-ttu-id="bb095-139">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="bb095-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="bb095-140">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb095-140">Description</span></span> | <span data-ttu-id="bb095-141">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-141">A description of the tile.</span></span> |
   | <span data-ttu-id="bb095-142">ที่อยู่อินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="bb095-142">Internet address</span></span> | <span data-ttu-id="bb095-143">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="bb095-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="bb095-144">ขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-144">Tile size</span></span> | <span data-ttu-id="bb095-145">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="bb095-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="bb095-146">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="bb095-146">Target</span></span> | <span data-ttu-id="bb095-147">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bb095-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="bb095-148">รูปภาพพื้นหลังของไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-148">Tile background image</span></span> | <span data-ttu-id="bb095-149">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="bb095-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="bb095-150">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="bb095-150">Start</span></span> | <span data-ttu-id="bb095-151">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb095-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="bb095-152">End</span><span class="sxs-lookup"><span data-stu-id="bb095-152">End</span></span> | <span data-ttu-id="bb095-153">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb095-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="bb095-154">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="bb095-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="bb095-155">ตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="bb095-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="bb095-156">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="bb095-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="bb095-157">เลือกแท็บ **การตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bb095-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="bb095-158">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bb095-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bb095-159">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bb095-159">Field</span></span> | <span data-ttu-id="bb095-160">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb095-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bb095-161">รหัสไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-161">Tile ID</span></span> | <span data-ttu-id="bb095-162">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="bb095-163">ข้อความป้ายชื่อของไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-163">Tile label text</span></span> | <span data-ttu-id="bb095-164">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="bb095-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="bb095-165">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb095-165">Description</span></span> | <span data-ttu-id="bb095-166">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-166">A description of the tile.</span></span> |
   | <span data-ttu-id="bb095-167">ที่อยู่อินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="bb095-167">Internet address</span></span> | <span data-ttu-id="bb095-168">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="bb095-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="bb095-169">ขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-169">Tile size</span></span> | <span data-ttu-id="bb095-170">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="bb095-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="bb095-171">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="bb095-171">Target</span></span> | <span data-ttu-id="bb095-172">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bb095-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="bb095-173">รูปภาพพื้นหลังของไทล์</span><span class="sxs-lookup"><span data-stu-id="bb095-173">Tile background image</span></span> | <span data-ttu-id="bb095-174">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="bb095-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="bb095-175">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="bb095-175">Start</span></span> | <span data-ttu-id="bb095-176">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb095-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="bb095-177">End</span><span class="sxs-lookup"><span data-stu-id="bb095-177">End</span></span> | <span data-ttu-id="bb095-178">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb095-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="bb095-179">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="bb095-179">Select **Save**.</span></span>
