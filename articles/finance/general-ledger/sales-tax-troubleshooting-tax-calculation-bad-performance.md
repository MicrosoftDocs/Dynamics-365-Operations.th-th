---
title: ประสิทธิภาพการคํานวณภาษีมีผลกระทบต่อธุรกรรม
description: หัวข้อนี้มีข้อมูลการแก้ไขปัญหาที่เกี่ยวข้องกับประสิทธิภาพการคํานวณภาษีและผลกระทบต่อธุรกรรม
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947719"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="3abcd-103">ประสิทธิภาพการคํานวณภาษีมีผลกระทบต่อธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3abcd-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3abcd-104">ในบางครั้ง ธุรกรรมจะได้รับผลกระทบจากปัญหาด้านประสิทธิภาพการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="3abcd-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="3abcd-105">เมื่อต้องการแก้ไขปัญหานี้ ให้ปฏิบัติตามขั้นตอนในส่วนต่อไปนี้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="3abcd-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="3abcd-106">ตรวจสอบจำนวนรายการธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3abcd-106">Review the transaction line count</span></span>

<span data-ttu-id="3abcd-107">ระบุว่าธุรกรรมมีรายการจํานวนมาก (ตัวอย่างเช่น มากกว่าหนึ่งร้อย) หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3abcd-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="3abcd-108">หากไม่ เลื่อนไปที่ส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3abcd-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="3abcd-109">ถ้าธุรกรรมมีมากกว่าหนึ่งรายการ ให้หน่วงเวลาการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="3abcd-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="3abcd-110">สำหรับข้อมูลเพิ่มเติม ให้ดู [เปิดใช้งานการคํานวณภาษีล่าช้าในสมุดรายวัน](enable-delayed-tax-calculation.md)</span><span class="sxs-lookup"><span data-stu-id="3abcd-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="3abcd-111">จากนั้น คุณสามารถระบุว่าเป็นไปตามเงื่อนไขใดเงื่อนไขหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3abcd-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="3abcd-112">มีธุรกรรมการนําเข้าจากไฟล์ขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="3abcd-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="3abcd-113">รอบเวลาหลายรอบจะประมวลผลการคํานวณภาษีธุรกรรมในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="3abcd-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="3abcd-114">ธุรกรรมมีหลายรายการ และมีการอัปเดตมุมมองในเวลาจริง</span><span class="sxs-lookup"><span data-stu-id="3abcd-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="3abcd-115">ตัวอย่างเช่น ฟิลด์ **ยอดภาษีขายที่คํานวณได้** ในหน้า **สมุดรายวันทั่วไป** จะมีการอัปเดตในเวลาจริงเมื่อมีการเปลี่ยนแปลงฟิลด์ของบรรทัด</span><span class="sxs-lookup"><span data-stu-id="3abcd-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="3abcd-116">[![ฟิลด์จํานวนเงินภาษีขายที่คํานวณได้ในหน้าใบสำคัญสมุดรายวัน](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="3abcd-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="3abcd-117">หากเป็นไปตามเงื่อนไขใดเงื่อนไขหนึ่ง ให้หน่วงเวลาการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="3abcd-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="3abcd-118">ตรวจทานสแต็คการเรียก</span><span class="sxs-lookup"><span data-stu-id="3abcd-118">Review the call stack</span></span>

<span data-ttu-id="3abcd-119">ทบทวนสแต็คการเรียกเพื่อระบุว่าจะเรียกการคํานวณภาษีหลายครั้งหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3abcd-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="3abcd-120">หากไม่ เลื่อนไปที่ส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3abcd-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="3abcd-121">ถ้าเรียกสแต็คการเรียกหลายครั้ง ให้ปฏิบัติตามขั้นตอนเหล่านี้เพื่อลดเวลาการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="3abcd-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="3abcd-122">ถ้าสมุดรายวันพิจารณาว่าเป็นธุรกรรมแล้ว ให้หน่วงเวลาการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="3abcd-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="3abcd-123">สำหรับข้อมูลเพิ่มเติม ให้ดู [เปิดใช้งานการคํานวณภาษีล่าช้าในสมุดรายวัน](enable-delayed-tax-calculation.md)</span><span class="sxs-lookup"><span data-stu-id="3abcd-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="3abcd-124">ถ้าธุรกรรมเป็นใบสั่งซื้อ และรุ่นของโปรแกรมประยุกต์หลัง 10.0.15 คุณสามารถเลื่อนเวลาการคํานวณภาษีได้จนกว่าจะมีการคํานวณครั้งสุดท้ายโดยเปิดใช้งานเที่ยวบิน **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** ได้</span><span class="sxs-lookup"><span data-stu-id="3abcd-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="3abcd-125">ตรวจทานเส้นเวลาสแต็คการเรียก</span><span class="sxs-lookup"><span data-stu-id="3abcd-125">Review the call stack timeline</span></span>

<span data-ttu-id="3abcd-126">ทบทวนเส้นเวลาสแต็คการเรียก เพื่อตัดสินว่ามีปัญหาต่อไปนี้อยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3abcd-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="3abcd-127">หากสินค้าเหล่านั้นเปิดใช้งานเที่ยวบินของ **TaxUncommittedDoSollateSolFsoling** เพื่อแก้ปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="3abcd-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="3abcd-128">ธุรกรรมจะส่งผลให้ระบบหยุดตอบสนองจนกว่ารอบเวลาจะสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="3abcd-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="3abcd-129">ดังนั้น ธุรกรรมจึงไม่สามารถคํานวณผลภาษีได้</span><span class="sxs-lookup"><span data-stu-id="3abcd-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="3abcd-130">ภาพประกอบต่อไปนี้จะแสดงกล่องข้อความ "รอบเวลาสิ้นสุด" ที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="3abcd-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="3abcd-131">[![ข้อความสิ้นสุดรอบเวลา](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="3abcd-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="3abcd-132">วิธีการ **TaxUncommitted** จะใช้เวลามากกว่าวิธีการอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="3abcd-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="3abcd-133">ตัวอย่างเช่น ในภาพประกอบต่อไปนี้ วิธีการ **TaxUncommitted::updateTaxUncommitted()** จะใช้เวลา 43,347.42 วินาที แต่วิธีการอื่น ๆ จะใช้เวลา 0.09 วินาที</span><span class="sxs-lookup"><span data-stu-id="3abcd-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="3abcd-134">[![ระยะเวลาของวิธีการ](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="3abcd-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="3abcd-135">การปรับแต่งและการคํานวณภาษีที่เรียก</span><span class="sxs-lookup"><span data-stu-id="3abcd-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="3abcd-136">เมื่อคุณกำหนดเอง อย่าเรียกการคํานวณภาษีในวิธีการ **insert()** หรือ **update()** ของแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="3abcd-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="3abcd-137">ควรเรียกการคํานวณภาษีที่ระดับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3abcd-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="3abcd-138">ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3abcd-138">Determine whether customization exists</span></span>

<span data-ttu-id="3abcd-139">หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ไม่พบปัญหา ให้ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3abcd-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="3abcd-140">ถ้าไม่มีการเลือกเองอยู่ ให้สร้างคำขอบริการของ Microsoft เพื่อขอความช่วยเหลือเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3abcd-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
