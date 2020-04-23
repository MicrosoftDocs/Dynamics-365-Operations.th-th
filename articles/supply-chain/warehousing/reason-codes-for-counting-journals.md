---
title: รหัสเหตุผลสำหรับการตรวจนับสินค้าคงคลัง
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและใช้รหัสเหตุผลสำหรับงานการนับ
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 6d71de53f5d24ecea03892790449c7a57c60eb55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207312"
---
# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="bc936-103">รหัสเหตุผลสำหรับการตรวจนับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="bc936-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc936-104">รหัสเหตุผลช่วยคุณวิเคราะห์ผลลัพธ์ของกระบวนการตรวจนับ และความขัดแย้งใดๆ ที่เกิดขึ้นในระหว่างกระบวนการนั้น</span><span class="sxs-lookup"><span data-stu-id="bc936-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="bc936-105">คุณสามารถระบุเหตุผลสำหรับการทำการตรวจนับได้ เช่น แท่นวางสินค้าที่เสียหาย หรือการปรับปรุงสินค้าคงคลังที่ยึดตามตัวอย่างของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="bc936-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="bc936-106">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bc936-106">Recommendation</span></span>

<span data-ttu-id="bc936-107">ก่อนที่คุณจะตั้งค่าระบบ เราขอแนะนำให้คุณกำหนดกลยุทธ์สำหรับการทำงานกับรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="bc936-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="bc936-108">ตัวอย่างเช่น ลองตอบคำถามต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bc936-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="bc936-109">รหัสเหตุผลควรเป็นแบบบังคับในคลังสินค้าหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="bc936-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="bc936-110">รหัสเหตุผลควรเป็นแบบบังคับหรือแบบไม่บังคับในบางรายการหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="bc936-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="bc936-111">คุณต้องการรหัสเหตุผลกี่รหัส?</span><span class="sxs-lookup"><span data-stu-id="bc936-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="bc936-112">ผู้ใช้สแกนเนอร์ของบาร์โค้ดควรใช้รหัสเหตุผลอย่างไร?</span><span class="sxs-lookup"><span data-stu-id="bc936-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="bc936-113">รหัสเหตุผลควรถูกเลือกไว้ล่วงหน้า เป็นแบบบังคับ หรือไม่สามารถแก้ไขได้?</span><span class="sxs-lookup"><span data-stu-id="bc936-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="bc936-114">พนักงานคลังสินค้าต้องมีพฤติกรรมรหัสเหตุผลที่แตกต่างกันบนสแกนเนอร์แบบเคลื่อนที่หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="bc936-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="bc936-115">ถ้าคำตอบคือ ใช่ คุณสามารถสร้างรายการเมนูเพิ่มเติม และกำหนดให้กับบุคคลอื่นได้</span><span class="sxs-lookup"><span data-stu-id="bc936-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="bc936-116">ที่ซึงใช้รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="bc936-116">Where reason codes apply</span></span>

<span data-ttu-id="bc936-117">คุณสามารถสร้างนโยบายรหัสเหตุผลหลายรายการได้ และนโยบายรหัสเหตุผลแต่ละรายการสามารถมีนโยบายรหัสเหตุผลการนับสองรายการ</span><span class="sxs-lookup"><span data-stu-id="bc936-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="bc936-118">คุณสามารถใช้นโยบายรหัสเหตุผลการนับที่ระดับคลังสินค้าหรือระดับสินค้า</span><span class="sxs-lookup"><span data-stu-id="bc936-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="bc936-119">ตั้งค่านโยบายรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="bc936-119">Set up reason code policies</span></span>

1. <span data-ttu-id="bc936-120">เลือก **การบริหารสินค้าคงคลัง** \> **ตั้งค่า** \> **สินค้าคงคลัง** \> **นโยบายรหัสเหตุผลของการตรวจนับ** และสร้างนโยบายรหัสเหตุผลใหม่</span><span class="sxs-lookup"><span data-stu-id="bc936-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="bc936-121">ในฟิลด์ **ชนิดรหัสเหตุผลการตรวจนับ** เลือก **แบบบังคับ** หรือ **แบบไม่บังคับ** อย่างใดอย่างหนึ่ง เพื่อระบุว่าการเลือกรหัสเหตุผลควรเป็นการดำเนินการแบบไม่บังคับหรือแบบบังคับ ในหนึ่งในสมุดรายวันการตรวจนับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bc936-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="bc936-122">การตรวจนับตามรอบ (อุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="bc936-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="bc936-123">การตรวจนับทันที (อุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="bc936-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="bc936-124">การตรวจนับตามขีดจำกัด (อุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="bc936-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="bc936-125">การปรับปรุงเข้า (อุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="bc936-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="bc936-126">การปรับปรุงออก (อุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="bc936-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="bc936-127">การตรวจนับสมุดรายวัน (ไคลเอนต์ที่สมบูรณ์)</span><span class="sxs-lookup"><span data-stu-id="bc936-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="bc936-128">คุณยังสามารถตั้งค่ารหัสเหตุผล สำหรับคลังสินค้าแต่ละแห่ง และสำหรับผลิตภัณฑ์ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="bc936-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="bc936-129">การตั้งค่ารหัสเหตุผลสำหรับผลิตภัณฑ์สามารถไม่คำนึงถึงการตั้งค่าสำหรับคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="bc936-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="bc936-130">รหัสเหตุผลที่เป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="bc936-130">Mandatory reason codes</span></span>

<span data-ttu-id="bc936-131">ถ้าพารามิเตอร์ **แบบบังคับ** ถูกตั้งค่าในการตั้งค่าคอนฟิกรหัสเหตุผลสำหรับคลังสินค้าหรือสินค้า สมุดรายวันการตรวจนับไม่เสร็จสมบูรณ์ และจะปิดจนกว่าจะมีการระบุรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="bc936-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="bc936-132">ตั้งค่ารหัสเหตุผลสำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bc936-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="bc936-133">เลือก **การบริหารสินค้าคงคลัง** \> **การตั้งค่า** \> **การแบ่งสินค้าคงคลัง** \> **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bc936-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="bc936-134">บนแท็บ **คลังสินค้า** ในฟิลด์ **นโยบายรหัสเหตุผลของการตรวจนับ** เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bc936-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="bc936-135">**ว่างเปล่า**– พารามิเตอร์ที่ตั้งค่าไว้สำหรับสินค้า ถูกใช้เพื่อกำหนดว่าการตรวจนับสมุดรายวันเป็นแบบบังคับสำหรับผลิตภัณฑ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bc936-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="bc936-136">**แบบบังคับ** – จำเป็นต้องใช้รหัสเหตุผลในสมุดรายวันการตรวจนับสำหรับคลังสินค้าเสมอ</span><span class="sxs-lookup"><span data-stu-id="bc936-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="bc936-137">**แบบไม่บังคับ** – ไม่จำเป็นต้องใช้รหัสเหตุผลในสมุดรายวันการตรวจนับสำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bc936-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="bc936-138">ตั้งค่ารหัสเหตุผลสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bc936-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="bc936-139">เลือก **การจัดการข้อมูลผลิตภัณฑ์** \> **ผลิตภัณฑ์** \> **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="bc936-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="bc936-140">บนแท็บ **ผลิตภัณฑ์** เลือก **นโยบายรหัสเหตุผลของการตรวจนับ** และจากนั้น เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bc936-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="bc936-141">**ว่างเปล่า** – พารามิเตอร์ที่ตั้งค่าไว้สำหรับคลังสินค้า ถูกใช้เพื่อกำหนดว่าการตรวจนับสมุดรายวันเป็นแบบบังคับสำหรับผลิตภัณฑ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bc936-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="bc936-142">**แบบบังคับ** – จำเป็นต้องใช้รหัสเหตุผลในสมุดรายวันการตรวจนับสำหรับผลิตภัณฑ์เสมอ</span><span class="sxs-lookup"><span data-stu-id="bc936-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="bc936-143">การตั้งค่านี้แทนที่การตั้งค่ารหัสเหตุผลใดๆ ในระดับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bc936-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="bc936-144">**แบบไม่บังคับ** – ไม่จำเป็นต้องใช้รหัสเหตุผลในสมุดรายวันการตรวจนับสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bc936-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="bc936-145">การตั้งค่านี้แทนที่การตั้งค่ารหัสเหตุผลใดๆ ในระดับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bc936-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="bc936-146">ใช้รหัสเหตุผลในสมุดรายวันการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="bc936-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="bc936-147">ในสมุดรายวันการตรวจนับ คุณสามารถเพิ่มรหัสเหตุผลสำหรับการตรวจนับชนิดต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="bc936-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="bc936-148">การตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="bc936-148">Cycle Count</span></span>
- <span data-ttu-id="bc936-149">การตรวจนับทันที</span><span class="sxs-lookup"><span data-stu-id="bc936-149">Spot Count</span></span>
- <span data-ttu-id="bc936-150">การตรวจนับตามขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="bc936-150">Threshold Count</span></span>
- <span data-ttu-id="bc936-151">การปรับปรุงเข้า</span><span class="sxs-lookup"><span data-stu-id="bc936-151">Adjustment In</span></span>
- <span data-ttu-id="bc936-152">การปรับปรุงออก</span><span class="sxs-lookup"><span data-stu-id="bc936-152">Adjustment Out</span></span>

<span data-ttu-id="bc936-153">รหัสเหตุผลถูกเพิ่มลงในรายการสมุดรายวันในสมุดรายวันการตรวจนับของชนิด **สมุดรายวันการตรวจนับ**</span><span class="sxs-lookup"><span data-stu-id="bc936-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="bc936-154">เลือก **การบริหารสินค้าคงคลัง** \> **รายการสมุดรายวัน** \> **การนับสินค้า** \> **การนับ**</span><span class="sxs-lookup"><span data-stu-id="bc936-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="bc936-155">ในรายละเอียดรายการของสมุดรายวันการตรวจนับ ในฟิลด์ **รหัสเหตุผลของการตรวจนับ** เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bc936-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="bc936-156">ดูประวัติการตรวจนับ ตามที่มีการบันทึกโดยรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="bc936-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="bc936-157">เลือก **การบริหารสินค้าคงคลัง** \> **การสอบถามและรายงาน** \> **ประวัติการตรวจนับ** และจากนั้น ในฟิลด์ **รหัสเหตุผลของการตรวจนับ** ดูประวัติการตรวจนับที่มีการ บันทึกโดยใช้รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="bc936-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="bc936-158">ใช้รหัสเหตุผลสำหรับการปรับปรุงปริมาณ</span><span class="sxs-lookup"><span data-stu-id="bc936-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="bc936-159">ในหน้า **สินค้าคงคลังคงเหลือ** เลือก **ปรับปรุงปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="bc936-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="bc936-160">คุณสามารถเปิดหน้า **สินค้าคงคลังคงเหลือ** ได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="bc936-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="bc936-161">ตัวอย่างเช่น เลือก **การบริหารสินค้าคงคลัง** \> **การสอบถามและรายงาน** \> **ปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="bc936-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="bc936-162">เลือก **ปรับปรุงปริมาณ** และจากนั้น ในฟิลด์ **รหัสเหตุผลของการตรวจนับ** เลือกรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="bc936-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="bc936-163">ตั้งค่าคอนฟิกรหัสเหตุผลสำหรับรายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="bc936-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="bc936-164">คุณสามารถตั้งค่าคอนฟิกรหัสเหตุผลสำหรับการตรวจนับชนิดใดๆ ได้บนรายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="bc936-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="bc936-165">การตั้งค่าคอนฟิกของรายการเมนูของอุปกรณ์เคลื่อนที่ ประกอบด้วยข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bc936-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="bc936-166">ไม่ว่ารหัสเหตุผลจะถูกแสดงสำหรับผู้ปฏิบัติงานของอุปกรณ์เคลื่อนที่ในระหว่างการตรวจนับหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bc936-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="bc936-167">รหัสเหตุผลเริ่มต้นที่จะปรากฏบนรายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="bc936-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="bc936-168">ไม่ว่าผู้ใช้จะสามารถแก้ไขรหัสเหตุผลได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bc936-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="bc936-169">ตั้งค่ารหัสเหตุผลบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="bc936-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="bc936-170">เลือก **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **อุปกรณ์เคลื่อนที่** \> **รายการเมนูอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="bc936-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="bc936-171">บนแท็บ **การตรวจนับตามรอบ** เลือก **การตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="bc936-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="bc936-172">ในฟิลด์ **รหัสเหตุผลของการตรวจนับเริ่มต้น** กำหนดรหัสเหตุผลเริ่มต้นที่ควรถูกบันทึก เมื่อดำเนินการตรวจนับโดยใช้รายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="bc936-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="bc936-173">ในฟิลด์ **แสดงรหัสเหตุผลการตรวจนับ** เลือก **รายการ** เพื่อแสดงรหัสเหตุผล หลังจากที่มีการบันทึกผลต่างแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="bc936-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="bc936-174">อีกทางหนึ่งคือ เลือก **ซ่อน** ถ้าไม่ควรแสดงรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="bc936-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="bc936-175">ตั้งค่าตัวเลือก **แก้ไขรหัสเหตุผลการตรวจนับ** เป็น **ใช่** หรือ **ไม่ใช่** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bc936-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="bc936-176">ถ้าคุณกำหนดตัวเลือกนี้เป็น **ใช่** ผู้ปฏิบัติงานสามารถแก้ไขรหัสเหตุผลได้ เมื่อมีการแสดงอยู่บนอุปกรณ์เคลื่อนที่ระหว่างการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="bc936-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="bc936-177">ปุ่ม **การตรวจนับตามรอบ** จะถูกเปิดใช้งานบนรายการเมนูของอุปกรณ์เคลื่อนใดที่ๆ ที่สามารถทำการตรวจนับได้</span><span class="sxs-lookup"><span data-stu-id="bc936-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="bc936-178">ตัวอย่างรวมถึงรายการเมนูสำหรับการตรวจนับพิเศษ งานที่สั่งการโดยผู้ใช้ และงานที่สั่งการโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="bc936-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="bc936-179">การอนุมัติการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="bc936-179">Cycle count approvals</span></span>

<span data-ttu-id="bc936-180">ก่อนที่จะมีการอนุมัติการตรวจนับ ผู้ใช้สามารถเปลี่ยนรหัสเหตุผลที่เกี่ยวข้องกับการตรวจนับได้</span><span class="sxs-lookup"><span data-stu-id="bc936-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="bc936-181">เมื่อมีการอนุมัติการตรวจนับ จะมีการป้อนรหัสเหตุผลในรายการสมุดรายวันการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="bc936-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="bc936-182">แก้ไขการอนุมัติการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="bc936-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="bc936-183">เลือก **การบริหารคลังสินค้า** \> **การตรวจนับตามรอบ** \> **การตรวจทานที่ค้างอยู่ของงานการตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="bc936-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="bc936-184">เลือก **การตรวจนับตามรอบ** และจากนั้น ในฟิลด์ **รหัสเหตุผล** เลือกรหัสเหตุผลใหม่</span><span class="sxs-lookup"><span data-stu-id="bc936-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="bc936-185">แก้ไขรายการเมนูของอุปกรณ์เคลื่อนที่สำหรับการปรับปรุงเข้าและการปรับปรุงออก</span><span class="sxs-lookup"><span data-stu-id="bc936-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="bc936-186">เลือก **การบริหารคลังสินค้า** \> **ตั้งค่า** \> **อุปกรณ์เคลื่อนที่** \> **รายการเมนูของอุปกรณ์เคลื่อนที่** แล้วจากนั้น เลือก **การปรับปรุงเข้าและออก**</span><span class="sxs-lookup"><span data-stu-id="bc936-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="bc936-187">ตั้งค่าตัวเลือก **ใช้งานที่มีอยู่** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="bc936-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="bc936-188">ในฟิลด์ **กระบวนการสร้างงาน** เลือก **การปรับปรุงเข้า**</span><span class="sxs-lookup"><span data-stu-id="bc936-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="bc936-189">ฟิลด์ต่อไปนี้จะถูกเพิ่มเข้าไปในสินค้าในเมนูของอุปกรณ์เคลื่อนที่ เมื่อมีการเลือก **การปรับปรุงเข้า** หรือ **การปรับปรุงออก** ในระหว่างกระบวนการสร้างงาน:</span><span class="sxs-lookup"><span data-stu-id="bc936-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="bc936-190">รหัสเหตุผลการตรวจนับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bc936-190">Default counting reason code</span></span>
- <span data-ttu-id="bc936-191">แสดงรหัสเหตุผลการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="bc936-191">Display counting reason code</span></span>
- <span data-ttu-id="bc936-192">แก้ไขรหัสเหตุผลการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="bc936-192">Edit counting reason code</span></span>
