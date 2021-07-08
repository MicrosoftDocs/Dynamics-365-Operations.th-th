---
title: การปัดเศษทศนิยมของปริมาณการอัปเดตจริงไม่ถูกต้อง
description: เมื่อคุณสร้างบันทึกการจัดส่ง สินค้าขาออกมีปริมาณซึ่งไม่ตรงกับตำแหน่งทศนิยมที่ระบุในหน่วย
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248807"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="0cbd3-103">การปัดเศษทศนิยมของปริมาณการอัปเดตจริงไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0cbd3-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="0cbd3-104">รหัสข้อผิดพลาด: SYS19589</span><span class="sxs-lookup"><span data-stu-id="0cbd3-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="0cbd3-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="0cbd3-105">Symptoms</span></span>

<span data-ttu-id="0cbd3-106">เมื่อคุณสร้างบันทึกการจัดส่ง สินค้าขาออกมีปริมาณซึ่งไม่ตรงกับตำแหน่งทศนิยมที่ระบุในหน่วย</span><span class="sxs-lookup"><span data-stu-id="0cbd3-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="0cbd3-107">เมื่อคุณพยายามสร้างบันทึกการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0cbd3-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="0cbd3-108">การปัดทศนิยมของปริมาณการอัพเดตจริงในหน่วย %1 ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0cbd3-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="0cbd3-109">ดังนั้นคุณจึงไม่สามารถสร้างบันทึกการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="0cbd3-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="0cbd3-110">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="0cbd3-110">Cause</span></span>

<span data-ttu-id="0cbd3-111">ระบบจะประเมินว่าการปัดเศษทศนิยมของปริมาณการจัดส่งตรงกับตำแหน่งทศนิยมที่กําหนดไว้ของหน่วยการจัดส่งหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0cbd3-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="0cbd3-112">เมื่อระบบปัดเศษปริมาณการจัดส่งเป็นตำแหน่งทศนิยมที่ระบุ หากพบว่าปริมาณการจัดส่งที่ปัดเศษไม่ตรงกับปริมาณการจัดส่งจริง คุณไม่สามารถสร้างบันทึกการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="0cbd3-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="0cbd3-113">ตัวอย่างเช่น ปัญหานี้อาจเกิดขึ้นถ้าปริมาณการขายคือ 1.75 กิโลกรัม (กก.) แต่ตำแหน่งทศนิยมมีการตั้งค่าเป็น *1*</span><span class="sxs-lookup"><span data-stu-id="0cbd3-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="0cbd3-114">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="0cbd3-114">Resolution</span></span>

<span data-ttu-id="0cbd3-115">สินค้าหรือการจัดส่งอยู่ในสถานะที่การสร้างบันทึกการจัดส่งล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="0cbd3-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="0cbd3-116">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำหนึ่งในงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0cbd3-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="0cbd3-117">ตรวจทานรายการสินค้าของคุณ และปรับปรุงเพื่อให้แน่ใจว่าสามารถแปลงปริมาณทั้งหมดโดยไม่มีปัญหาการปัดเศษทษนิยมและปัญหาการปัดเศษใดๆ</span><span class="sxs-lookup"><span data-stu-id="0cbd3-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="0cbd3-118">ตรวจทานรายการสินค้าของคุณ และปรับปรุงเพื่อให้แน่ใจว่าหน่วยและปริมาณสอดคล้องกับตําแหน่งทศนิยมของหน่วย</span><span class="sxs-lookup"><span data-stu-id="0cbd3-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="0cbd3-119">ตรวจทานรายการสินค้าของคุณ และปรับปรุงเพื่อให้แน่ใจว่าสามารถแปลงปริมาณทั้งหมดโดยไม่มีปัญหาการปัดเศษทษนิยมและปัญหาการปัดเศษใดๆ</span><span class="sxs-lookup"><span data-stu-id="0cbd3-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="0cbd3-120">ใช้กระบวนงานต่อไปนี้เพื่อตรวจทานรายการสินค้าของคุณ และปรับปรุงเพื่อให้แน่ใจว่าสามารถแปลงปริมาณทั้งหมดโดยไม่มีปัญหาการปัดเศษทษนิยมและปัญหาการปัดเศษใดๆ</span><span class="sxs-lookup"><span data-stu-id="0cbd3-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="0cbd3-121">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0cbd3-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0cbd3-122">เลือกสินค้าที่บันทึกการจัดส่งไม่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="0cbd3-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0cbd3-123">ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **กลับรายการ** ให้เลือก **กลับรายการการยืนยันการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="0cbd3-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="0cbd3-124">บนแท็บ  **รายการสินค้า** ให้เลือกรายการสินค้าของสินค้าที่ก่อให้เกิดปัญหา</span><span class="sxs-lookup"><span data-stu-id="0cbd3-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="0cbd3-125">เลือก **ลดปริมาณที่เบิกสินค้า** เพื่อปรับปรุงปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="0cbd3-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="0cbd3-126">บนแท็บ  **รายละเอียดของรายการ** ให้เลือก **ใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="0cbd3-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="0cbd3-127">ตั้งค่าฟิลด์ **ปริมาณ** ให้กับปริมาณที่เบิกสินค้า (นั่นคือค่าของฟิลด์ **ปริมาณที่สร้างขึ้นของงาน**) เพื่อให้การสร้างบันทึกการจัดส่งสามารถดำเนินการต่อได้</span><span class="sxs-lookup"><span data-stu-id="0cbd3-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="0cbd3-128">ตรวจทานรายการสินค้าของคุณ และปรับปรุงเพื่อให้แน่ใจว่าหน่วยและปริมาณสอดคล้องกับตําแหน่งทศนิยมของหน่วย</span><span class="sxs-lookup"><span data-stu-id="0cbd3-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="0cbd3-129">ใช้กระบวนงานต่อไปนี้เพื่อตรวจทานรายการสินค้าของคุณ และปรับปรุงเพื่อให้แน่ใจว่าหน่วยและปริมาณสอดคล้องกับตําแหน่งทศนิยมของหน่วย</span><span class="sxs-lookup"><span data-stu-id="0cbd3-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="0cbd3-130">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0cbd3-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0cbd3-131">เลือกสินค้าที่บันทึกการจัดส่งไม่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="0cbd3-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0cbd3-132">บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้าของสินค้าที่ก่อให้เกิดปัญหา</span><span class="sxs-lookup"><span data-stu-id="0cbd3-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="0cbd3-133">บันทึกค่าของฟิลด์ **ปริมาณ** และ **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="0cbd3-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="0cbd3-134">ไปที่ **การจัดการองค์กร \> หน่วย \> หน่วย**</span><span class="sxs-lookup"><span data-stu-id="0cbd3-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="0cbd3-135">เลือกหน่วยที่บันทึกการจัดส่งไม่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="0cbd3-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0cbd3-136">ปรับปรุงค่าของฟิลด์ **ตำแหน่งทศนิยม** ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="0cbd3-136">Adjust the value of the **Decimal precision** field as required.</span></span>
