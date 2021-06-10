---
title: ตั้งค่าคอนฟิกระบบบริการตนเองของพนักงาน
description: ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดในบริการตนเองของพนักงาน
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f0d39b30b7c8d0a5729ebe3b1ed9e0d569a6660
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052996"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="77623-103">ตั้งค่าคอนฟิกระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="77623-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="77623-104">ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดในบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="77623-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="77623-105">ไทล์แผนสิทธิประโยชน์ครอบคลุมผู้ใช้โดยตรงสำหรับแผนสิทธิประโยชน์ที่พวกเขามีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="77623-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="77623-106">ตั้งค่าไทล์ของแผนสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="77623-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="77623-107">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="77623-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="77623-108">เลือกแท็บ **การตั้งค่าไทล์ของแผนสิทธิประโยชน์** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="77623-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="77623-109">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="77623-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="77623-110">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="77623-110">Field</span></span> | <span data-ttu-id="77623-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="77623-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="77623-112">**รหัสไทล์**</span><span class="sxs-lookup"><span data-stu-id="77623-112">**Tile ID**</span></span> | <span data-ttu-id="77623-113">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="77623-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="77623-114">**ข้อความป้ายชื่อของไทล์**</span><span class="sxs-lookup"><span data-stu-id="77623-114">**Tile label text**</span></span> | <span data-ttu-id="77623-115">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="77623-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="77623-116">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="77623-116">**Description**</span></span> | <span data-ttu-id="77623-117">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="77623-117">A description of the tile.</span></span> |
   | <span data-ttu-id="77623-118">**ที่อยู่อินเทอร์เน็ต**</span><span class="sxs-lookup"><span data-stu-id="77623-118">**Internet address**</span></span> | <span data-ttu-id="77623-119">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="77623-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="77623-120">**ขนาดไทล์**</span><span class="sxs-lookup"><span data-stu-id="77623-120">**Tile size**</span></span> | <span data-ttu-id="77623-121">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="77623-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="77623-122">**เป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="77623-122">**Target**</span></span> | <span data-ttu-id="77623-123">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="77623-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="77623-124">**รูปภาพพื้นหลังของไทล์**</span><span class="sxs-lookup"><span data-stu-id="77623-124">**Tile background image**</span></span> | <span data-ttu-id="77623-125">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="77623-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="77623-126">**เริ่ม**</span><span class="sxs-lookup"><span data-stu-id="77623-126">**Start**</span></span> | <span data-ttu-id="77623-127">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="77623-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="77623-128">**End**</span><span class="sxs-lookup"><span data-stu-id="77623-128">**End**</span></span> | <span data-ttu-id="77623-129">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="77623-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="77623-130">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="77623-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="77623-131">ตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="77623-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="77623-132">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="77623-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="77623-133">เลือกแท็บ **การตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="77623-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="77623-134">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="77623-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="77623-135">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="77623-135">Field</span></span> | <span data-ttu-id="77623-136">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="77623-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="77623-137">**รหัสไทล์**</span><span class="sxs-lookup"><span data-stu-id="77623-137">**Tile ID**</span></span> | <span data-ttu-id="77623-138">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="77623-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="77623-139">**ข้อความป้ายชื่อของไทล์**</span><span class="sxs-lookup"><span data-stu-id="77623-139">**Tile label text**</span></span> | <span data-ttu-id="77623-140">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="77623-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="77623-141">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="77623-141">**Description**</span></span> | <span data-ttu-id="77623-142">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="77623-142">A description of the tile.</span></span> |
   | <span data-ttu-id="77623-143">**ที่อยู่อินเทอร์เน็ต**</span><span class="sxs-lookup"><span data-stu-id="77623-143">**Internet address**</span></span> | <span data-ttu-id="77623-144">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="77623-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="77623-145">**ขนาดไทล์**</span><span class="sxs-lookup"><span data-stu-id="77623-145">**Tile size**</span></span> | <span data-ttu-id="77623-146">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="77623-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="77623-147">**เป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="77623-147">**Target**</span></span> | <span data-ttu-id="77623-148">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="77623-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="77623-149">**รูปภาพพื้นหลังของไทล์**</span><span class="sxs-lookup"><span data-stu-id="77623-149">**Tile background image**</span></span> | <span data-ttu-id="77623-150">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="77623-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="77623-151">**เริ่ม**</span><span class="sxs-lookup"><span data-stu-id="77623-151">**Start**</span></span> | <span data-ttu-id="77623-152">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="77623-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="77623-153">**End**</span><span class="sxs-lookup"><span data-stu-id="77623-153">**End**</span></span> | <span data-ttu-id="77623-154">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="77623-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="77623-155">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="77623-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]