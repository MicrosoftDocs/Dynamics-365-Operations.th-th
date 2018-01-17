---
title: "การตั้งค่าอัตราดอกเบี้ยสำหรับรหัสดอกเบี้ย"
description: "รหัสดอกเบี้ยที่ประกอบด้วยการตั้งค่าที่กำหนดเมื่อมีการเรียกเก็บดอกเบี้ยและวิธีที่คำนวณในบัญชีที่พ้นกำหนดชำระ "
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Interest
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 0279050dc8303e9c0cc3d7339c0ce072dd803707
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="9c1e8-103">การตั้งค่าอัตราดอกเบี้ยสำหรับรหัสดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="9c1e8-103">Set up interest rates for an interest code</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9c1e8-104">รหัสดอกเบี้ยที่ประกอบด้วยการตั้งค่าที่กำหนดเมื่อมีการเรียกเก็บดอกเบี้ยและวิธีที่คำนวณในบัญชีที่พ้นกำหนดชำระ </span><span class="sxs-lookup"><span data-stu-id="9c1e8-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="9c1e8-105">คุณสามารถตั้งค่ารหัสดอกเบี้ยเดี่ยว และนำไปใช้กับโพรไฟล์การลงบัญชีลูกค้า รหัสการเรียกเก็บเงิน หรือใช้กับรายการใบแจ้งหนี้โดยเฉพาะได้ </span><span class="sxs-lookup"><span data-stu-id="9c1e8-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="9c1e8-106">เมื่อมีการเปลี่ยนแปลงรายละเอียดรหัสดอกเบี้ย ลักษณะการทำงานทั้งหมดที่ใช้รหัสจะใช้เปลี่ยนแปลงบนธุรกรรมใหม่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9c1e8-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="9c1e8-107">สำหรับแต่ละรหัสดอกเบี้ย คุณสามารถตั้งค่าอัตราสองชนิด:</span><span class="sxs-lookup"><span data-stu-id="9c1e8-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="9c1e8-108">อัตราสำหรับรายได้จากดอกเบี้ย โดยแสดงถึงรายได้ที่จะได้รับจากการคิดค่าธรรมเนียมดอกเบี้ยในใบแจ้งหนี้หรือดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="9c1e8-109">อัตราสำหรับการชำระดอกเบี้ย โดยแสดงถึงต้นทุนที่จ่ายสำหรับดอกเบี้ยในใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="9c1e8-110">อัตราทั้งสองชนิดนี้สามารถอยู่ในเวลาเดียวกัน และในรหัสดอกเบี้ยเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="9c1e8-111">อัตราดอกเบี้ยอาจยึดตามการคำนวณสามชนิด</span><span class="sxs-lookup"><span data-stu-id="9c1e8-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="9c1e8-112">ดอกเบี้ยตามเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="9c1e8-112">Interest by percentage.</span></span>
-   <span data-ttu-id="9c1e8-113">ดอกเบี้ยตามยอด</span><span class="sxs-lookup"><span data-stu-id="9c1e8-113">Interest by amount.</span></span>
-   <span data-ttu-id="9c1e8-114">ดอกเบี้ยตามช่วง ซึ่งส่งผลต่อเปอร์เซ็นต์หรือยอดเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="9c1e8-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="9c1e8-115">เมื่อมีการใช้รหัสดอกเบี้ยเพื่อคำนวณดอกเบี้ย บันทึกดอกเบี้ยแยกจะสร้างขึ้นสำหรับแต่ละอัตราดอกเบี้ยที่มีผลกระทบระหว่างเวลาที่การชำระเงินเกินวันครบกำหนดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9c1e8-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="9c1e8-116">คุณใช้แท็บ **รายได้** บนหน้า **รหัสดอกเบี้ย** เพื่อตั้งค่าอัตราดอกเบี้ยสำหรับดอกเบี้ยที่คุณได้รับโดยการคิดค่าธรรมเนียมดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="9c1e8-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="9c1e8-117">ใช้แท็บ **การชำระเงิน** เพื่อตั้งค่าอัตราดอกเบี้ยสำหรับดอกเบี้ยที่คุณชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="9c1e8-118">อัตราดอกเบี้ยตามเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="9c1e8-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="9c1e8-119">คุณสามารถตั้งค่าอัตราดอกเบี้ยที่คำนวณเปอร์เซ็นต์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="9c1e8-119">You can set up interest rates that calculate a specified percentage.</span></span>

-   <span data-ttu-id="9c1e8-120">ยอดดอกเบี้ยที่ใช้กับสกุลเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9c1e8-120">Interest amount applies to all currencies.</span></span>
-   <span data-ttu-id="9c1e8-121">คุณสามารถป้อนวงเงินยอดเงินดอกเบี้ยที่ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="9c1e8-121">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="9c1e8-122">**เปอร์เซ็นต์** มีการเลือก** **ในฟิลด์ **คำนวณดอกเบี้ยตาม** ในหน้า **ตั้งค่ารหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-122">**Percentage** is selected** **in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="9c1e8-123">ตัวอย่างเช่น ในการตั้งค่ารหัสดอกเบี้ยที่ประเมิณดอกเบี้ยได้ 5 เปอร์เซ็นต์สำหรับทุกๆสองเดือนที่การชำระเงินตามใบแจ้งหนี้เกินวันครบกำหนดของธุรกรรม คุณจะต้องป้อน 2 ในฟิลด์ **คำนวณดอกเบี้ยทุกๆ** และเลือก **เดือน**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="9c1e8-124">อัตราดอกเบี้ยตามยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-124">Interest rates based on amounts</span></span>
<span data-ttu-id="9c1e8-125">คุณสามารถตั้งค่าอัตราดอกเบี้ยที่คำนวณเปอร์เซ็นต์ที่ระบุต่อสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
-   <span data-ttu-id="9c1e8-126">มีการระบุยอดเงินดอกเบี้ยสำหรับแต่ละสกุลเงินในรหัสดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="9c1e8-126">An interest amount is specified for each currency in the interest code.</span></span>
-   <span data-ttu-id="9c1e8-127">คุณสามารถป้อนวงเงินยอดเงินดอกเบี้ยที่ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="9c1e8-127">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="9c1e8-128">**ยอดเงิน** มีการเลือกในฟิลด์ **คำนวณดอกเบี้ยตาม** ในหน้า **ตั้งค่ารหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-128">**Amount **is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="9c1e8-129">ตัวอย่างเช่น ในการตั้งค่ารหัสดอกเบี้ยที่ประเมิณดอกเบี้ยได้ 25.00 สำหรับทุกๆ 20 วัน ที่การชำระเงินตามใบแจ้งหนี้เกินวันครบกำหนดของธุรกรรม คุณจะต้องป้อน 20 ในฟิลด์ **คำนวณดอกเบี้ยทุกๆ** และเลือก **วัน**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="9c1e8-130">อัตราดอกเบี้ยตามช่วง</span><span class="sxs-lookup"><span data-stu-id="9c1e8-130">Interest rates based on ranges</span></span>
<span data-ttu-id="9c1e8-131">คุณสามารถตั้งค่าอัตราดอกเบี้ยที่แตกต่างกันไปขึ้นอยู่กับยอดเงินที่เกินกำหนด จำนวนวันที่จ่ายยอดเงินล่าช้า หรือจำนวนเดือนที่จ่ายยอดเงินล่าช้า</span><span class="sxs-lookup"><span data-stu-id="9c1e8-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="9c1e8-132">คุณสามารถใช้แท็บ **รายได้โดยเรียงตามสกุลเงิน** เพื่อกำหนดการตั้งค่าเฉพาะดอกเบี้ยสำหรับแต่ละสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="9c1e8-133">นี่คือที่ที่คุณจะกำหนดช่วง</span><span class="sxs-lookup"><span data-stu-id="9c1e8-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="9c1e8-134">ใช้ปุ่ม **ช่วง** เพื่อเพิ่มรายการที่แสดงถึงช่วงที่คุณต้องการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="9c1e8-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="9c1e8-135">ค่า **จาก** แสดงจุดเริ่มต้นของช่วงและหมายเลข **มูลค่าดอกเบี้ย** ที่แสดงถึงเปอร์เซ็นต์หรือยอดเงิน โดยขึ้นอยู่กับการเลือกในฟิลด์ **คำนวณดอกเบี้ยตาม** ในหน้า **ตั้งค่ารหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="9c1e8-136">ตัวอย่างที่ 1: ดอกเบี้ยตามช่วง =ยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="9c1e8-137">คุณตั้งค่ารหัสดอกเบี้ยที่ประเมินดอกเบี้ยหนึ่งครั้งทุกสามเดือน ซึ่งการชำระใบแจ้งหนี้เกินวันที่ครบกำหนดของธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="9c1e8-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="9c1e8-138">คุณต้องการคำนวณตามค่าเปอร์เซ็นต์ดอกเบี้ย ตามช่วงยอดเงินขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="9c1e8-139">มูลค่าดอกเบี้ยจะเป็น 1 เปอร์เซ็นต์สำหรับยอดเงินใบแจ้งหนี้จนถึง 1, 000.00, 2 เปอร์เซ็นต์สำหรับยอดเงินจาก 1,001.00 ถึง 5,000.00 และ 3 เปอร์เซ็นต์สำหรับยอดเงินที่มีขนาดมากกว่า 5,000.00</span><span class="sxs-lookup"><span data-stu-id="9c1e8-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="9c1e8-140">คุณตั้งค่าฟิลด์รหัสดอกเบี้ยดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="9c1e8-141">**ชื่อฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-141">**Field name**</span></span>                  | <span data-ttu-id="9c1e8-142">**ค่าฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="9c1e8-143">**รหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-143">**Interest code**</span></span>               | <span data-ttu-id="9c1e8-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="9c1e8-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="9c1e8-145">**คำนวณดอกเบี้ยทุกๆ**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-145">**Calculate interest every**</span></span>    | <span data-ttu-id="9c1e8-146">3/เดือน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-146">3/Month</span></span>         |
| <span data-ttu-id="9c1e8-147">**ดอกเบี้ยตามช่วง**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-147">**Interest by range**</span></span>           | <span data-ttu-id="9c1e8-148">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-148">Amount</span></span>          |
| <span data-ttu-id="9c1e8-149">**คำนวณดอกเบี้ยตาม**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-149">**Calculate interest based on**</span></span> | <span data-ttu-id="9c1e8-150">เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="9c1e8-150">Percentage</span></span>      |

<span data-ttu-id="9c1e8-151">คุณตั้งค่าข้อมูลช่วงดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="9c1e8-152">**ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-152">**From value**</span></span> | <span data-ttu-id="9c1e8-153">**มูลค่าดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="9c1e8-154">0</span><span class="sxs-lookup"><span data-stu-id="9c1e8-154">0</span></span>              | <span data-ttu-id="9c1e8-155">1</span><span class="sxs-lookup"><span data-stu-id="9c1e8-155">1</span></span>                  |
| <span data-ttu-id="9c1e8-156">1,001</span><span class="sxs-lookup"><span data-stu-id="9c1e8-156">1,001</span></span>          | <span data-ttu-id="9c1e8-157">2</span><span class="sxs-lookup"><span data-stu-id="9c1e8-157">2</span></span>                  |
| <span data-ttu-id="9c1e8-158">5,001</span><span class="sxs-lookup"><span data-stu-id="9c1e8-158">5,001</span></span>          | <span data-ttu-id="9c1e8-159">3</span><span class="sxs-lookup"><span data-stu-id="9c1e8-159">3</span></span>                  |

 
## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="9c1e8-160">ตัวอย่างที่ 2: ดอกเบี้ยตามช่วง =วัน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="9c1e8-161">คุณตั้งค่ารหัสดอกเบี้ยที่ประเมินดอกเบี้ยหนึ่งครั้งในทุกๆ 15 วัน ซึ่งการชำระเงินใบแจ้งหนี้เกินวันที่ครบกำหนดของธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="9c1e8-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="9c1e8-162">คุณต้องการคำนวณตามยอดเงินมูลค่าดอกเบี้ย ตามช่วงวันขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="9c1e8-163">มูลค่าดอกเบี้ยจะเป็น 10.00 ต่อ 15 วันระหว่าง 60 วันแรก 15.00 ต่อ 15 วันระหว่างวัน 61 ถึง 90 และ 20.00 ต่อ 15 วัน จากวันที่ 91 และหลังจากนั้น</span><span class="sxs-lookup"><span data-stu-id="9c1e8-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="9c1e8-164">คุณตั้งค่าฟิลด์รหัสดอกเบี้ยดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="9c1e8-165">**ชื่อฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-165">**Field name**</span></span>                  | <span data-ttu-id="9c1e8-166">**ค่าฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="9c1e8-167">**รหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-167">**Interest code**</span></span>               | <span data-ttu-id="9c1e8-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="9c1e8-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="9c1e8-169">**คำนวณดอกเบี้ยทุกๆ**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-169">**Calculate interest every**</span></span>    | <span data-ttu-id="9c1e8-170">15/วัน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-170">15/Day</span></span>          |
| <span data-ttu-id="9c1e8-171">**ดอกเบี้ยตามช่วง**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-171">**Interest by range**</span></span>           | <span data-ttu-id="9c1e8-172">วัน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-172">Days</span></span>            |
| <span data-ttu-id="9c1e8-173">**คำนวณดอกเบี้ยตาม**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-173">**Calculate interest based on**</span></span> | <span data-ttu-id="9c1e8-174">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-174">Amount</span></span>          |

<span data-ttu-id="9c1e8-175">คุณตั้งค่าข้อมูลช่วงดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="9c1e8-176">**ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-176">**From value**</span></span> | <span data-ttu-id="9c1e8-177">**มูลค่าดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="9c1e8-178">0</span><span class="sxs-lookup"><span data-stu-id="9c1e8-178">0</span></span>              | <span data-ttu-id="9c1e8-179">10</span><span class="sxs-lookup"><span data-stu-id="9c1e8-179">10</span></span>                 |
| <span data-ttu-id="9c1e8-180">61</span><span class="sxs-lookup"><span data-stu-id="9c1e8-180">61</span></span>             | <span data-ttu-id="9c1e8-181">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="9c1e8-181">15</span></span>                 |
| <span data-ttu-id="9c1e8-182">91</span><span class="sxs-lookup"><span data-stu-id="9c1e8-182">91</span></span>             | <span data-ttu-id="9c1e8-183">20</span><span class="sxs-lookup"><span data-stu-id="9c1e8-183">20</span></span>                 |

 
## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="9c1e8-184">ตัวอย่างที่ 3: ดอกเบี้ยตามช่วง =เดือน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="9c1e8-185">คุณตั้งค่ารหัสดอกเบี้ยที่ประเมิณดอกเบี้ยหนึ่งครั้งต่อเดือน ซึ่งการชำระเงินใบแจ้งหนี้เกินวันครบกำหนดของธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="9c1e8-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="9c1e8-186">คุณต้องการคำนวณตามค่าเปอร์เซ็นต์ดอกเบี้ย ตามช่วงเดือนขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="9c1e8-187">มูลค่าดอกเบี้ยจะเป็น 1.5 เปอร์เซ็นต์ต่อเดือนสำหรับการพ้นกำหนดสามเดือนแรก 2.0 เปอร์เซ็นต์ต่อเดือนสำหรับสามเดือนที่สอง และ 2.5 เปอร์เซ็นต์ต่อเดือนสำหรับแต่ละเดือนนอกเหนือจากหกเดือนแรก</span><span class="sxs-lookup"><span data-stu-id="9c1e8-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="9c1e8-188">คุณตั้งค่าฟิลด์รหัสดอกเบี้ยดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="9c1e8-189">**ชื่อฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-189">**Field name**</span></span>                  | <span data-ttu-id="9c1e8-190">**ค่าฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="9c1e8-191">**รหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-191">**Interest code**</span></span>               | <span data-ttu-id="9c1e8-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="9c1e8-192">1M%ByMth</span></span>        |
| <span data-ttu-id="9c1e8-193">**คำนวณดอกเบี้ยทุกๆ**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-193">**Calculate interest every**</span></span>    | <span data-ttu-id="9c1e8-194">1/เดือน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-194">1/Month</span></span>         |
| <span data-ttu-id="9c1e8-195">**ดอกเบี้ยตามช่วง**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-195">**Interest by range**</span></span>           | <span data-ttu-id="9c1e8-196">เดือน</span><span class="sxs-lookup"><span data-stu-id="9c1e8-196">Months</span></span>          |
| <span data-ttu-id="9c1e8-197">**คำนวณดอกเบี้ยตาม**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-197">**Calculate interest based on**</span></span> | <span data-ttu-id="9c1e8-198">เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="9c1e8-198">Percentage</span></span>      |

<span data-ttu-id="9c1e8-199">คุณตั้งค่าข้อมูลช่วงดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="9c1e8-200">**ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-200">**From value**</span></span> | <span data-ttu-id="9c1e8-201">**มูลค่าดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="9c1e8-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="9c1e8-202">0</span><span class="sxs-lookup"><span data-stu-id="9c1e8-202">0</span></span>              | <span data-ttu-id="9c1e8-203">1.5</span><span class="sxs-lookup"><span data-stu-id="9c1e8-203">1.5</span></span>                |
| <span data-ttu-id="9c1e8-204">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="9c1e8-204">4</span></span>              | <span data-ttu-id="9c1e8-205">2</span><span class="sxs-lookup"><span data-stu-id="9c1e8-205">2</span></span>                  |
| <span data-ttu-id="9c1e8-206">7</span><span class="sxs-lookup"><span data-stu-id="9c1e8-206">7</span></span>              | <span data-ttu-id="9c1e8-207">2.5</span><span class="sxs-lookup"><span data-stu-id="9c1e8-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="9c1e8-208">เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="9c1e8-208">New versions</span></span>
<span data-ttu-id="9c1e8-209">รหัสดอกเบี้ยคือวันที่มีผลบังคับใช้ </span><span class="sxs-lookup"><span data-stu-id="9c1e8-209">Interest codes are date effective.</span></span> <span data-ttu-id="9c1e8-210">ถ้าคุณต้องการแก้ไขอัตราดอกเบี้ย คุณสามารถสร้าง **เวอร์ชันใหม่** ที่จะมีผลบังคับใช้ ณ วันในอนาคตได้</span><span class="sxs-lookup"><span data-stu-id="9c1e8-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="9c1e8-211">เพื่อดูเวอร์ชันอื่น คุณสามารถใช้ตัวเลือกเมนู **ณ วันที่** เพื่อเลือกวันที่ตัดยอด</span><span class="sxs-lookup"><span data-stu-id="9c1e8-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="9c1e8-212">คุณยังสามารถเลือก **แสดงเรกคอร์ดทั้งหมด** เพื่อดูรหัสดอกเบี้ยทั้งหมดในหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="9c1e8-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>




