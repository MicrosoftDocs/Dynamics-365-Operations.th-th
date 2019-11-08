---
title: การคำนวณภาษีขายสำหรับรายการสมุดรายวันทั่วไป
description: หัวข้อนี้จะอธิบายถึงวิธีการคำนวณภาษีขายสำหรับบัญชีชนิดต่าง ๆ (ผู้จัดจำหน่าย ลูกค้า บัญชีแยกประเภท และโครงการ) ในรายการสมุดรายวันทั่วไป
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dd1df355d39065d6959915cc916987d3c58b15a6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570205"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="8248d-103">การคำนวณภาษีขายสำหรับรายการสมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8248d-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="8248d-104">หัวข้อนี้จะอธิบายถึงวิธีการคำนวณภาษีขายสำหรับบัญชีชนิดต่าง ๆ (ผู้จัดจำหน่าย ลูกค้า บัญชีแยกประเภท และโครงการ) ในรายการสมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8248d-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="8248d-105">กระบวนการสามารถแบ่งออกเป็นสามขั้นตอนดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8248d-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="8248d-106">กำหนดทิศทางภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="8248d-107">กำหนดยอดภาษีขายที่จะจัดเก็บตารางภาษีขายชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="8248d-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="8248d-108">กำหนดยอดเงินภาษีขายและบัญชีในใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="8248d-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="8248d-109">กำหนดทิศทางภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-109">Determine the sales tax direction</span></span>

<span data-ttu-id="8248d-110">วิธีการกำหนดทิศทางภาษีขายจะขึ้นอยู่กับชนิดของบัญชีในใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="8248d-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="8248d-111">ทิศทางภาษีขายจะขึ้นอยู่กับชุดของชนิดบัญชีและรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="8248d-112">ส่วนต่อไปนี้เป็นไปได้ในรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8248d-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="8248d-113">ชนิดบัญชีเป็นโครงการ</span><span class="sxs-lookup"><span data-stu-id="8248d-113">Account type is Project</span></span>

<span data-ttu-id="8248d-114">ถ้าใบสำคัญมีรายการสมุดรายวันที่ชนิดบัญชีเป็น **โครงการ** รายการสมุดรายวันทั้งหมดในใบสำคัญจะใช้คำสั่งภาษีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8248d-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="8248d-115">ภาพประกอบต่อไปนี้แสดงกฎ</span><span class="sxs-lookup"><span data-stu-id="8248d-115">The following illustration shows the rule.</span></span> <span data-ttu-id="8248d-116">เนื้อหาต่อไปนี้จะแสดงคำสั่งภาษีที่เป็นไปได้สำหรับบัญชีโครงการ</span><span class="sxs-lookup"><span data-stu-id="8248d-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="8248d-117">•   หากรหัสภาษีขายเป็นภาษีนำเข้า ทิศทางของภาษีขายจะเป็นภาษีนำเข้า</span><span class="sxs-lookup"><span data-stu-id="8248d-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="8248d-118">•   หากรหัสภาษีขายเป็นภาษีที่ได้รับการยกเว้น ทิศทางของภาษีขายจะเป็นการซื้อแบบปลอดภาษี</span><span class="sxs-lookup"><span data-stu-id="8248d-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="8248d-119">•   หากรหัสภาษีขายเป็นภาษีระหว่างบริษัท ทิศทางของภาษีขายจะเป็นเจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8248d-120">•   หากรหัสภาษีขายเป็นการเก็บภาษีย้อนกลับ ทิศทางของภาษีขายจะเป็นเจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8248d-121">มิฉะนั้น ทิศทางของภาษีขายจะเป็นลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="8248d-122">แผนภาพต่อไปนี้แสดงกฎแบบกราฟิก</span><span class="sxs-lookup"><span data-stu-id="8248d-122">The following diagram illustrates the rule graphically.</span></span>

![ความเป็นไปได้ของคำสั่งภาษีสำหรับบัญชีโครงการ](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="8248d-124">ชนิดบัญชีเป็นผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8248d-124">Account type is Vendor</span></span>

<span data-ttu-id="8248d-125">ถ้าใบสำคัญมีรายการสมุดรายวันที่ชนิดบัญชีเป็น **ผู้จัดจำหน่าย** รายการสมุดรายวันทั้งหมดในใบสำคัญจะใช้คำสั่งภาษีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8248d-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="8248d-126">เนื้อหาต่อไปนี้จะแสดงทิศทางภาษีที่เป็นไปได้สำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8248d-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="8248d-127">•   หากรหัสภาษีขายเป็นภาษีที่ได้รับการยกเว้น ทิศทางของภาษีขายจะเป็นการซื้อแบบปลอดภาษี</span><span class="sxs-lookup"><span data-stu-id="8248d-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="8248d-128">•   หากรหัสภาษีขายเป็นภาษีระหว่างบริษัท ทิศทางของภาษีขายจะเป็นลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="8248d-129">•   หากรหัสภาษีขายเป็นการเก็บภาษีย้อนกลับ ทิศทางของภาษีขายจะเป็นลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="8248d-130">มิฉะนั้น ทิศทางของภาษีขายจะเป็นเจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8248d-131">แผนภาพต่อไปนี้แสดงกฎแบบกราฟิก</span><span class="sxs-lookup"><span data-stu-id="8248d-131">The following diagram illustrates the rule graphically.</span></span>

![ความเป็นไปได้ของคำสั่งภาษีสำหรับบัญชีผู้จัดจำหน่าย](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="8248d-133">ชนิดบัญชีเป็นลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8248d-133">Account type is Customer</span></span>

<span data-ttu-id="8248d-134">ถ้าใบสำคัญมีรายการสมุดรายวันที่ชนิดบัญชีเป็น **ลูกค้า** รายการสมุดรายวันทั้งหมดในใบสำคัญจะใช้คำสั่งภาษีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8248d-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="8248d-135">เนื้อหาต่อไปนี้จะแสดงคำสั่งภาษีที่เป็นไปได้สำหรับบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8248d-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="8248d-136">•   หากรหัสภาษีขายเป็นภาษีนำเข้า ทิศทางของภาษีขายจะเป็นภาษีนำเข้า</span><span class="sxs-lookup"><span data-stu-id="8248d-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="8248d-137">•   หากรหัสภาษีขายเป็นภาษีที่ได้รับการยกเว้น ทิศทางของภาษีขายจะเป็นการซื้อแบบปลอดภาษี</span><span class="sxs-lookup"><span data-stu-id="8248d-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="8248d-138">•   หากรหัสภาษีขายเป็นภาษีระหว่างบริษัท ทิศทางของภาษีขายจะเป็นเจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8248d-139">•   หากรหัสภาษีขายเป็นการเก็บภาษีย้อนกลับ ทิศทางของภาษีขายจะเป็นเจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8248d-140">มิฉะนั้น ทิศทางของภาษีขายจะเป็นลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="8248d-141">แผนภาพต่อไปนี้แสดงกฎแบบกราฟิก</span><span class="sxs-lookup"><span data-stu-id="8248d-141">The following diagram illustrates the rule graphically.</span></span>

![ความเป็นไปได้ของคำสั่งภาษีสำหรับบัญชีลูกค้า](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="8248d-143">ชนิดบัญชีเป็นบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="8248d-143">Account type is Ledger</span></span>

<span data-ttu-id="8248d-144">ภาพประกอบต่อไปนี้แสดงกฎที่ใช้ เมื่อใบสำคัญมีเฉพาะรายการสมุดประจำวันที่มีบัญชีชนิด **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="8248d-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="8248d-145">เนื้อหาต่อไปนี้จะแสดงทิศทางภาษีที่เป็นไปได้สำหรับบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="8248d-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="8248d-146">•   หากรหัสภาษีขายเป็นภาษีนำเข้า ทิศทางของภาษีขายจะเป็นภาษีนำเข้า</span><span class="sxs-lookup"><span data-stu-id="8248d-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="8248d-147">•   หากรหัสภาษีขายเป็นภาษีที่ได้รับการยกเว้น ทิศทางของภาษีขายจะเป็นการซื้อแบบปลอดภาษี</span><span class="sxs-lookup"><span data-stu-id="8248d-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="8248d-148">มิฉะนั้น หากยอดเงินในสมุดรายวันเป็นเดบิต (ค่าบวก) คำสั่งภาษีขายจะเป็นแบบลูกหนี้ภาษีขาย หากยอดเงินในสมุดรายวันเป็นเครดิต (ลบ) คำสั่งภาษีขายจะเป็นแบบเจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8248d-149">แผนภาพต่อไปนี้แสดงกฎแบบกราฟิก</span><span class="sxs-lookup"><span data-stu-id="8248d-149">The following diagram illustrates the rule graphically.</span></span>

![ความเป็นไปได้ของคำสั่งภาษีสำหรับบัญชีแยกประเภท](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="8248d-151">แทนที่ทิศทางภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-151">Override the sales tax direction</span></span>

<span data-ttu-id="8248d-152">คุณสามารถแทนที่คำสั่งภาษีขายได้ เมื่อใบสำคัญมีเฉพาะรายการที่ชนิดบัญชีเป็น **บัญชีแยกประเภท** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8248d-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="8248d-153">ไปที่ **บัญชีแยกประเภททั่วไป \> ผังบัญชี \> บัญชี \> บัญชีหลัก** หลังจากนั้นให้เลือกแท็บด่วน **แทนที่นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="8248d-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="8248d-154">กำหนดยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-154">Determine the sales tax amount</span></span>

<span data-ttu-id="8248d-155">ในหัวข้อนี้จะอธิบายวิธีการคำนวณเครื่องหมายของยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-155">This section describes how the sales tax amount sign is calculated.</span></span>

![หน้าธุรกรรมภาษีขาย](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="8248d-157">ตารางต่อไปนี้แสดงกฎทั่วไปสำหรับการกำหนดเครื่องหมายของยอดภาษีขายในตารางภาษีขายชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="8248d-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="8248d-158">ยอดเงินในรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8248d-158">Journal line amount</span></span> | <span data-ttu-id="8248d-159">ทิศทางของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-159">Sales tax direction</span></span>  | <span data-ttu-id="8248d-160">เครื่องหมายยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="8248d-161">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-161">Positive</span></span>            | <span data-ttu-id="8248d-162">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-162">Sales Tax Receivable</span></span> | <span data-ttu-id="8248d-163">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-163">Positive</span></span>              |
| <span data-ttu-id="8248d-164">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-164">Positive</span></span>            | <span data-ttu-id="8248d-165">เจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-165">Sales Tax Payable</span></span>    | <span data-ttu-id="8248d-166">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-166">Negative</span></span>              |
| <span data-ttu-id="8248d-167">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-167">Negative</span></span>            | <span data-ttu-id="8248d-168">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-168">Sales Tax Receivable</span></span> | <span data-ttu-id="8248d-169">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-169">Negative</span></span>              |
| <span data-ttu-id="8248d-170">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-170">Negative</span></span>            | <span data-ttu-id="8248d-171">เจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-171">Sales Tax Payable</span></span>    | <span data-ttu-id="8248d-172">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-172">Positive</span></span>              |

<span data-ttu-id="8248d-173">มีกฎพิเศษสำหรับใบสำคัญที่มีเฉพาะรายการ **โครงการ** หรือ **บัญชีแยกประเภท** เมื่อมีการเลือกกลุ่มภาษีขายหรือกลุ่มภาษีขายตามรายการ **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="8248d-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="8248d-174">กฎนี้ควบคุมโดยการเปิดใช้งานลักษณะการทำงานการคำนวณภาษีขายอิสระสำหรับสมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8248d-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="8248d-175">เมื่อปิดใช้งานคุณลักษณะนี้ ยอดภาษีของรายการ **บัญชีแยกประเภท** จะใช้ทิศทาง เดบิต/เครดิต ของรายการ **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="8248d-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="8248d-176">เมื่อปิดใช้งานคุณลักษณะนี้ ยอดภาษีของรายการ **บัญชีแยกประเภท** จะใช้ทิศทาง เดบิต/เครดิต ของตัวเอง</span><span class="sxs-lookup"><span data-stu-id="8248d-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="8248d-177">ตารางต่อไปนี้จะแสดงกฎสำหรับแต่ละสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="8248d-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="8248d-178">**กฎเมื่อคุณลักษณะถูกเปิด**</span><span class="sxs-lookup"><span data-stu-id="8248d-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="8248d-179">ยอดเงินในรายการสมุดรายวันสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="8248d-179">Journal line amount of project</span></span> | <span data-ttu-id="8248d-180">ทิศทางของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-180">Sales tax direction</span></span>  | <span data-ttu-id="8248d-181">เครื่องหมายยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="8248d-182">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-182">Positive</span></span>                       | <span data-ttu-id="8248d-183">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-183">Sales Tax Receivable</span></span> | <span data-ttu-id="8248d-184">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-184">Positive</span></span>              |
| <span data-ttu-id="8248d-185">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-185">Negative</span></span>                       | <span data-ttu-id="8248d-186">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-186">Sales Tax Receivable</span></span> | <span data-ttu-id="8248d-187">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-187">Negative</span></span>              |

<span data-ttu-id="8248d-188">**กฎเมื่อคุณลักษณะถูกปิด**</span><span class="sxs-lookup"><span data-stu-id="8248d-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="8248d-189">ยอดเงินในรายการสมุดรายวันสำหรับบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="8248d-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="8248d-190">ทิศทางของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-190">Sales tax direction</span></span>  | <span data-ttu-id="8248d-191">เครื่องหมายยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="8248d-192">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-192">Positive</span></span>                       | <span data-ttu-id="8248d-193">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-193">Sales Tax Receivable</span></span> | <span data-ttu-id="8248d-194">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-194">Positive</span></span>              |
| <span data-ttu-id="8248d-195">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-195">Negative</span></span>                       | <span data-ttu-id="8248d-196">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-196">Sales Tax Receivable</span></span> | <span data-ttu-id="8248d-197">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="8248d-198">กำหนดยอดเงินภาษีขายและบัญชีในใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="8248d-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="8248d-199">เมื่อคุณลงรายการบัญชีภาษีขาย จะมีการดึงข้อมูลบัญชีหลักมาจากโพรไฟล์กลุ่มการลงรายการบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="8248d-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="8248d-200">เมื่อภาษีขายเป็นบัญชีลูกหนี้ ระบบจะใช้บัญชีลูกหนี้ภาษีขายตามที่ระบุไว้ในโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="8248d-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="8248d-201">สำหรับภาษีขายที่เป็นบัญชีเจ้าหนี้ ระบบจะใช้บัญชีเจ้าหนี้ภาษีขายตามที่ระบุไว้ในโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="8248d-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="8248d-202">ตารางต่อไปนี้แสดงกฎทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8248d-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="8248d-203">ทิศทางของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-203">Sales tax direction</span></span>  | <span data-ttu-id="8248d-204">เครื่องหมายยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-204">Sales tax amount sign</span></span> | <span data-ttu-id="8248d-205">บัญชีภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-205">Sales tax account</span></span>      | <span data-ttu-id="8248d-206">ยอดเงินในใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="8248d-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="8248d-207">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-207">Sales Tax Receivable</span></span> | <span data-ttu-id="8248d-208">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-208">Positive</span></span>              | <span data-ttu-id="8248d-209">บัญชีภาษีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="8248d-209">Tax Receivable Account</span></span> | <span data-ttu-id="8248d-210">ค่าบวก (เดบิต)</span><span class="sxs-lookup"><span data-stu-id="8248d-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="8248d-211">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-211">Sales Tax Receivable</span></span> | <span data-ttu-id="8248d-212">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-212">Negative</span></span>              | <span data-ttu-id="8248d-213">บัญชีภาษีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="8248d-213">Tax Receivable Account</span></span> | <span data-ttu-id="8248d-214">ค่าลบ (เครดิต)</span><span class="sxs-lookup"><span data-stu-id="8248d-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="8248d-215">เจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-215">Sales Tax Payable</span></span>    | <span data-ttu-id="8248d-216">ค่าบวก</span><span class="sxs-lookup"><span data-stu-id="8248d-216">Positive</span></span>              | <span data-ttu-id="8248d-217">บัญชีภาษีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="8248d-217">Tax Payable Account</span></span>    | <span data-ttu-id="8248d-218">ค่าลบ (เครดิต)</span><span class="sxs-lookup"><span data-stu-id="8248d-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="8248d-219">เจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8248d-219">Sales Tax Payable</span></span>    | <span data-ttu-id="8248d-220">ค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8248d-220">Negative</span></span>              | <span data-ttu-id="8248d-221">บัญชีภาษีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="8248d-221">Tax Payable Account</span></span>    | <span data-ttu-id="8248d-222">ค่าบวก (เดบิต)</span><span class="sxs-lookup"><span data-stu-id="8248d-222">Positive (Debit)</span></span>  |
