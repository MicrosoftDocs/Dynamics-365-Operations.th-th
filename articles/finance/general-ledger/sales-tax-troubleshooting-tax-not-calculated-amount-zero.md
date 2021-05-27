---
title: ไม่ได้คํานวณภาษีหรือยอดเงินภาษีเป็นศูนย์
description: หัวข้อนี้มีข้อมูลการแก้ไขปัญหาที่สามารถช่วยเมื่อยอดเงินภาษีเป็น 0 (ศูนย์) หรือไม่ได้คํานวณภาษี
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020126"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="4958f-103">ไม่ได้คํานวณภาษีหรือยอดเงินภาษีเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="4958f-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4958f-104">ธุรกรรมอาจมียอดเงินรายการที่ไม่ใช่ 0 (ศูนย์) แต่ภาษีไม่ได้คํานวณหรือยอดภาษีที่คํานวณได้คือ 0</span><span class="sxs-lookup"><span data-stu-id="4958f-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="4958f-105">เมื่อต้องการแก้ไขปัญหานี้ ให้ปฏิบัติตามขั้นตอนในส่วนต่อไปนี้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="4958f-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="4958f-106">ตรวจสอบว่ามีการเลือกรหัสภาษีโดยธุรกรรมอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4958f-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="4958f-107">ถ้าธุรกรรมไม่เลือกรหัสภาษีที่ถูกต้อง หรือถ้าไม่ได้เลือกรหัสภาษีใด ๆ ภาษีจะไม่ได้รับการคํานวณ</span><span class="sxs-lookup"><span data-stu-id="4958f-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="4958f-108">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตรวจสอบว่ามีการเลือกรหัสภาษีโดยธุรกรรมอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4958f-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="4958f-109">บนบรรทัดธุรกรรม บนแท็บด่วน **รายละเอียดของรายการ** บนแท็บ **การตั้งค่า** ในส่วน **ภาษีขาย** ตรวจสอบว่ามีการเลือกรหัสภาษีโดยธุรกรรมอย่างถูกต้องในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** และ **กลุ่มภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="4958f-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="4958f-110">ถ้าไม่ได้เลือกกลุ่มภาษีที่ถูกต้อง ให้เลือกกลุ่มภาษีนั้น</span><span class="sxs-lookup"><span data-stu-id="4958f-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="4958f-111">[![กลุ่มภาษีขายสินค้าและฟิลด์กลุ่มภาษีขาย](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="4958f-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="4958f-112">ไปที่ **ภาษี** \> **ภาษีทางอ้อม** \> **ภาษีขาย** \> **กลุ่มภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="4958f-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="4958f-113">เลือกกลุ่มภาษีขายที่เหมาะสม จากนั้นบนแท็บด่วน **การตั้งค่า** ให้บันทึกรหัสภาษีในฟิลด์ **รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="4958f-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="4958f-114">[![หน้ากลุ่มภาษีขาย](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="4958f-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="4958f-115">ไปที่ **ภาษี** \> **ภาษีทางอ้อม** \> **ภาษีขาย** \> **กลุ่มภาษีขายตามประเภทสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4958f-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="4958f-116">เลือกกลุ่มภาษีขายตามประเภทสินค้าที่เหมาะสม จากนั้นบนแท็บด่วน **การตั้งค่า** ให้ตรวจสอบว่ารหัสภาษีในฟิลด์ **รหัสภาษีขาย** ตรงกับรหัสภาษีของกลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="4958f-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="4958f-117">[![หน้ากลุ่มภาษีขายตามประเภทสินค้า](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="4958f-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="4958f-118">หากรหัสภาษีไม่ตรงกัน ให้อัปเดตรหัสภาษีขายของกลุ่มใดกลุ่มหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4958f-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="4958f-119">ตรวจสอบว่ารหัสภาษีที่เลือกไม่ได้รับยกเว้นและมีค่าอัตราภาษีที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4958f-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="4958f-120">ถ้ารหัสภาษีได้รับการยกเว้น หรือถ้าอัตราภาษีเป็น 0 (ศูนย์) ผลการคํานวณภาษีจะเป็น 0</span><span class="sxs-lookup"><span data-stu-id="4958f-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="4958f-121">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อระบุว่ารหัสภาษีที่เลือกได้รับยกเว้นหรือไม่ และตรวจสอบว่ามีการใช้อัตราภาษีที่ถูกต้องกับรหัสดังกล่าวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4958f-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="4958f-122">ไปที่ **ภาษี** \> **ภาษีทางอ้อม** \> **ภาษีขาย** \> **กลุ่มภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="4958f-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="4958f-123">เลือกกลุ่มภาษีขายที่เหมาะสม จากนั้นบนแท็บด่วน **การตั้งค่า** ให้ตรวจสอบว่าไม่ได้เลือกกล่องกาเครื่องหมาย **ยกเว้น**</span><span class="sxs-lookup"><span data-stu-id="4958f-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="4958f-124">ถ้าเลือกไว้ ให้ล้าง</span><span class="sxs-lookup"><span data-stu-id="4958f-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="4958f-125">[![กล่องกาเครื่องหมายยกเว้นในหน้ากลุ่มภาษีขาย](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="4958f-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="4958f-126">ไปที่ **ภาษี** \> **ภาษีทางอ้อม** \> **ภาษีขาย** \> **รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="4958f-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="4958f-127">เลือกรหัสภาษีขายที่เหมาะสม แล้วตรวจสอบว่าค่าอัตราภาษีในฟิลด์ **ค่า** ไม่ใช่ 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="4958f-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="4958f-128">ถ้าเป็น 0 ให้อัปเดตฟิลด์เพื่อให้มีการตั้งค่าเป็นอัตราภาษีที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4958f-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="4958f-129">[![ฟิลด์ค่าบนหน้าค่าของรหัสภาษีขาย](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="4958f-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="4958f-130">ระบุว่าศูนย์เป็นยอดภาษีที่ถูกต้องหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4958f-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="4958f-131">ในบางสถานการณ์ ยอดเงินภาษี 0 (ศูนย์) ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4958f-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="4958f-132">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อระบุว่า 0 เป็นจํานวนเงินภาษีที่ถูกต้องในธุรกรรมของคุณหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4958f-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="4958f-133">ไปที่ **บัญชีแยกประเภททั่วไป** \> **การตั้งค่าบัญชีแยกประเภท** \> **พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="4958f-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="4958f-134">บนแท็บ **ภาษีขาย** ในฟิลด์ **วิธีการคํานวณ** ให้ตรวจสอบว่ามีการเลือก **ผลรวม** ไว้</span><span class="sxs-lookup"><span data-stu-id="4958f-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="4958f-135">[![ฟิลด์วิธีการคํานวณในหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="4958f-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="4958f-136">ไปที่ **ภาษี** \> **ภาษีทางอ้อม** \> **ภาษีขาย** \> **รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="4958f-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="4958f-137">เลือกรหัสภาษีขายที่เหมาะสม เลือก **การคํานวณ** \> **ฐานกำไรเบื้องต้น** และตรวจสอบว่ามีการตั้งค่าฐานกําไรเป็น **ยอดเงินสุทธิของยอดดุลใบแจ้งหนี้** หรือ **ยอดรวมใบแจ้งหนี้ รวมยอดภาษีขายอื่น ๆ**</span><span class="sxs-lookup"><span data-stu-id="4958f-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="4958f-138">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยอดรวมของใบแจ้งหนี้รวมยอดภาษีขายอื่น](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts)</span><span class="sxs-lookup"><span data-stu-id="4958f-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="4958f-139">ถ้าตั้งค่าที่ถูกต้องในขั้นตอนที่ 2 และ 4 ให้ระบุว่ายอดรวมของธุรกรรมเป็น 0 (ศูนย์) หรือไม่</span><span class="sxs-lookup"><span data-stu-id="4958f-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="4958f-140">ถ้ายอดเงินรวมเป็น 0 ยอดเงินภาษี 0 จะเป็นผลที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="4958f-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="4958f-141">เนื่องจากการคํานวณภาษีจะขึ้นอยู่กับยอดเงินรวมของยอดดุลใบแจ้งหนี้ และยอดเงินนี้ไม่เป็นไปตามรายการ ดังนั้นยอดภาษี 0 จะถูกปันส่วนไปยังแต่ละรายการหลังจากการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="4958f-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="4958f-142">ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="4958f-142">Determine whether customization exists</span></span>

<span data-ttu-id="4958f-143">หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ไม่พบปัญหา ให้ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="4958f-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="4958f-144">ถ้าไม่มีการเลือกเองอยู่ ให้สร้างคำขอบริการของ Microsoft เพื่อขอความช่วยเหลือเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4958f-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
