---
title: การตั้งค่าการจัดการสินเชื่อ
description: หัวข้อนี้จะอธิบายเกี่ยวกับการตั้งค่าที่จำเป็นสำหรับการจัดการเครดิต
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c54c74af6f2c1be9aedfa792d0676d1165fb0ab8
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015419"
---
# <a name="credit-management-setup"></a><span data-ttu-id="17a2d-103">การตั้งค่าการจัดการสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="17a2d-103">Credit management setup</span></span> 

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="credit-management-workflows"></a><span data-ttu-id="17a2d-104">ลำดับงานการจัดการสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="17a2d-104">Credit management workflows</span></span>

<span data-ttu-id="17a2d-105">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> การตั้งค่า \> ลำดับงานการจัดการสินเชื่อ** เพื่อกำหนดลำดับงานที่จะใช้ในการจัดการการปรับปรุงวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="17a2d-105">Go to **Credit and collections \> Setup \> Credit management workflows** to define the workflows that are used to manage credit limit adjustments.</span></span>

- <span data-ttu-id="17a2d-106">คุณสามารถสร้างลำดับงานที่ช่วยให้คุณสามารถอนุมัติชุดงานของการปรับปรุงวงเงินสินเชื่อผ่านการอนุมัติเดียว</span><span class="sxs-lookup"><span data-stu-id="17a2d-106">You can create a workflow that lets you approve a batch of credit limits adjustments through a single approval.</span></span>
- <span data-ttu-id="17a2d-107">คุณสามารถเพิ่มลำดับงานที่ระดับรายการ เพื่อให้สามารถอนุมัติการปรับปรุงวงเงินสินเชื่อทีละรายการได้</span><span class="sxs-lookup"><span data-stu-id="17a2d-107">You can add a workflow at the line level, so that credit limit adjustments can be approved individually.</span></span>
- <span data-ttu-id="17a2d-108">คุณสามารถสร้างลำดับงานการนำออกใช้ที่กระบวนการผลิตระงับสำหรับกระบวนการลำดับงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="17a2d-108">You can create a release workflow that automatically routes holds to a workflow process.</span></span>

## <a name="blocking-rules"></a><span data-ttu-id="17a2d-109">กฎการบล็อค</span><span class="sxs-lookup"><span data-stu-id="17a2d-109">Blocking rules</span></span>

### <a name="ranking-payment-terms"></a><span data-ttu-id="17a2d-110">การจัดอันดับเงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="17a2d-110">Ranking payment terms</span></span>

<span data-ttu-id="17a2d-111">คุณสามารถระงับใบสั่งขายได้ ถ้าเงื่อนไขการชำระเงินในใบสั่งไม่ตรงกับเงื่อนไขการชำระเงินเริ่มต้นสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-111">You can put a sales order on hold if the payment terms on the order don't match the default payment terms for the customer.</span></span> <span data-ttu-id="17a2d-112">อย่างไรก็ตาม ในบางครั้งเงื่อนไขการชำระเงินจะแตกต่างกันไป แต่มีลักษณะคล้ายคลึงกันเพียงพอที่คุณไม่ต้องการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="17a2d-112">However, sometimes the payment terms differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="17a2d-113">คุณสามารถจัดอันดับเงื่อนไขการชำระเงิน เพื่อให้บางส่วนของเงื่อนไขการชำระเงินมีอันดับเดียวกัน ในขณะที่รายการอื่นมีระดับสูงกว่าหรือต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="17a2d-113">You can rank payment terms so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="17a2d-114">ถ้าการจัดอันดับสำหรับเงื่อนไขการชำระเงินใช้งานอยู่ ใบสั่งขายจะถูกระงับ ถ้าเงื่อนไขการชำระเงินในใบสั่งมีอันดับสูงกว่าเงื่อนไขการชำระเงินเริ่มต้นสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-114">If the rankings for payment terms are active, the sales orders will be put on hold if the payment terms on the order have a higher rank than the default payment terms for the customer.</span></span>

### <a name="ranking-settlement-discounts"></a><span data-ttu-id="17a2d-115">การจัดอันดับส่วนลดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="17a2d-115">Ranking settlement discounts</span></span>

<span data-ttu-id="17a2d-116">คุณสามารถระงับใบสั่งขายได้ ถ้าส่วนลดเงินสดในใบสั่งไม่ตรงกับส่วนลดเงินสดเริ่มต้นสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-116">You can put a sales order on hold if the cash discount on the order doesn't match the default cash discount for the customer.</span></span> <span data-ttu-id="17a2d-117">อย่างไรก็ตาม ในบางครั้งส่วนลดเงินสดจะแตกต่างกันไป แต่มีลักษณะคล้ายคลึงกันเพียงพอที่คุณไม่ต้องการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="17a2d-117">However, sometimes the cash discounts differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="17a2d-118">คุณสามารถจัดอันดับส่วนลดเงินสด เพื่อให้บางส่วนมีอันดับเดียวกัน ในขณะที่รายการอื่นมีระดับสูงกว่าหรือต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="17a2d-118">You can rank cash discounts so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="17a2d-119">ถ้าการจัดอันดับสำหรับเงื่อนไขการชำระเงินใช้งานอยู่ ใบสั่งขายจะถูกระงับ ถ้าส่วนลดเงินสดในใบสั่งมีอันดับสูงกว่าส่วนลดเงินสดเริ่มต้นสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-119">If rankings for settlement discounts are active, the sales orders will be put on hold if the cash discount on the order has a higher rank than the default cash discount for the customer.</span></span>

## <a name="reasons"></a><span data-ttu-id="17a2d-120">เหตุผล</span><span class="sxs-lookup"><span data-stu-id="17a2d-120">Reasons</span></span>

<span data-ttu-id="17a2d-121">มีการใช้เหตุผลหลายชนิดในการจัดการเครดิต:</span><span class="sxs-lookup"><span data-stu-id="17a2d-121">Several types of reasons are used in Credit management:</span></span>

- <span data-ttu-id="17a2d-122">เหตุผลการระงับบ่งชี้ว่าทำไมใบสั่งขายจึงถูกระงับไว้</span><span class="sxs-lookup"><span data-stu-id="17a2d-122">Hold reasons indicate why a sales order was put on hold.</span></span>
- <span data-ttu-id="17a2d-123">เหตุผลการนำออกใช้จะได้รับการกำหนดให้กับใบสั่ง เมื่อมีการนำออกใช้จากการระงับ</span><span class="sxs-lookup"><span data-stu-id="17a2d-123">Release reasons are assigned to an order when it's released from hold.</span></span>
- <span data-ttu-id="17a2d-124">เหตุผลของสถานะบ่งชี้ว่าทำไมสถานะของบัญชีได้รับการกำหนดให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-124">Status reasons indicate why an account status was assigned to a customer.</span></span>

<span data-ttu-id="17a2d-125">คุณสามารถตั้งค่าเหตุผลบนหน้า **เหตุผลการจัดการเครดิต** (**การจัดการเครดิต \> การตั้งค่า \> การจัดการเครดิต \> เหตุผลของการจัดการเครดิต**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-125">You can set up reasons on the **Credit management reasons** page (**Credit management \> Setup \> Credit management \> Credit management reasons**).</span></span>

1. <span data-ttu-id="17a2d-126">ในฟิลด์ **ชนิดของเหตุผล** ให้เลือกชนิดของเหตุผล: **ระงับ** **การนำออกใช้** หรือ **สถานะ**</span><span class="sxs-lookup"><span data-stu-id="17a2d-126">In the **Reason type** field, select the type of reason: **Hold**, **Release**, or **Status**.</span></span>
2. <span data-ttu-id="17a2d-127">ในฟิลด์ **เหตุผล** ป้อนชื่อสำหรับเหตุผล</span><span class="sxs-lookup"><span data-stu-id="17a2d-127">In the **Reason** field, enter a name for the reason.</span></span>
3. <span data-ttu-id="17a2d-128">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบายของรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="17a2d-128">In the **Description** field, enter a description of the reason code.</span></span>

## <a name="credit-management-groups"></a><span data-ttu-id="17a2d-129">กลุ่มการจัดการสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="17a2d-129">Credit management groups</span></span>

<span data-ttu-id="17a2d-130">กลุ่มการจัดการเครดิตถูกใช้ในการระบุลูกค้าหรือกลุ่มของลูกค้าที่มีคุณสมบัติการจัดการเครดิตเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="17a2d-130">Credit management groups are used to identify customers or groups of customers that have the same credit management properties.</span></span> <span data-ttu-id="17a2d-131">ตัวอย่างเช่น คุณสามารถใช้กลุ่มการจัดการเครดิตเพื่อกำหนดกฎการบล็อคและการจัดการเครดิตของข้อยกเว้นสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-131">For example, credit management groups can be used to determine the blocking and exclusion credit management rules for customers.</span></span>

<span data-ttu-id="17a2d-132">คุณสามารถสร้างกลุ่มการจัดการเครดิตบนหน้า **กลุ่มการจัดการเครดิต** (**การจัดการเครดิต \> การตั้งค่า > การตั้งค่ากลุ่ม \> กลุ่มการจัดการเครดิต**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-132">You can create credit management groups on the **Credit management groups** page (**Credit management \> Setup> Groups setup \> Credit management groups**).</span></span>

1. <span data-ttu-id="17a2d-133">เลือก **สร้าง** เพื่อสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="17a2d-133">Select **New** to create a line.</span></span>
2. <span data-ttu-id="17a2d-134">ป้อนรหัสสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="17a2d-134">Enter an ID for the group.</span></span> <span data-ttu-id="17a2d-135">รหัสสามารถมีอักขระได้มากถึง 10 อักขระ</span><span class="sxs-lookup"><span data-stu-id="17a2d-135">The ID can have up to 10 characters.</span></span>
3. <span data-ttu-id="17a2d-136">ในฟิลด์ **คำอธิบาย** ให้ป้อนชื่อสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="17a2d-136">In the **Description** field, enter a name for the group.</span></span> <span data-ttu-id="17a2d-137">ชื่อสามารถมีอักขระได้มากถึง 60 อักขระ</span><span class="sxs-lookup"><span data-stu-id="17a2d-137">The name can have up to 60 characters.</span></span>

<span data-ttu-id="17a2d-138">กลุ่มการจัดการเครดิตจะถูกกำหนดให้กับลูกค้าบน FastTab **สินเชื่อและการเรียกเก็บเงิน** ของหน้า **ลูกค้าทั้งหมด** (**บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-138">The credit management group is assigned to a customer on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

## <a name="account-statuses"></a><span data-ttu-id="17a2d-139">สถานะบัญชี</span><span class="sxs-lookup"><span data-stu-id="17a2d-139">Account statuses</span></span>

<span data-ttu-id="17a2d-140">คุณสามารถสร้างสถานะบัญชีเพื่อระบุสถานะเครดิตของบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-140">You can create account statuses to identify the credit standing of a customer account.</span></span> <span data-ttu-id="17a2d-141">คุณสามารถกำหนดสถานะและผลที่เกิดขึ้นกับกระบวนการออกใบแจ้งหนี้และการจัดส่งสินค้าที่ระงับ</span><span class="sxs-lookup"><span data-stu-id="17a2d-141">You can define a status and its effect on the invoicing and delivery on-hold processes.</span></span> <span data-ttu-id="17a2d-142">นอกจากนี้ ยังสามารถใช้สถานะของบัญชีเพื่อกำหนดกฎการบล็อคสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-142">Account statuses can also be used to determine blocking rules for a customer.</span></span>

<span data-ttu-id="17a2d-143">คุณสามารถสร้างสถานะของบัญชีในหน้า **สถานะของบัญชี** (**การจัดการเครดิต \> การตั้งค่า > การตั้งค่ากลุ่ม \> สถานะบัญชี**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-143">You can create account statuses on the **Account statuses** page (**Credit management \> Setup> Groups setup \> Account statuses**).</span></span>

1. <span data-ttu-id="17a2d-144">เพิ่มสถานะของบัญชี และป้อนคำอธิบายที่แสดงถึงสถานะเครดิตสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-144">Add an account status, and enter a description that represents the credit standing for a customer.</span></span> <span data-ttu-id="17a2d-145">ตัวอย่างเช่น ใช้ **ปกติ** เพื่อบ่งชี้ว่าลูกค้าอยู่ในสถานะที่ดี และใบสั่งที่เปิดค้างอยู่อยู่ภายใต้การประมวลผลการจัดการเครดิตมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="17a2d-145">For example, use **Normal** to indicate that a customer is in good standing and open orders are subject to standard credit management processing.</span></span>
2. <span data-ttu-id="17a2d-146">ในฟิลด์ **การออกใบแจ้งหนี้** และ **การระงับการจัดส่ง** ให้เลือกชนิดของการระงับที่ควรเกิดขึ้นสำหรับลูกค้าที่มีสถานะบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="17a2d-146">In the **Invoicing** and **Delivery on Hold** fields, select the type of hold that should occur for customers who have this account status.</span></span> <span data-ttu-id="17a2d-147">คุณสามารถระงับการประมวลผลทั้งหมด ค้างไว้เฉพาะการประมวลผลใบแจ้งหนี้ หรือไม่ระงับการประมวลผลเมื่อมีการใช้กฎวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="17a2d-147">You can hold all processing, hold only invoice processing, or hold no processing when the credit limit rules are applied.</span></span>

## <a name="scoring-groups"></a><span data-ttu-id="17a2d-148">กลุ่มการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="17a2d-148">Scoring groups</span></span>

<span data-ttu-id="17a2d-149">คุณสามารถตั้งค่ากลุ่มการให้คะแนนเพื่อกำหนดปัจจัยความเสี่ยงและเงื่อนไขที่ใช้ในการวัด</span><span class="sxs-lookup"><span data-stu-id="17a2d-149">You can set up scoring groups to define risk factors and the criteria that are used to measure them.</span></span> <span data-ttu-id="17a2d-150">เมื่อมีการใช้ข้อมูลเกี่ยวกับลูกค้ากับกลุ่มการให้คะแนน คะแนนจะถูกคำนวณสำหรับตัวคูณความเสี่ยงแต่ละรายการและใช้ในการวางลูกค้าในกลุ่มความเสี่ยง</span><span class="sxs-lookup"><span data-stu-id="17a2d-150">When information about a customer is applied to a scoring group, a score is calculated for each risk factor and used to put the customer in a risk group.</span></span> <span data-ttu-id="17a2d-151">คุณสามารถใช้กลุ่มความเสี่ยงเพื่อระบุความน่าเชื่อถือของผู้ถือบัตรเครดิตและคำนวณวงเงินสินเชื่ออัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="17a2d-151">The risk group can be used to identify credit worthiness and calculate automatic credit limits.</span></span>

<span data-ttu-id="17a2d-152">คุณสามารถสร้างกลุ่มการให้คะแนนในหน้า **กลุ่มการให้คะแนน** (**การจัดการเครดิต \> การตั้งค่า \> การตั้งค่าความเสี่ยง \> กลุ่มการให้คะแนน**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-152">You can create scoring groups on the **Scoring groups** page (**Credit management \> Setup \> Risk setup \> Scoring groups**).</span></span>

1. <span data-ttu-id="17a2d-153">สร้างกลุ่มการให้คะแนน และป้อนชื่อสำหรับกลุ่มนั้น</span><span class="sxs-lookup"><span data-stu-id="17a2d-153">Create a scoring group, and enter a name for it.</span></span>
2. <span data-ttu-id="17a2d-154">ป้อนคำอธิบายเพื่ออธิบายกลุ่มการให้คะแนนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="17a2d-154">Enter a description to further describe the scoring group.</span></span>
3. <span data-ttu-id="17a2d-155">เลือกชนิดของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="17a2d-155">Select a group type.</span></span> <span data-ttu-id="17a2d-156">มีชนิดของธุรกรรมที่กำหนดไว้ล่วงหน้าแปดชนิด</span><span class="sxs-lookup"><span data-stu-id="17a2d-156">There are eight predefined types.</span></span> <span data-ttu-id="17a2d-157">นอกจากนี้ คุณยังสามารถเลือก **ผู้ใช้ที่กำหนด** เพื่อกำหนดชนิดกลุ่มที่เหมาะสมกับองค์กรของคุณได้ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="17a2d-157">You can also select **User defined** to define a group type that's better suited to your organization.</span></span>
4. <span data-ttu-id="17a2d-158">เลือกชนิดคะแนนเพื่อกำหนดว่ากลุ่มการให้คะแนนคำนวณคะแนนความเสี่ยงอย่างไร</span><span class="sxs-lookup"><span data-stu-id="17a2d-158">Select a score type to define how the scoring group calculates the risk score.</span></span> <span data-ttu-id="17a2d-159">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17a2d-159">The following options are available:</span></span>

    - <span data-ttu-id="17a2d-160">**ช่วง** – ใช้ตัวเลือกนี้เพื่อกำหนดช่วงของค่าที่ควรใช้ในการคำนวณคะแนน</span><span class="sxs-lookup"><span data-stu-id="17a2d-160">**Range** – Use this option to define a range of values that should be used to calculate a score.</span></span>
    - <span data-ttu-id="17a2d-161">**ผู้ใช้ที่กำหนด** – ใช้ตัวเลือกนี้เพื่อกำหนดรายการของค่าที่ควรใช้สำหรับคะแนนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="17a2d-161">**User defined** – Use this option to manually define a list of values that should be used for the score.</span></span>

5. <span data-ttu-id="17a2d-162">ถ้าคุณเลือก **ช่วง** เป็นชนิดของคะแนน ให้เพิ่มรายการเพื่อกำหนดช่วงของค่าและคะแนนที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="17a2d-162">If you selected **Range** as the score type, add lines to define the range of values and the corresponding scores.</span></span>

    1. <span data-ttu-id="17a2d-163">ในฟิลด์ **ค่าเริ่มต้น** ให้ระบุค่าต่ำสุดในช่วง</span><span class="sxs-lookup"><span data-stu-id="17a2d-163">In the **From value** field, specify the lowest value in the range.</span></span>
    2. <span data-ttu-id="17a2d-164">ในฟิลด์ **ค่าสิ้นสุด** ให้ระบุค่าสูงสุดในช่วง</span><span class="sxs-lookup"><span data-stu-id="17a2d-164">In the **To value** field, specify the highest value in the range.</span></span>
    3. <span data-ttu-id="17a2d-165">ในฟิลด์ **คะแนน** ให้ป้อนคะแนนที่ควรถูกกำหนด เมื่อค่าที่ระบุอยู่ในช่วง "เริ่มต้น"/"สิ้นสุด"</span><span class="sxs-lookup"><span data-stu-id="17a2d-165">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

    <span data-ttu-id="17a2d-166">ถ้าคุณเลือก **ผู้ใช้ที่กำหนด** เป็นชนิดของคะแนน ให้เพิ่มรายการเพื่อกำหนดค่าผู้ใช้ที่กำหนดและคะแนนที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="17a2d-166">If you selected **User defined** as the score type, add lines to define the user-defined values and the corresponding scores.</span></span>

    1. <span data-ttu-id="17a2d-167">ในฟิลด์ **ค่า** ให้ป้อนค่าที่ผู้ใช้ที่กำหนดซึ่งควรระบุจากข้อมูลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-167">In the **Value** field, enter the user-defined value that should be provided from the customer information.</span></span>
    2. <span data-ttu-id="17a2d-168">ในฟิลด์ **คะแนน** ให้ป้อนคะแนนที่ควรถูกกำหนด เมื่อค่าที่ระบุอยู่ในช่วง "เริ่มต้น"/"สิ้นสุด"</span><span class="sxs-lookup"><span data-stu-id="17a2d-168">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

## <a name="risk-assessments"></a><span data-ttu-id="17a2d-169">การประเมินความเสี่ยง</span><span class="sxs-lookup"><span data-stu-id="17a2d-169">Risk assessments</span></span>

<span data-ttu-id="17a2d-170">คุณสามารถกำหนดการประเมินความเสี่ยงที่สามารถกำหนดให้กับลูกค้าได้ตามคะแนนความเสี่ยงของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="17a2d-170">You can define risk assessments that can be assigned to customers, based on their risk score.</span></span> <span data-ttu-id="17a2d-171">มีการคำนวณคะแนนความเสี่ยงโดยการเปรียบเทียบข้อมูลลูกค้ากับกลุ่มการให้คะแนนแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="17a2d-171">A risk score is calculated by comparing customer information to each scoring group.</span></span> <span data-ttu-id="17a2d-172">คะแนนจะถูกรวม และจะมีการเปรียบเทียบคะแนนรวมกับค่าในการตั้งค่ากลุ่มความเสี่ยงเพื่อระบุกลุ่มความเสี่ยงที่ลูกค้าเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="17a2d-172">The scores are summed, and the total score is compared to the values in the risk group setup to identify the risk group that the customer belongs to.</span></span> <span data-ttu-id="17a2d-173">จากนั้น จะมีการใช้คะแนนของกลุ่มความเสี่ยงเพื่อกำหนดการบล็อคการจัดการเครดิตและกฎข้อยกเว้นสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="17a2d-173">The risk group score is then used to define credit management blocking and exclusion rules for the customer.</span></span>

<span data-ttu-id="17a2d-174">คุณสามารถตั้งค่ากลุ่มความเสี่ยงในหน้า **การประเมินความเสี่ยง** (**การจัดการเครดิต \> การตั้งค่า \> การตั้งค่าความเสี่ยง \> การประเมินความเสี่ยง**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-174">You can set up risk groups on the **Risk assessments** page (**Credit management \> Setup \> Risk setup \> Risk assessments**).</span></span>

1. <span data-ttu-id="17a2d-175">ป้อนรหัสกลุ่มความเสี่ยง</span><span class="sxs-lookup"><span data-stu-id="17a2d-175">Enter a risk group ID.</span></span>
2. <span data-ttu-id="17a2d-176">ป้อนคำอธิบายเพื่ออธิบายกลุ่มความเสี่ยงเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="17a2d-176">Enter a description to further explain the risk group.</span></span>
3. <span data-ttu-id="17a2d-177">ป้อนช่วงของคะแนนที่ใช้เพื่อกำหนดว่าลูกค้ารายใดเป็นสมาชิกของกลุ่มความเสี่ยง</span><span class="sxs-lookup"><span data-stu-id="17a2d-177">Enter a range of scores that is used to determine which customers belong to the risk group.</span></span>
4. <span data-ttu-id="17a2d-178">เลือกตัวบ่งชี้กลุ่มความเสี่ยงเพื่อระบุสัญลักษณ์ที่แสดงถึงกลุ่มความเสี่ยง</span><span class="sxs-lookup"><span data-stu-id="17a2d-178">Select a risk group indicator to specify the symbol that represents the risk group.</span></span>

## <a name="guaranteeinsurance-types"></a><span data-ttu-id="17a2d-179">ชนิดของการค้ำประกัน/การประกันภัย</span><span class="sxs-lookup"><span data-stu-id="17a2d-179">Guarantee/insurance types</span></span>

<span data-ttu-id="17a2d-180">คุณสามารถตั้งค่าชนิดการค้ำประกัน/การประกันภัยบนหน้า **ชนิดการค้ำประกัน/การประกันภัย** (**การจัดการเครดิต \> การตั้งค่า \> การตั้งค่าการค้ำประกัน/การประกันภัย \> ชนิดการค้ำประกัน/การประกันภัย**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-180">You can set up guarantee/insurance types on the **Guarantee/insurance types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Guarantee/insurance types**).</span></span>

1. <span data-ttu-id="17a2d-181">ป้อนชนิดของการค้ำประกันหรือการประกันภัยที่ระบุชื่อของผู้ค้ำประกันหรือนายหน้าประกันภัย</span><span class="sxs-lookup"><span data-stu-id="17a2d-181">Enter a guarantee or insurance type that identifies the name of the guarantor or insurance broker.</span></span>
2. <span data-ttu-id="17a2d-182">ป้อนคำอธิบายเพื่ออธิบายผู้ค้ำประกัน/นายหน้าประกันภัย</span><span class="sxs-lookup"><span data-stu-id="17a2d-182">Enter a description to describe the guarantor/insurance broker.</span></span>

## <a name="coverage-types"></a><span data-ttu-id="17a2d-183">ชนิดความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="17a2d-183">Coverage types</span></span>

<span data-ttu-id="17a2d-184">ชนิดความครอบคลุมสามารถใช้เพื่อจัดประเภทกรมธรรม์ประกันภัยเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="17a2d-184">Coverage types can be used to further classify insurance policies.</span></span> <span data-ttu-id="17a2d-185">ไม่สามารถใช้ได้กับการค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="17a2d-185">They can't be used with guarantees.</span></span>

<span data-ttu-id="17a2d-186">คุณสามารถเพิ่มชนิดความครอบคลุมในหน้า **ชนิดความครอบคลุม** (**การจัดการเครดิต \> การตั้งค่า \> การตั้งค่าการค้ำประกัน/การประกันภัย \> ชนิดความครอบคลุม**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-186">You can add coverage types on the **Coverage types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Coverage types**).</span></span>

1. <span data-ttu-id="17a2d-187">ป้อนชนิดความครอบคลุมเพื่อระบุชนิดของความครอบคลุมที่ควรจะเพิ่มเป็นการประกันภัยหรือการค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="17a2d-187">Enter a coverage type to identify the type of coverage that should be added as insurance or a guarantee.</span></span>
2. <span data-ttu-id="17a2d-188">ป้อนคำอธิบายเพื่ออธิบายชนิดความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="17a2d-188">Enter a description to describe of the coverage type.</span></span>

## <a name="automatic-credit-limits"></a><span data-ttu-id="17a2d-189">วงเงินสินเชื่ออัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="17a2d-189">Automatic credit limits</span></span>

<span data-ttu-id="17a2d-190">คุณสามารถสร้างเกณฑ์สำหรับวงเงินสินเชื่ออัตโนมัติบนหน้า **วงเงินสินเชื่ออัตโนมัติ** (**การจัดการเครดิต \> การตั้งค่า \> ตั้งค่าความเสี่ยง \> วงเงินสินเชื่ออัตโนมัติ**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-190">You can create criteria for automatic credit limits on the **Automatic credit limits** page (**Credit management \> Setup \> Risk setup \> Automatic credit limits**).</span></span>

1. <span data-ttu-id="17a2d-191">เลือกกลุ่มความเสี่ยงที่ควรกำหนดวงเงินสินเชื่ออัตโนมัติให้</span><span class="sxs-lookup"><span data-stu-id="17a2d-191">Select a risk group that the automatic credit limit should be assigned to.</span></span>
2. <span data-ttu-id="17a2d-192">เลือกสกุลเงินสำหรับวงเงินสินเชื่ออัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="17a2d-192">Select the currency for the automatic credit limit.</span></span> <span data-ttu-id="17a2d-193">คุณสามารถสร้างวงเงินสินเชื่ออัตโนมัติที่หลากหลายในสกุลเงินที่แตกต่างกันสำหรับกลุ่มความเสี่ยงเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="17a2d-193">You can create multiple automatic credit limits in different currencies for the same risk group.</span></span>
3. <span data-ttu-id="17a2d-194">ป้อนยอดเงินรายได้ที่แสดงถึงรายได้ของบริษัทสูงสุดที่สามารถใช้สำหรับวงเงินสินเชื่ออัตโนมัตินี้</span><span class="sxs-lookup"><span data-stu-id="17a2d-194">Enter the revenue amount that represents the maximum company revenue that can be used for this automatic credit limit.</span></span> <span data-ttu-id="17a2d-195">เมื่อมีการสร้างวงเงินสินเชื่อย อดเงินรายได้จะถูกเปรียบเทียบกับมูลค่ารายได้ที่พบในหน้า **การเงิน** (**บัญชีลูกหนี้ \> ลูกค้าทั้งหมด \> เลือกลูกค้า \> ทั่วไป \> สถิติ \> การเงิน**)</span><span class="sxs-lookup"><span data-stu-id="17a2d-195">When credit limits are created, the revenue amount is compared to a revenue value that is found on the **Financials** page (**Accounts receivable \> All customers \> Select a customer \> General \> Statistics \> Financial**).</span></span> <span data-ttu-id="17a2d-196">ระบบจะใช้ค่าล่าสุดในส่วน **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="17a2d-196">The system uses the latest value in the **Overview** section.</span></span>

<span data-ttu-id="17a2d-197">ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มรายการที่แสดงถึงวงเงินสินเชื่อที่จะถูกสร้างขึ้นตามเงื่อนไขที่เลือก</span><span class="sxs-lookup"><span data-stu-id="17a2d-197">Follow these steps to add lines that represent the credit limit that will be generated based on the selected criteria.</span></span>

1. <span data-ttu-id="17a2d-198">เลือกกลุ่มการให้คะแนนซึ่งกำหนดข้อมูลลูกค้าที่ควรใช้ในการคำนวณวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="17a2d-198">Select the scoring group that defines the customer information that should be used to calculate the credit limit.</span></span>
2. <span data-ttu-id="17a2d-199">เลือกตัวดำเนินการเปรียบเทียบที่กำหนดวิธีการที่ควรประเมินข้อมูลกลุ่มการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="17a2d-199">Select the comparison operator that defines how the scoring group information should be evaluated.</span></span>
3. <span data-ttu-id="17a2d-200">ป้อนค่าที่ควรจะเปรียบเทียบกับค่าที่ระบุไว้สำหรับกลุ่มการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="17a2d-200">Enter the value that should be compared to the value that is specified for the scoring group.</span></span>
4. <span data-ttu-id="17a2d-201">ป้อนวงเงินสินเชื่อที่ควรถูกกำหนด ถ้าข้อมูลลูกค้าตรงกับค่าที่ระบุไว้สำหรับกลุ่มการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="17a2d-201">Enter the credit limit that should be assigned if the customer information matches the value that is specified for the scoring group.</span></span> <span data-ttu-id="17a2d-202">ตัวอย่างเช่น คุณสร้างวงเงินสินเชื่ออัตโนมัติสำหรับกลุ่มการให้คะแนน **ต่ำ**</span><span class="sxs-lookup"><span data-stu-id="17a2d-202">For example, you create an automatic credit limit for the **Low** scoring group.</span></span> <span data-ttu-id="17a2d-203">ถ้าปีในธุรกิจเป็นหนึ่งในกลุ่มการให้คะแนน คุณสามารถกำหนดหนึ่งรายการที่กำหนดวงเงินสินเชื่อเป็น 100,000 ถ้าลูกค้าได้อยู่ในธุรกิจนานห้าปี และอีกรายการหนึ่งที่กำหนดวงเงินสินเชื่อเป็น 200,000 ถ้าลูกค้าอยู่ในธุรกิจเป็นเวลา 10 ปี</span><span class="sxs-lookup"><span data-stu-id="17a2d-203">If the years in business is one of the scoring groups, you can define one line that assigns a 100,000 credit limit if the customer has been in business five years and another line that assigns a 200,000 credit limit if the customer has been in business for 10 years.</span></span>
