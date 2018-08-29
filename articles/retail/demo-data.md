---
title: "โครงร่างหน้าจอข้อมูลสาธิตใน Retail Modern POS (MPOS) และ Cloud POS"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับโครงร่างหน้าจอ ที่มาพร้อมกับชุดข้อมูลสาธิตสำหรับประสบการณ์การขายหน้าร้าน (POS) ใน Microsoft Dynamics 365 for Retail"
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 41930e89a7cae5cdb84e728da47de3bc5de312ca
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="demo-data-screen-layouts-in-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="d9fb2-103">โครงร่างหน้าจอข้อมูลสาธิตใน Retail Modern POS (MPOS) และ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="d9fb2-103">Demo data screen layouts in Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9fb2-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับโครงร่างหน้าจอ ที่มาพร้อมกับชุดข้อมูลสาธิตสำหรับประสบการณ์การขายหน้าร้าน (POS) ใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="d9fb2-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="d9fb2-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="d9fb2-105">Overview</span></span>

<span data-ttu-id="d9fb2-106">โครงร่างหน้าจอตัวอย่างที่มาพร้อมกับข้อมูลสาธิตของการขายปลีก ให้เนื้อหาที่มีการปรับให้เหมาะสมสำหรับเซ็กเมนต์ บทบาทผู้ปฏิบัติงาน และอุปกรณ์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-106">The sample screen layouts that are included with Retail demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="d9fb2-107">โครงร่างเดี่ยวอาจประกอบด้วยหลายขนาดโครงร่างและชุดของกริดปุ่ม เพื่อช่วยให้มั่นใจถึงความครอบคลุม เมื่อผู้ปฏิบัติงานประจำร้านย้ายที่ระหว่างอุปกรณ์และสถานีของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d9fb2-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="d9fb2-108">หัวข้อนี้เน้นถึงผลต่างระหว่างโครงร่างเหล่านี้ การดำเนินการที่พวกเขาให้ ประสบการณ์โดยรวมที่พวกเขาจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![โครงร่างข้อมูลสาธิตระหว่างอุปกรณ์](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="d9fb2-110">Anatomy ของรหัสโครงร่างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="d9fb2-111">เมื่อต้องการค้นหาโครงร่างหน้าจอในการขายปลีก ไปที่ **การขายปลีก** > **ตั้งค่าช่องทาง** > **ตั้งค่า POS** > **POS** > **โครงร่างหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="d9fb2-111">To find screen layouts in Retail, go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>

![หน้าโครงร่างหน้าจอในการขายปลีก](../retail/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="d9fb2-113">รหัสโครงร่างหน้าจอสามารถมีได้สูงสุด 10 อักขระ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="d9fb2-114">รหัสจะเป็นสตริงที่ประกอบด้วยสามส่วนข้อมูล ตามลำดับนี้:</span><span class="sxs-lookup"><span data-stu-id="d9fb2-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="d9fb2-115">บริษัท</span><span class="sxs-lookup"><span data-stu-id="d9fb2-115">Company</span></span>
2. <span data-ttu-id="d9fb2-116">รุ่นโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-116">Layout version</span></span>
3. <span data-ttu-id="d9fb2-117">ลักษณะ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="d9fb2-118">บริษัท</span><span class="sxs-lookup"><span data-stu-id="d9fb2-118">Company</span></span>

| <span data-ttu-id="d9fb2-119">จดหมาย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-119">Letter</span></span> | <span data-ttu-id="d9fb2-120">บริษัท</span><span class="sxs-lookup"><span data-stu-id="d9fb2-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="d9fb2-121">A</span><span class="sxs-lookup"><span data-stu-id="d9fb2-121">A</span></span>      | <span data-ttu-id="d9fb2-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="d9fb2-122">Adventure Works</span></span> |
| <span data-ttu-id="d9fb2-123">F</span><span class="sxs-lookup"><span data-stu-id="d9fb2-123">F</span></span>      | <span data-ttu-id="d9fb2-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d9fb2-124">Fabrikam</span></span>        |
| <span data-ttu-id="d9fb2-125">C</span><span class="sxs-lookup"><span data-stu-id="d9fb2-125">C</span></span>      | <span data-ttu-id="d9fb2-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="d9fb2-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="d9fb2-127">รุ่นโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-127">Layout version</span></span>

| <span data-ttu-id="d9fb2-128">หมายเลขเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-128">Version number</span></span> | <span data-ttu-id="d9fb2-129">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9fb2-130">3</span><span class="sxs-lookup"><span data-stu-id="d9fb2-130">3</span></span>              | <span data-ttu-id="d9fb2-131">รุ่นพื้นฐานที่รองรับหน้าจอขนาดต่างๆ สำหรับอุปกรณ์ต่างๆ และอัตราส่วนกว้างยาว</span><span class="sxs-lookup"><span data-stu-id="d9fb2-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="d9fb2-132">3.1</span><span class="sxs-lookup"><span data-stu-id="d9fb2-132">3.1</span></span>            | <span data-ttu-id="d9fb2-133">เวอร์ชันพื้นฐานที่มีการสนับสนุนเพิ่มเติมสำหรับแผง **ผลิตภัณฑ์ที่แนะนำ**</span><span class="sxs-lookup"><span data-stu-id="d9fb2-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="d9fb2-134">ลักษณะ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-134">Persona</span></span>

| <span data-ttu-id="d9fb2-135">ตัวย่อ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-135">Abbreviation</span></span> | <span data-ttu-id="d9fb2-136">ลักษณะ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-136">Persona</span></span>       | <span data-ttu-id="d9fb2-137">เนื้อหา</span><span class="sxs-lookup"><span data-stu-id="d9fb2-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="d9fb2-138">CSH</span><span class="sxs-lookup"><span data-stu-id="d9fb2-138">CSH</span></span>          | <span data-ttu-id="d9fb2-139">พนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-139">Cashier</span></span>       | <span data-ttu-id="d9fb2-140">โครงร่างพนักงานเก็บเงินรวมการดำเนินงานที่เกี่ยวข้องกับธุรกรรมทั้งหมด เช่น ใบสั่งของลูกค้า การส่งคืน ส่วนลด การยกเลิก และคืนบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="d9fb2-141">โครงร่างเหล่านี้ยังรวมงานประจำวันสำหรับการจัดการสินค้าคงคลัง เช่น การตรวจสอบราคา การค้นหาสินค้าคงคลัง และการตรวจนับสินค้าคงคลังด้วย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="d9fb2-142">ยังมีระบุการจัดการกะพื้นฐานสำหรับยอดเงินเริ่มต้น การระงับกะ และนาฬิกาตอกบัตรด้วย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="d9fb2-143">MGR</span><span class="sxs-lookup"><span data-stu-id="d9fb2-143">MGR</span></span>          | <span data-ttu-id="d9fb2-144">ผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d9fb2-144">Store Manager</span></span> | <span data-ttu-id="d9fb2-145">โครงร่างผู้จัดการร้านค้ารวมการดำเนินการที่เกี่ยวข้องกับธุรกรรมทั้งหมดที่พบในโครงร่างพนักงานเก็บเงิน แต่ยังจะมีการแทนที่ภาษีด้วย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="d9fb2-146">โครงร่างเหล่านี้ยังรวมงานประจำวันสำหรับการจัดการสินค้าคงคลัง เช่น การตรวจสอบราคา การค้นหาสินค้าคงคลัง และการตรวจนับสินค้าคงคลังด้วย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="d9fb2-147">มีระบุการจัดการกะสำหรับการเริ่มต้น การระงับ และการปิดกะ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="d9fb2-148">นอกจากนี้ โครงร่างประกอบด้วย การดำเนินงานลิ้นชักสำหรับรายการ การเอาออก การตรวจนับเงิน และการนำเงินฝากเข้าเซฟและธนาคาร</span><span class="sxs-lookup"><span data-stu-id="d9fb2-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="d9fb2-149">ในตอนท้าย เค้าโครงเหล่านี้รวมถึงการเข้าถึงรายงานประสิทธิภาพการทำงาน และเปิดใช้งานรายงาน X และ Z ที่จะถูกพิมพ์</span><span class="sxs-lookup"><span data-stu-id="d9fb2-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="d9fb2-150">STK</span><span class="sxs-lookup"><span data-stu-id="d9fb2-150">STK</span></span>          | <span data-ttu-id="d9fb2-151">เจ้าหน้าที่สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-151">Stock Clerk</span></span>   | <span data-ttu-id="d9fb2-152">โครงร่างของเจ้าหน้าที่สินค้าคงคลังมีการปรับให้เหมาะสำหรับการบริหารสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="d9fb2-153">พวกเขารวมการเข้าถึงกับงานประจำวันสำหรับการตรวจสอบราคา การค้นหาในสินค้าคงคลัง การเบิกสินค้าและการรับสินค้า การตรวจนับสินค้าคงคลัง และการแยกชุด</span><span class="sxs-lookup"><span data-stu-id="d9fb2-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="d9fb2-154">โครงร่างเหล่านี้ยังให้ดำเนินงานกะพื้นฐานสำหรับนาฬิกาตอกบัตรและการระงับกะอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="d9fb2-155">ถึงแม้ว่าโครงร่างเหล่านี้มีไว้สำหรับงานสนับสนุนโดยส่วนใหญ่ เจ้าหน้าที่สินค้าคงคลังมีการดำเนินงานเดียวกันกับพนักงานเก็บเงินสำหรับหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d9fb2-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="d9fb2-156">โครงร่างตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-156">Example layout</span></span>

<span data-ttu-id="d9fb2-157">นี่เป็นตัวอย่างของรหัสโครงร่างหน้าจอสำหรับบริษัท Fabrikam โครงร่างรุ่น 3 และลักษณะผู้จัดการร้านค้า:</span><span class="sxs-lookup"><span data-stu-id="d9fb2-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="d9fb2-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="d9fb2-158">F3MGR</span></span>

<span data-ttu-id="d9fb2-159">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้าจอต้อนรับสำหรับผู้จัดการร้านค้า Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d9fb2-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![หน้าจอต้อนรับสำหรับผู้จัดการร้านค้า Fabrikam](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="d9fb2-161">ขนาดโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="d9fb2-162">เค้าโครงแบบเต็ม vs. แบบย่อ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-162">Full vs. compact layouts</span></span>

<span data-ttu-id="d9fb2-163">เค้าโครงหน้าจอสามารถมีการตั้งค่าคอนฟิกได้สำหรับทั้งอุปกรณ์แบบเต็มและแบบย่อ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="d9fb2-164">ดังนั้น ผู้ใช้สามรถถูกมอบหมายให้กับโครงร่างหน้าจอเดี่ยวที่จะทำงานในขนาดและสัดส่วนของแบบฟอร์มที่หลากหลายภายในร้านค้าได้</span><span class="sxs-lookup"><span data-stu-id="d9fb2-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="d9fb2-165">**Modern POS - รุ่นเต็ม** - โดยทั่วไปโครงร่างแบบเต็มจะใช้ได้ดีที่สุดสำหรับการแสดงขนาดใหญ่ เช่น จอภาพของคอมพิวเตอร์เดสก์ท็อปหรือแท็บเล็ต</span><span class="sxs-lookup"><span data-stu-id="d9fb2-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="d9fb2-166">ผู้ใช้สามารถเลือกองค์ประกอบ UI ที่มีโครงร่าง ระบุขนาดและตำแหน่งขององค์ประกอบเหล่านั้น และตั้งค่าคอนฟิกคุณสมบัติโดยรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="d9fb2-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="d9fb2-167">เค้าโครงทั้งหมดสนับสนุนการตั้งค่าคอนฟิกทั้งแนวตั้งและแนวนอน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="d9fb2-168">**Modern POS - รุ่นย่อ** - โดยทั่วไปโครงร่างแบบย่อจะใช้ได้ดีที่สุดสำหรับโทรศัพท์หรือแท็บเล็ตขนาดเล็ก</span><span class="sxs-lookup"><span data-stu-id="d9fb2-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="d9fb2-169">ความสามารถในการออกแบบถูกจำกัดสำหรับอุปกรณ์แบบย่อ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="d9fb2-170">ผู้ใช้สามารถตั้งค่าคอนฟิกคอลัมน์และฟิลด์ได้สำหรับบานหน้าต่างการรับสินค้าและบานหน้าต่างผลรวม</span><span class="sxs-lookup"><span data-stu-id="d9fb2-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="d9fb2-171">ความละเอียดหน้าจอที่มีให้</span><span class="sxs-lookup"><span data-stu-id="d9fb2-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="d9fb2-172">ตารางต่อไปนี้แสดงขนาดของโครงร่างที่กำหนดไว้สำหรับความละเอียดของหน้าจอโดยทั่วไป</span><span class="sxs-lookup"><span data-stu-id="d9fb2-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="d9fb2-173">ชนิดของโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-173">Layout type</span></span> | <span data-ttu-id="d9fb2-174">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="d9fb2-174">Resolution</span></span> | <span data-ttu-id="d9fb2-175">อัตราส่วนกว้างยาว</span><span class="sxs-lookup"><span data-stu-id="d9fb2-175">Aspect ratio</span></span> | <span data-ttu-id="d9fb2-176">การแสดงเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="d9fb2-177">อัดแน่น\*</span><span class="sxs-lookup"><span data-stu-id="d9fb2-177">Compact\*</span></span>   | <span data-ttu-id="d9fb2-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="d9fb2-178">480 × 853</span></span>  | <span data-ttu-id="d9fb2-179">16:9 น.</span><span class="sxs-lookup"><span data-stu-id="d9fb2-179">16:9</span></span>         | <span data-ttu-id="d9fb2-180">โทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="d9fb2-180">Phones</span></span>                  |
| <span data-ttu-id="d9fb2-181">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d9fb2-181">Full</span></span>        | <span data-ttu-id="d9fb2-182">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="d9fb2-182">1024 × 768</span></span> | <span data-ttu-id="d9fb2-183">4:3 น.</span><span class="sxs-lookup"><span data-stu-id="d9fb2-183">4:3</span></span>          | <span data-ttu-id="d9fb2-184">แท็บเล็ต</span><span class="sxs-lookup"><span data-stu-id="d9fb2-184">Tablets</span></span>                 |
| <span data-ttu-id="d9fb2-185">ทั้งหมด\*</span><span class="sxs-lookup"><span data-stu-id="d9fb2-185">Full\*</span></span>      | <span data-ttu-id="d9fb2-186">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="d9fb2-186">1280 × 720</span></span> | <span data-ttu-id="d9fb2-187">16:9 น.</span><span class="sxs-lookup"><span data-stu-id="d9fb2-187">16:9</span></span>         | <span data-ttu-id="d9fb2-188">แท็บเล็ต</span><span class="sxs-lookup"><span data-stu-id="d9fb2-188">Tablets</span></span>                 |
| <span data-ttu-id="d9fb2-189">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d9fb2-189">Full</span></span>        | <span data-ttu-id="d9fb2-190">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="d9fb2-190">1366 × 768</span></span> | <span data-ttu-id="d9fb2-191">16:9 น.</span><span class="sxs-lookup"><span data-stu-id="d9fb2-191">16:9</span></span>         | <span data-ttu-id="d9fb2-192">แท็บเล็ต หน้าจอที่ขนาดใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="d9fb2-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="d9fb2-193">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d9fb2-193">Full</span></span>        | <span data-ttu-id="d9fb2-194">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="d9fb2-194">1440 × 960</span></span> | <span data-ttu-id="d9fb2-195">3:2 น.</span><span class="sxs-lookup"><span data-stu-id="d9fb2-195">3:2</span></span>          | <span data-ttu-id="d9fb2-196">แท็บเล็ต หน้าจอที่ขนาดใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="d9fb2-196">Tablets, larger screens</span></span> |

<span data-ttu-id="d9fb2-197">\* ขนาดของโครงร่างเพิ่มเติมเหล่านี้จะพร้อมใช้งานเฉพาะใน Adventure Works และโครงร่างของ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d9fb2-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>


>[!TIP]
> <span data-ttu-id="d9fb2-198">POS เลือกขนาดของโครงร่างโดยอัตโนมัติ ตามขนาดใกล้เคียงที่สุดที่พร้อมใช้งานสำหรับความละเอียดของหน้าจอของหน้าต่างแอพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="d9fb2-199">เพื่อค้นหารหัสโครงร่างหน้าจอและความละเอียดโครงร่างที่ใช้อยู่ในปัจจุบัน ใน Retail Modern POS (MPOS) หรือ Retail Cloud POS (CPOS) เปิดหน้า **การตั้งค่า** และค้นหาในส่วน **ข้อมูลรอบเวลา**</span><span class="sxs-lookup"><span data-stu-id="d9fb2-199">To find the screen layout ID and layout resolution that are currently used, in Retail Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="d9fb2-200">คุณยังสามารถดูความละเอียดหน้าต่างจริงสำหรับแอพลิเคชันหรือเฟรมของเบราเซอร์ปัจจุบันของคุณได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="d9fb2-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="d9fb2-201">หลังจากที่คุณมีข้อมูลนี้ คุณสามารถค้นหาแหล่งที่มาของเนื้อหาโครงร่างได้ในการขายปลีก โดยการไปที่ **ตั้งค่าช่องทาง** > **ตั้งค่า POS** > **POS** > **โครงร่างหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="d9fb2-201">After you have this information, you can find the source of the layout content in Retail by going to **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>


![โครงร่างหน้าจอและความละเอียด/ขนาดโครงร่างในการขายปลีกและ POS](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="d9fb2-203">บริษัทและยี่ห้อ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-203">Companies and brands</span></span>

<span data-ttu-id="d9fb2-204">บริษัทสมมติแต่ละแห่งถูกตั้งเป้าหมายไปยังเซ็กเมนต์การขายปลีกที่แตกต่างกัน และมีแค็ตตาล็อกผลิตภัณฑ์ที่สามารถใช้ได้สำหรับตลาดของบริษัท</span><span class="sxs-lookup"><span data-stu-id="d9fb2-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="d9fb2-205">บริษัทแต่ละแห่งมียี่ห้อในการมองเห็นเฉพาะที่มาพร้อมกับผลิตภัณฑ์ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="d9fb2-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="d9fb2-206">องค์ประกอบของตราสินค้ารวมสีอักขระการออกเสียง ชุดรูปแบบหรือไฟ และรูปถ่ายที่มีมาซึ่งให้ประสบการณ์ตามจริง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="d9fb2-207">เซ็กเมนต์บริษัทและลักษณะแบบเป็นภาพ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="d9fb2-208">บริษัท</span><span class="sxs-lookup"><span data-stu-id="d9fb2-208">Company</span></span>         | <span data-ttu-id="d9fb2-209">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-209">Location</span></span> | <span data-ttu-id="d9fb2-210">เซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="d9fb2-210">Segment</span></span>        | <span data-ttu-id="d9fb2-211">อักขระการออกเสียง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-211">Accent</span></span> | <span data-ttu-id="d9fb2-212">ชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="d9fb2-213">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="d9fb2-213">Adventure Works</span></span> | <span data-ttu-id="d9fb2-214">ซีแอตเทิล</span><span class="sxs-lookup"><span data-stu-id="d9fb2-214">Seattle</span></span>  | <span data-ttu-id="d9fb2-215">สินค้าผลิตภัณฑ์กีฬา</span><span class="sxs-lookup"><span data-stu-id="d9fb2-215">Sporting Goods</span></span> | <span data-ttu-id="d9fb2-216">สีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-216">Blue</span></span>   | <span data-ttu-id="d9fb2-217">มืด</span><span class="sxs-lookup"><span data-stu-id="d9fb2-217">Dark</span></span>  |
| <span data-ttu-id="d9fb2-218">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d9fb2-218">Fabrikam</span></span>        | <span data-ttu-id="d9fb2-219">Houston</span><span class="sxs-lookup"><span data-stu-id="d9fb2-219">Houston</span></span>  | <span data-ttu-id="d9fb2-220">แฟชั่น</span><span class="sxs-lookup"><span data-stu-id="d9fb2-220">Fashion</span></span>        | <span data-ttu-id="d9fb2-221">สีเขียว</span><span class="sxs-lookup"><span data-stu-id="d9fb2-221">Green</span></span>  | <span data-ttu-id="d9fb2-222">Light</span><span class="sxs-lookup"><span data-stu-id="d9fb2-222">Light</span></span> |
| <span data-ttu-id="d9fb2-223">Contoso</span><span class="sxs-lookup"><span data-stu-id="d9fb2-223">Contoso</span></span>         | <span data-ttu-id="d9fb2-224">บอสตัน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-224">Boston</span></span>   | <span data-ttu-id="d9fb2-225">อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d9fb2-225">Electronics</span></span>    | <span data-ttu-id="d9fb2-226">สีแดง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-226">Red</span></span>    | <span data-ttu-id="d9fb2-227">มืด</span><span class="sxs-lookup"><span data-stu-id="d9fb2-227">Dark</span></span>  |


>[!NOTE]
> <span data-ttu-id="d9fb2-228">Adventure Works และ Fabrikam มียี่ห้อ flagship สองยี่ห้อ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="d9fb2-229">Contoso พร้อมใช้งาน แต่ไม่ได้มีโครงร่างทั้งหมดมาให้</span><span class="sxs-lookup"><span data-stu-id="d9fb2-229">Contoso is available, but not all layouts have been provided.</span></span>


<span data-ttu-id="d9fb2-230">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้าต้อนรับและหน้าธุรกรรมสำหรับบริษัทสมมติสามแห่ง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="d9fb2-231">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="d9fb2-231">Adventure Works</span></span>

![หน้าต้อนรับข้อมูลสาธิตสำหรับ Adventure Works](../retail/media/demo-screen-layouts-fig-4-1a.png)

![หน้าธุรกรรมข้อมูลสาธิตสำหรับ Adventure Works](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="d9fb2-234">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d9fb2-234">Fabrikam</span></span>

![หน้าต้อนรับข้อมูลสาธิตสำหรับ Fabrikam](../retail/media/demo-screen-layouts-fig-4-2a.png)

![หน้าธุรกรรมข้อมูลสาธิตสำหรับ Fabrikam](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="d9fb2-237">Contoso</span><span class="sxs-lookup"><span data-stu-id="d9fb2-237">Contoso</span></span>

![โครงร่างข้อมูลสาธิตสำหรับ Contoso](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="d9fb2-239">เมทริกซ์การลงชื่อเข้าใช้ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d9fb2-239">User sign in matrix</span></span>

<span data-ttu-id="d9fb2-240">ผู้ใช้ได้รับมาสำหรับโครงร่างหน้าจอต่างๆ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="d9fb2-241">โดยการใช้ตารางต่อไปนี้ คุณควรจะสามารถเข้าถึงหน้าจอใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="d9fb2-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="d9fb2-242">เพียงแค่ลงชื่อเข้าใช้ โดยการใช้รหัสการดำเนินการที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d9fb2-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="d9fb2-243">บริษัท</span><span class="sxs-lookup"><span data-stu-id="d9fb2-243">Company</span></span>         | <span data-ttu-id="d9fb2-244">รหัสโครงร่างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-244">Screen layout ID</span></span> | <span data-ttu-id="d9fb2-245">ลักษณะ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-245">Persona</span></span>          | <span data-ttu-id="d9fb2-246">รหัสผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------   |------------------------|
| <span data-ttu-id="d9fb2-247">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="d9fb2-247">Adventure Works</span></span> | <span data-ttu-id="d9fb2-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="d9fb2-248">A3MGR</span></span>            | <span data-ttu-id="d9fb2-249">ผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d9fb2-249">Store Manager</span></span>    | <span data-ttu-id="d9fb2-250">000154, 000137, 000073</span><span class="sxs-lookup"><span data-stu-id="d9fb2-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="d9fb2-251">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="d9fb2-251">Adventure Works</span></span> | <span data-ttu-id="d9fb2-252">A3CSH</span><span class="sxs-lookup"><span data-stu-id="d9fb2-252">A3CSH</span></span>            | <span data-ttu-id="d9fb2-253">พนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-253">Cashier</span></span>          | <span data-ttu-id="d9fb2-254">000150, 000175, 000165</span><span class="sxs-lookup"><span data-stu-id="d9fb2-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="d9fb2-255">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="d9fb2-255">Adventure Works</span></span> | <span data-ttu-id="d9fb2-256">A3STK</span><span class="sxs-lookup"><span data-stu-id="d9fb2-256">A3STK</span></span>            | <span data-ttu-id="d9fb2-257">เจ้าหน้าที่สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-257">Stock Clerk</span></span>      | <span data-ttu-id="d9fb2-258">000155, 000181, 000152</span><span class="sxs-lookup"><span data-stu-id="d9fb2-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="d9fb2-259">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d9fb2-259">Fabrikam</span></span>        | <span data-ttu-id="d9fb2-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="d9fb2-260">F3MGR</span></span>            | <span data-ttu-id="d9fb2-261">ผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d9fb2-261">Store Manager</span></span>    | <span data-ttu-id="d9fb2-262">000160, 000168, 000163</span><span class="sxs-lookup"><span data-stu-id="d9fb2-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="d9fb2-263">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d9fb2-263">Fabrikam</span></span>        | <span data-ttu-id="d9fb2-264">F3CSH</span><span class="sxs-lookup"><span data-stu-id="d9fb2-264">F3CSH</span></span>            | <span data-ttu-id="d9fb2-265">พนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-265">Cashier</span></span>          | <span data-ttu-id="d9fb2-266">000161, 000113, 000114</span><span class="sxs-lookup"><span data-stu-id="d9fb2-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="d9fb2-267">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d9fb2-267">Fabrikam</span></span>        | <span data-ttu-id="d9fb2-268">F3STK</span><span class="sxs-lookup"><span data-stu-id="d9fb2-268">F3STK</span></span>            | <span data-ttu-id="d9fb2-269">เจ้าหน้าที่สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-269">Stock Clerk</span></span>      | <span data-ttu-id="d9fb2-270">000164, 000112, 000123</span><span class="sxs-lookup"><span data-stu-id="d9fb2-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="d9fb2-271">Contoso</span><span class="sxs-lookup"><span data-stu-id="d9fb2-271">Contoso</span></span>         | <span data-ttu-id="d9fb2-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="d9fb2-272">C3MGR</span></span>            | <span data-ttu-id="d9fb2-273">ผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d9fb2-273">Store Manager</span></span>    | <span data-ttu-id="d9fb2-274">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="d9fb2-274">000100, 000111</span></span>         |
| <span data-ttu-id="d9fb2-275">Contoso</span><span class="sxs-lookup"><span data-stu-id="d9fb2-275">Contoso</span></span>         | <span data-ttu-id="d9fb2-276">C3CSH</span><span class="sxs-lookup"><span data-stu-id="d9fb2-276">C3CSH</span></span>            | <span data-ttu-id="d9fb2-277">พนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d9fb2-277">Cashier</span></span>          | <span data-ttu-id="d9fb2-278">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="d9fb2-278">000110, 000120</span></span>         |
| <span data-ttu-id="d9fb2-279">Contoso</span><span class="sxs-lookup"><span data-stu-id="d9fb2-279">Contoso</span></span>         | <span data-ttu-id="d9fb2-280">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="d9fb2-280">Not applicable</span></span>   | <span data-ttu-id="d9fb2-281">เจ้าหน้าที่สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d9fb2-281">Stock Clerk</span></span>      | <span data-ttu-id="d9fb2-282">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="d9fb2-282">Not applicable</span></span>         |


>[!TIP]
> <span data-ttu-id="d9fb2-283">เพื่อให้ได้ผลลัพธ์ที่ดีที่สุด เรียกใช้งานเครื่องบันทึกเงินสดในสถานเก็บที่สอดคล้องกัน และตั้งค่าบริษัทไปยังบริษัทของลักษณะที่คุณวางแผนจะใช้เมื่อคุณเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="d9fb2-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="d9fb2-284">ด้วยวิธีนี้ คุณจะช่วยรับรองว่าโพรไฟล์ภาพและรูปตราสินค้าสอดคล้องกันระหว่างประสบการณ์</span><span class="sxs-lookup"><span data-stu-id="d9fb2-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="d9fb2-285">ตัวอย่างเช่น ถ้าคุณสนใจดูโครงร่าง Fabrikam สำหรับพนักงานเก็บเงิน คุณควรเรียกใช้เครื่องบันทึกเงินสดในร้านค้า Houston</span><span class="sxs-lookup"><span data-stu-id="d9fb2-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

