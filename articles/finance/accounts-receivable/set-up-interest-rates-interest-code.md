---
title: การตั้งค่าอัตราดอกเบี้ยสำหรับรหัสดอกเบี้ย
description: 'รหัสดอกเบี้ยที่ประกอบด้วยการตั้งค่าที่กำหนดเมื่อมีการเรียกเก็บดอกเบี้ยและวิธีที่คำนวณในบัญชีที่พ้นกำหนดชำระ '
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62868c30d3ff60e51d99c71b743ab0bbb3c87451
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835207"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="4c6d2-103">การตั้งค่าอัตราดอกเบี้ยสำหรับรหัสดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="4c6d2-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c6d2-104">รหัสดอกเบี้ยที่ประกอบด้วยการตั้งค่าที่กำหนดเมื่อมีการเรียกเก็บดอกเบี้ยและวิธีที่คำนวณในบัญชีที่พ้นกำหนดชำระ </span><span class="sxs-lookup"><span data-stu-id="4c6d2-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="4c6d2-105">คุณสามารถตั้งค่ารหัสดอกเบี้ยเดี่ยว และนำไปใช้กับโพรไฟล์การลงบัญชีลูกค้า รหัสการเรียกเก็บเงิน หรือใช้กับรายการใบแจ้งหนี้โดยเฉพาะได้ </span><span class="sxs-lookup"><span data-stu-id="4c6d2-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="4c6d2-106">เมื่อมีการเปลี่ยนแปลงรายละเอียดรหัสดอกเบี้ย ลักษณะการทำงานทั้งหมดที่ใช้รหัสจะใช้เปลี่ยนแปลงบนธุรกรรมใหม่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4c6d2-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="4c6d2-107">สำหรับแต่ละรหัสดอกเบี้ย คุณสามารถตั้งค่าอัตราสองชนิด:</span><span class="sxs-lookup"><span data-stu-id="4c6d2-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="4c6d2-108">อัตราสำหรับรายได้จากดอกเบี้ย โดยแสดงถึงรายได้ที่จะได้รับจากการคิดค่าธรรมเนียมดอกเบี้ยในใบแจ้งหนี้หรือดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="4c6d2-109">อัตราสำหรับการชำระดอกเบี้ย โดยแสดงถึงต้นทุนที่จ่ายสำหรับดอกเบี้ยในใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="4c6d2-110">อัตราทั้งสองชนิดนี้สามารถอยู่ในเวลาเดียวกัน และในรหัสดอกเบี้ยเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="4c6d2-111">อัตราดอกเบี้ยอาจยึดตามการคำนวณสามชนิด</span><span class="sxs-lookup"><span data-stu-id="4c6d2-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="4c6d2-112">ดอกเบี้ยตามเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="4c6d2-112">Interest by percentage.</span></span>
-   <span data-ttu-id="4c6d2-113">ดอกเบี้ยตามยอด</span><span class="sxs-lookup"><span data-stu-id="4c6d2-113">Interest by amount.</span></span>
-   <span data-ttu-id="4c6d2-114">ดอกเบี้ยตามช่วง ซึ่งส่งผลต่อเปอร์เซ็นต์หรือยอดเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="4c6d2-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="4c6d2-115">เมื่อมีการใช้รหัสดอกเบี้ยเพื่อคำนวณดอกเบี้ย บันทึกดอกเบี้ยแยกจะสร้างขึ้นสำหรับแต่ละอัตราดอกเบี้ยที่มีผลกระทบระหว่างเวลาที่การชำระเงินเกินวันครบกำหนดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="4c6d2-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="4c6d2-116">คุณใช้แท็บ **รายได้** บนหน้า **รหัสดอกเบี้ย** เพื่อตั้งค่าอัตราดอกเบี้ยสำหรับดอกเบี้ยที่คุณได้รับโดยการคิดค่าธรรมเนียมดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="4c6d2-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="4c6d2-117">ใช้แท็บ **การชำระเงิน** เพื่อตั้งค่าอัตราดอกเบี้ยสำหรับดอกเบี้ยที่คุณชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="4c6d2-118">อัตราดอกเบี้ยตามเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="4c6d2-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="4c6d2-119">คุณสามารถตั้งค่าอัตราดอกเบี้ยที่คำนวณเปอร์เซ็นต์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4c6d2-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="4c6d2-120">ยอดดอกเบี้ยที่ใช้กับสกุลเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4c6d2-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="4c6d2-121">คุณสามารถป้อนวงเงินยอดเงินดอกเบี้ยที่ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="4c6d2-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="4c6d2-122">**เปอร์เซ็นต์** ได้รับเลือกในฟิลด์ **คำนวณดอกเบี้ยตาม** ในหน้า **ตั้งค่ารหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="4c6d2-123">ตัวอย่างเช่น ในการตั้งค่ารหัสดอกเบี้ยที่ประเมิณดอกเบี้ยได้ 5 เปอร์เซ็นต์สำหรับทุกๆสองเดือนที่การชำระเงินตามใบแจ้งหนี้เกินวันครบกำหนดของธุรกรรม คุณจะต้องป้อน 2 ในฟิลด์ **คำนวณดอกเบี้ยทุกๆ** และเลือก **เดือน**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="4c6d2-124">อัลกอริทึมใหม่ที่จะเพิ่มการคํานวณดอกเบี้ยตั๋วเงินโดยใช้การจัดการลักษณะการงาน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="4c6d2-125">หากต้องการใช้อัลกอริทึมนี้ ให้เปิดใช้งานคุณลักษณะ **(GBL) เพื่อให้สามารถคํานวณดอกเบี้ยต่อวันได้ เป็นเปอร์เซ็นต์ต่อปีหารด้วย 365**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="4c6d2-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะนี้ ดูที่ [ภาพรวมของการจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="4c6d2-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="4c6d2-127">สูตรการคํานวณยอดเงินของดอกเบี้ยตั๋วเงิน คือ:</span><span class="sxs-lookup"><span data-stu-id="4c6d2-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="4c6d2-128">ยอดเงินของดอกเบี้ยตั๋วเงิน = ยอดเงินที่ค้างชำระ \* % ดอกเบี้ยรายปี / 365 \* จํานวนวันล่าช้า</span><span class="sxs-lookup"><span data-stu-id="4c6d2-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="4c6d2-129">คุณลักษณะนี้พร้อมใช้งานในรุ่น 10.0.18 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="4c6d2-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="4c6d2-130">อัตราดอกเบี้ยตามยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-130">Interest rates based on amounts</span></span>
<span data-ttu-id="4c6d2-131">คุณสามารถตั้งค่าอัตราดอกเบี้ยที่คำนวณเปอร์เซ็นต์ที่ระบุต่อสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="4c6d2-132">มีการระบุยอดเงินดอกเบี้ยสำหรับแต่ละสกุลเงินในรหัสดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="4c6d2-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="4c6d2-133">คุณสามารถป้อนวงเงินยอดเงินดอกเบี้ยที่ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="4c6d2-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="4c6d2-134">**ยอดเงิน** มีการเลือกในฟิลด์ **คำนวณดอกเบี้ยตาม** ในหน้า **ตั้งค่ารหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="4c6d2-135">ตัวอย่างเช่น ในการตั้งค่ารหัสดอกเบี้ยที่ประเมิณดอกเบี้ยได้ 25.00 สำหรับทุกๆ 20 วัน ที่การชำระเงินตามใบแจ้งหนี้เกินวันครบกำหนดของธุรกรรม คุณจะต้องป้อน 20 ในฟิลด์ **คำนวณดอกเบี้ยทุกๆ** และเลือก **วัน**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="4c6d2-136">อัตราดอกเบี้ยตามช่วง</span><span class="sxs-lookup"><span data-stu-id="4c6d2-136">Interest rates based on ranges</span></span>
<span data-ttu-id="4c6d2-137">คุณสามารถตั้งค่าอัตราดอกเบี้ยที่แตกต่างกันไปขึ้นอยู่กับยอดเงินที่เกินกำหนด จำนวนวันที่จ่ายยอดเงินล่าช้า หรือจำนวนเดือนที่จ่ายยอดเงินล่าช้า</span><span class="sxs-lookup"><span data-stu-id="4c6d2-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="4c6d2-138">คุณสามารถใช้แท็บ **รายได้โดยเรียงตามสกุลเงิน** เพื่อกำหนดการตั้งค่าเฉพาะดอกเบี้ยสำหรับแต่ละสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="4c6d2-139">นี่คือที่ที่คุณจะกำหนดช่วง</span><span class="sxs-lookup"><span data-stu-id="4c6d2-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="4c6d2-140">ใช้ปุ่ม **ช่วง** เพื่อเพิ่มรายการที่แสดงถึงช่วงที่คุณต้องการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="4c6d2-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="4c6d2-141">ค่า **จาก** แสดงจุดเริ่มต้นของช่วงและหมายเลข **มูลค่าดอกเบี้ย** ที่แสดงถึงเปอร์เซ็นต์หรือยอดเงิน โดยขึ้นอยู่กับการเลือกในฟิลด์ **คำนวณดอกเบี้ยตาม** ในหน้า **ตั้งค่ารหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="4c6d2-142">ตัวอย่างที่ 1: ดอกเบี้ยตามช่วง =ยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="4c6d2-143">คุณตั้งค่ารหัสดอกเบี้ยที่ประเมินดอกเบี้ยหนึ่งครั้งทุกสามเดือน ซึ่งการชำระใบแจ้งหนี้เกินวันที่ครบกำหนดของธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="4c6d2-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="4c6d2-144">คุณต้องการคำนวณตามค่าเปอร์เซ็นต์ดอกเบี้ย ตามช่วงยอดเงินขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="4c6d2-145">มูลค่าดอกเบี้ยจะเป็น 1 เปอร์เซ็นต์สำหรับยอดเงินใบแจ้งหนี้จนถึง 1, 000.00, 2 เปอร์เซ็นต์สำหรับยอดเงินจาก 1,001.00 ถึง 5,000.00 และ 3 เปอร์เซ็นต์สำหรับยอดเงินที่มีขนาดมากกว่า 5,000.00</span><span class="sxs-lookup"><span data-stu-id="4c6d2-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="4c6d2-146">คุณตั้งค่าฟิลด์รหัสดอกเบี้ยดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="4c6d2-147">**ชื่อฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-147">**Field name**</span></span>                  | <span data-ttu-id="4c6d2-148">**ค่าฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="4c6d2-149">**รหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-149">**Interest code**</span></span>               | <span data-ttu-id="4c6d2-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="4c6d2-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="4c6d2-151">**คำนวณดอกเบี้ยทุกๆ**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-151">**Calculate interest every**</span></span>    | <span data-ttu-id="4c6d2-152">3/เดือน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-152">3/Month</span></span>         |
| <span data-ttu-id="4c6d2-153">**ดอกเบี้ยตามช่วง**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-153">**Interest by range**</span></span>           | <span data-ttu-id="4c6d2-154">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-154">Amount</span></span>          |
| <span data-ttu-id="4c6d2-155">**คำนวณดอกเบี้ยตาม**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-155">**Calculate interest based on**</span></span> | <span data-ttu-id="4c6d2-156">เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="4c6d2-156">Percentage</span></span>      |

<span data-ttu-id="4c6d2-157">คุณตั้งค่าข้อมูลช่วงดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="4c6d2-158">**ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-158">**From value**</span></span> | <span data-ttu-id="4c6d2-159">**มูลค่าดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="4c6d2-160">0</span><span class="sxs-lookup"><span data-stu-id="4c6d2-160">0</span></span>              | <span data-ttu-id="4c6d2-161">1</span><span class="sxs-lookup"><span data-stu-id="4c6d2-161">1</span></span>                  |
| <span data-ttu-id="4c6d2-162">1,001</span><span class="sxs-lookup"><span data-stu-id="4c6d2-162">1,001</span></span>          | <span data-ttu-id="4c6d2-163">2</span><span class="sxs-lookup"><span data-stu-id="4c6d2-163">2</span></span>                  |
| <span data-ttu-id="4c6d2-164">5,001</span><span class="sxs-lookup"><span data-stu-id="4c6d2-164">5,001</span></span>          | <span data-ttu-id="4c6d2-165">3</span><span class="sxs-lookup"><span data-stu-id="4c6d2-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="4c6d2-166">ตัวอย่างที่ 2: ดอกเบี้ยตามช่วง =วัน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="4c6d2-167">คุณตั้งค่ารหัสดอกเบี้ยที่ประเมินดอกเบี้ยหนึ่งครั้งในทุกๆ 15 วัน ซึ่งการชำระเงินใบแจ้งหนี้เกินวันที่ครบกำหนดของธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="4c6d2-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="4c6d2-168">คุณต้องการคำนวณตามยอดเงินมูลค่าดอกเบี้ย ตามช่วงวันขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="4c6d2-169">มูลค่าดอกเบี้ยจะเป็น 10.00 ต่อ 15 วันระหว่าง 60 วันแรก 15.00 ต่อ 15 วันระหว่างวัน 61 ถึง 90 และ 20.00 ต่อ 15 วัน จากวันที่ 91 และหลังจากนั้น</span><span class="sxs-lookup"><span data-stu-id="4c6d2-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="4c6d2-170">คุณตั้งค่าฟิลด์รหัสดอกเบี้ยดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="4c6d2-171">**ชื่อฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-171">**Field name**</span></span>                  | <span data-ttu-id="4c6d2-172">**ค่าฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="4c6d2-173">**รหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-173">**Interest code**</span></span>               | <span data-ttu-id="4c6d2-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="4c6d2-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="4c6d2-175">**คำนวณดอกเบี้ยทุกๆ**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-175">**Calculate interest every**</span></span>    | <span data-ttu-id="4c6d2-176">15/วัน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-176">15/Day</span></span>          |
| <span data-ttu-id="4c6d2-177">**ดอกเบี้ยตามช่วง**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-177">**Interest by range**</span></span>           | <span data-ttu-id="4c6d2-178">วัน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-178">Days</span></span>            |
| <span data-ttu-id="4c6d2-179">**คำนวณดอกเบี้ยตาม**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-179">**Calculate interest based on**</span></span> | <span data-ttu-id="4c6d2-180">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-180">Amount</span></span>          |

<span data-ttu-id="4c6d2-181">คุณตั้งค่าข้อมูลช่วงดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="4c6d2-182">**ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-182">**From value**</span></span> | <span data-ttu-id="4c6d2-183">**มูลค่าดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="4c6d2-184">0</span><span class="sxs-lookup"><span data-stu-id="4c6d2-184">0</span></span>              | <span data-ttu-id="4c6d2-185">10</span><span class="sxs-lookup"><span data-stu-id="4c6d2-185">10</span></span>                 |
| <span data-ttu-id="4c6d2-186">61</span><span class="sxs-lookup"><span data-stu-id="4c6d2-186">61</span></span>             | <span data-ttu-id="4c6d2-187">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="4c6d2-187">15</span></span>                 |
| <span data-ttu-id="4c6d2-188">91</span><span class="sxs-lookup"><span data-stu-id="4c6d2-188">91</span></span>             | <span data-ttu-id="4c6d2-189">20</span><span class="sxs-lookup"><span data-stu-id="4c6d2-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="4c6d2-190">ตัวอย่างที่ 3: ดอกเบี้ยตามช่วง =เดือน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="4c6d2-191">คุณตั้งค่ารหัสดอกเบี้ยที่ประเมิณดอกเบี้ยหนึ่งครั้งต่อเดือน ซึ่งการชำระเงินใบแจ้งหนี้เกินวันครบกำหนดของธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="4c6d2-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="4c6d2-192">คุณต้องการคำนวณตามค่าเปอร์เซ็นต์ดอกเบี้ย ตามช่วงเดือนขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="4c6d2-193">มูลค่าดอกเบี้ยจะเป็น 1.5 เปอร์เซ็นต์ต่อเดือนสำหรับการพ้นกำหนดสามเดือนแรก 2.0 เปอร์เซ็นต์ต่อเดือนสำหรับสามเดือนที่สอง และ 2.5 เปอร์เซ็นต์ต่อเดือนสำหรับแต่ละเดือนนอกเหนือจากหกเดือนแรก</span><span class="sxs-lookup"><span data-stu-id="4c6d2-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="4c6d2-194">คุณตั้งค่าฟิลด์รหัสดอกเบี้ยดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="4c6d2-195">**ชื่อฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-195">**Field name**</span></span>                  | <span data-ttu-id="4c6d2-196">**ค่าฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="4c6d2-197">**รหัสดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-197">**Interest code**</span></span>               | <span data-ttu-id="4c6d2-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="4c6d2-198">1M%ByMth</span></span>        |
| <span data-ttu-id="4c6d2-199">**คำนวณดอกเบี้ยทุกๆ**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-199">**Calculate interest every**</span></span>    | <span data-ttu-id="4c6d2-200">1/เดือน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-200">1/Month</span></span>         |
| <span data-ttu-id="4c6d2-201">**ดอกเบี้ยตามช่วง**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-201">**Interest by range**</span></span>           | <span data-ttu-id="4c6d2-202">เดือน</span><span class="sxs-lookup"><span data-stu-id="4c6d2-202">Months</span></span>          |
| <span data-ttu-id="4c6d2-203">**คำนวณดอกเบี้ยตาม**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-203">**Calculate interest based on**</span></span> | <span data-ttu-id="4c6d2-204">เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="4c6d2-204">Percentage</span></span>      |

<span data-ttu-id="4c6d2-205">คุณตั้งค่าข้อมูลช่วงดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="4c6d2-206">**ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-206">**From value**</span></span> | <span data-ttu-id="4c6d2-207">**มูลค่าดอกเบี้ย**</span><span class="sxs-lookup"><span data-stu-id="4c6d2-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="4c6d2-208">0</span><span class="sxs-lookup"><span data-stu-id="4c6d2-208">0</span></span>              | <span data-ttu-id="4c6d2-209">1.5</span><span class="sxs-lookup"><span data-stu-id="4c6d2-209">1.5</span></span>                |
| <span data-ttu-id="4c6d2-210">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4c6d2-210">4</span></span>              | <span data-ttu-id="4c6d2-211">2</span><span class="sxs-lookup"><span data-stu-id="4c6d2-211">2</span></span>                  |
| <span data-ttu-id="4c6d2-212">7</span><span class="sxs-lookup"><span data-stu-id="4c6d2-212">7</span></span>              | <span data-ttu-id="4c6d2-213">2.5</span><span class="sxs-lookup"><span data-stu-id="4c6d2-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="4c6d2-214">เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="4c6d2-214">New versions</span></span>
<span data-ttu-id="4c6d2-215">รหัสดอกเบี้ยคือวันที่มีผลบังคับใช้ </span><span class="sxs-lookup"><span data-stu-id="4c6d2-215">Interest codes are date effective.</span></span> <span data-ttu-id="4c6d2-216">ถ้าคุณต้องการแก้ไขอัตราดอกเบี้ย คุณสามารถสร้าง **เวอร์ชันใหม่** ที่จะมีผลบังคับใช้ ณ วันในอนาคตได้</span><span class="sxs-lookup"><span data-stu-id="4c6d2-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="4c6d2-217">เพื่อดูเวอร์ชันอื่น คุณสามารถใช้ตัวเลือกเมนู **ณ วันที่** เพื่อเลือกวันที่ตัดยอด</span><span class="sxs-lookup"><span data-stu-id="4c6d2-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="4c6d2-218">คุณยังสามารถเลือก **แสดงเรกคอร์ดทั้งหมด** เพื่อดูรหัสดอกเบี้ยทั้งหมดในหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="4c6d2-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
