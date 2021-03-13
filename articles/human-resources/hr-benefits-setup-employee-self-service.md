---
title: ตั้งค่าคอนฟิกระบบบริการตนเองของพนักงาน
description: ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดในบริการตนเองของพนักงาน
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
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
ms.openlocfilehash: 32981812eac3c08e1409fe5470b550e421f5d6c9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114442"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="4277d-103">ตั้งค่าคอนฟิกระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="4277d-103">Configure employee self service</span></span>

<span data-ttu-id="4277d-104">ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดในบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="4277d-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="4277d-105">ไทล์แผนสิทธิประโยชน์ครอบคลุมผู้ใช้โดยตรงสำหรับแผนสิทธิประโยชน์ที่พวกเขามีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="4277d-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="4277d-106">ตั้งค่าไทล์ของแผนสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="4277d-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="4277d-107">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="4277d-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="4277d-108">เลือกแท็บ **การตั้งค่าไทล์ของแผนสิทธิประโยชน์** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4277d-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="4277d-109">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4277d-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4277d-110">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="4277d-110">Field</span></span> | <span data-ttu-id="4277d-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4277d-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4277d-112">**รหัสไทล์**</span><span class="sxs-lookup"><span data-stu-id="4277d-112">**Tile ID**</span></span> | <span data-ttu-id="4277d-113">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="4277d-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="4277d-114">**ข้อความป้ายชื่อของไทล์**</span><span class="sxs-lookup"><span data-stu-id="4277d-114">**Tile label text**</span></span> | <span data-ttu-id="4277d-115">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="4277d-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="4277d-116">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="4277d-116">**Description**</span></span> | <span data-ttu-id="4277d-117">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="4277d-117">A description of the tile.</span></span> |
   | <span data-ttu-id="4277d-118">**ที่อยู่อินเทอร์เน็ต**</span><span class="sxs-lookup"><span data-stu-id="4277d-118">**Internet address**</span></span> | <span data-ttu-id="4277d-119">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="4277d-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="4277d-120">**ขนาดไทล์**</span><span class="sxs-lookup"><span data-stu-id="4277d-120">**Tile size**</span></span> | <span data-ttu-id="4277d-121">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="4277d-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="4277d-122">**เป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="4277d-122">**Target**</span></span> | <span data-ttu-id="4277d-123">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4277d-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="4277d-124">**รูปภาพพื้นหลังของไทล์**</span><span class="sxs-lookup"><span data-stu-id="4277d-124">**Tile background image**</span></span> | <span data-ttu-id="4277d-125">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="4277d-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="4277d-126">**เริ่ม**</span><span class="sxs-lookup"><span data-stu-id="4277d-126">**Start**</span></span> | <span data-ttu-id="4277d-127">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4277d-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="4277d-128">**End**</span><span class="sxs-lookup"><span data-stu-id="4277d-128">**End**</span></span> | <span data-ttu-id="4277d-129">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4277d-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="4277d-130">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4277d-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="4277d-131">ตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="4277d-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="4277d-132">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="4277d-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="4277d-133">เลือกแท็บ **การตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา** จากนั้นเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4277d-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="4277d-134">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4277d-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4277d-135">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="4277d-135">Field</span></span> | <span data-ttu-id="4277d-136">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4277d-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4277d-137">**รหัสไทล์**</span><span class="sxs-lookup"><span data-stu-id="4277d-137">**Tile ID**</span></span> | <span data-ttu-id="4277d-138">ตัวระบุเฉพาะสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="4277d-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="4277d-139">**ข้อความป้ายชื่อของไทล์**</span><span class="sxs-lookup"><span data-stu-id="4277d-139">**Tile label text**</span></span> | <span data-ttu-id="4277d-140">ข้อความที่จะปรากฏในไทล์ของการบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="4277d-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="4277d-141">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="4277d-141">**Description**</span></span> | <span data-ttu-id="4277d-142">คำอธิบายเกี่ยวกับไทล์</span><span class="sxs-lookup"><span data-stu-id="4277d-142">A description of the tile.</span></span> |
   | <span data-ttu-id="4277d-143">**ที่อยู่อินเทอร์เน็ต**</span><span class="sxs-lookup"><span data-stu-id="4277d-143">**Internet address**</span></span> | <span data-ttu-id="4277d-144">ป้อน URL ไปยังหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="4277d-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="4277d-145">**ขนาดไทล์**</span><span class="sxs-lookup"><span data-stu-id="4277d-145">**Tile size**</span></span> | <span data-ttu-id="4277d-146">ขนาดของไทล์ เล็ก กลาง หรือใหญ่</span><span class="sxs-lookup"><span data-stu-id="4277d-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="4277d-147">**เป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="4277d-147">**Target**</span></span> | <span data-ttu-id="4277d-148">ระบุว่าควรเปิดหน้าในหน้าต่างใหม่หรือหน้าต่างปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4277d-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="4277d-149">**รูปภาพพื้นหลังของไทล์**</span><span class="sxs-lookup"><span data-stu-id="4277d-149">**Tile background image**</span></span> | <span data-ttu-id="4277d-150">URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="4277d-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="4277d-151">**เริ่ม**</span><span class="sxs-lookup"><span data-stu-id="4277d-151">**Start**</span></span> | <span data-ttu-id="4277d-152">วันที่และเวลาเริ่มต้นของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4277d-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="4277d-153">**End**</span><span class="sxs-lookup"><span data-stu-id="4277d-153">**End**</span></span> | <span data-ttu-id="4277d-154">วันที่และเวลาสิ้นสุดของไทล์ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4277d-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="4277d-155">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4277d-155">Select **Save**.</span></span>
