---
title: การรองรับสกุลเงินแบบคู่สำหรับภาษี
description: หัวข้อนี้จะอธิบายถึงวิธีการขยายคุณลักษณะการบัญชีสกุลเงินแบบคู่ในโดเมนภาษีและผลกระทบต่อการคำนวณภาษีและการลงรายการบัญชี
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0a3245febe31857181d17bba42e12b65f4ebb40f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832981"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="ec739-103">การรองรับสกุลเงินแบบคู่สำหรับภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="ec739-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec739-104">หัวข้อนี้จะอธิบายถึงวิธีการขยายการบัญชีสกุลเงินแบบคู่สำหรับภาษีขายและผลกระทบต่อการคำนวณภาษีขาย การลงรายการบัญชี และการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ec739-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="ec739-105">คุณลักษณะสกุลเงินแบบคู่สำหรับ Dynamics 365 Finance ได้รับการแนะนำในรุ่น 8.1 (ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="ec739-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="ec739-106">การทำเช่นนี้จะเปลี่ยนวิธีในการคำนวณเอนทิตีบัญชีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="ec739-107">ในรุ่นก่อนหน้านี้ ธุรกรรมได้รับการแปลงเป็นสกุลเงินการรายงานในลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ec739-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="ec739-108">มีการคำนวณผลรวมของธุรกรรมในสกุลเงินของธุรกรรม > ยอดเงินในธุรกรรมจะถูกแปลงเป็นสกุลเงินทางบัญชี > ยอดเงินในสกุลเงินทางบัญชีจะถูกแปลงเป็นสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="ec739-109">หลังจากเปิดใช้งานคุณลักษณะสกุลเงินแบบคู่ ธุรกรรมจะถูกแปลงเป็นสกุลเงินการรายงานในลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ec739-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="ec739-110">ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="ec739-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสกุลเงินแบบคู่ โปรดอ้างอิง [สกุลเงินแบบคู่](dual-currency.md)</span><span class="sxs-lookup"><span data-stu-id="ec739-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="ec739-112">เนื่องจากการสนับสนุนสำหรับสกุลเงินแบบคู่ คุณลักษณะใหม่สองรายการจะพร้อมใช้งานในการจัดการคุณลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="ec739-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="ec739-113">การแปลงภาษีขาย (รายการใหม่ในรุ่น 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="ec739-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="ec739-114">การสนับสนุนสกุลเงินแบบคู่สำหรับภาษีขายจะช่วยให้มั่นใจว่าภาษีจะถูกคำนวณอย่างถูกต้องในสกุลเงินภาษี และมีการคำนวณยอดดุลการชำระภาษีขายอย่างถูกต้องทั้งในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="ec739-115">การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="ec739-115">Sales tax conversion</span></span>

<span data-ttu-id="ec739-116">พารามิเตอร์ **การแปลงภาษีขาย** ให้ตัวเลือกสองรายการในการแปลงยอดเงินภาษีจากสกุลเงินของธุรกรรมเป็นสกุลเงินภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="ec739-117">สกุลเงินทางบัญชี: พาธจะเป็น "ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินทางบัญชี > ยอดเงินในสกุลเงินภาษี"</span><span class="sxs-lookup"><span data-stu-id="ec739-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="ec739-118">ชนิดอัตราแลกเปลี่ยนสกุลเงินทางบัญชี (ที่ตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท) จะถูกใช้สำหรับการแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="ec739-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="ec739-119">สกุลเงินการรายงาน: พาธจะเป็น "ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินการรายงาน > ยอดเงินในสกุลเงินภาษี"</span><span class="sxs-lookup"><span data-stu-id="ec739-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="ec739-120">ชนิดอัตราแลกเปลี่ยนสกุลเงินการรายงาน (ที่ตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท) จะถูกใช้สำหรับการแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="ec739-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="ec739-121">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ec739-121">Example</span></span>

<span data-ttu-id="ec739-122">ตัวอย่างแบบง่ายเพื่อสาธิตฟังก์ชันนี้คือ:</span><span class="sxs-lookup"><span data-stu-id="ec739-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="ec739-123">การตั้งค่าสกุลเงินสำหรับบัญชีแยกประเภทและภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="ec739-124">สกุลเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ec739-124">Transaction currency</span></span> | <span data-ttu-id="ec739-125">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="ec739-125">Accounting currency</span></span> | <span data-ttu-id="ec739-126">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-126">Reporting currency</span></span> | <span data-ttu-id="ec739-127">สกุลเงินภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="ec739-128">EUR</span><span class="sxs-lookup"><span data-stu-id="ec739-128">EUR</span></span>                  | <span data-ttu-id="ec739-129">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="ec739-129">USD</span></span>                 | <span data-ttu-id="ec739-130">GBP</span><span class="sxs-lookup"><span data-stu-id="ec739-130">GBP</span></span>                | <span data-ttu-id="ec739-131">GBP</span><span class="sxs-lookup"><span data-stu-id="ec739-131">GBP</span></span>          |

<span data-ttu-id="ec739-132">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="ec739-132">Exchange rate</span></span>

| <span data-ttu-id="ec739-133">สกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="ec739-133">From currency</span></span> | <span data-ttu-id="ec739-134">สกุลเงินปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ec739-134">To currency</span></span> | <span data-ttu-id="ec739-135">แฟคเตอร์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-135">Factor</span></span> | <span data-ttu-id="ec739-136">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="ec739-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="ec739-137">EUR</span><span class="sxs-lookup"><span data-stu-id="ec739-137">EUR</span></span>           | <span data-ttu-id="ec739-138">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="ec739-138">USD</span></span>         | <span data-ttu-id="ec739-139">1</span><span class="sxs-lookup"><span data-stu-id="ec739-139">1</span></span>      | <span data-ttu-id="ec739-140">1.11</span><span class="sxs-lookup"><span data-stu-id="ec739-140">1.11</span></span>          |
| <span data-ttu-id="ec739-141">EUR</span><span class="sxs-lookup"><span data-stu-id="ec739-141">EUR</span></span>           | <span data-ttu-id="ec739-142">GBP</span><span class="sxs-lookup"><span data-stu-id="ec739-142">GBP</span></span>         | <span data-ttu-id="ec739-143">1</span><span class="sxs-lookup"><span data-stu-id="ec739-143">1</span></span>      | <span data-ttu-id="ec739-144">0.83</span><span class="sxs-lookup"><span data-stu-id="ec739-144">0.83</span></span>          |
| <span data-ttu-id="ec739-145">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="ec739-145">USD</span></span>           | <span data-ttu-id="ec739-146">GBP</span><span class="sxs-lookup"><span data-stu-id="ec739-146">GBP</span></span>         | <span data-ttu-id="ec739-147">1</span><span class="sxs-lookup"><span data-stu-id="ec739-147">1</span></span>      | <span data-ttu-id="ec739-148">0.75</span><span class="sxs-lookup"><span data-stu-id="ec739-148">0.75</span></span>          |

<span data-ttu-id="ec739-149">การคำนวณยอดภาษีในตัวเลือกพารามิเตอร์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="ec739-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="ec739-150">ยอดภาษี = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="ec739-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="ec739-151">พารามิเตอร์การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="ec739-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="ec739-152">สกุลเงินของธุรกรรม (EUR)</span><span class="sxs-lookup"><span data-stu-id="ec739-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="ec739-153">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="ec739-153">Accounting currency (USD)</span></span> | <span data-ttu-id="ec739-154">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="ec739-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="ec739-155">สกุลเงินภาษี (GBP)</span><span class="sxs-lookup"><span data-stu-id="ec739-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="ec739-156">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="ec739-156">Accounting currency</span></span>             | <span data-ttu-id="ec739-157">100</span><span class="sxs-lookup"><span data-stu-id="ec739-157">100</span></span>                        | <span data-ttu-id="ec739-158">111</span><span class="sxs-lookup"><span data-stu-id="ec739-158">111</span></span>                       | <span data-ttu-id="ec739-159">83</span><span class="sxs-lookup"><span data-stu-id="ec739-159">83</span></span>                       | <span data-ttu-id="ec739-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="ec739-160">**83.25**</span></span>          |
| <span data-ttu-id="ec739-161">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-161">Reporting currency</span></span>              | <span data-ttu-id="ec739-162">100</span><span class="sxs-lookup"><span data-stu-id="ec739-162">100</span></span>                        | <span data-ttu-id="ec739-163">111</span><span class="sxs-lookup"><span data-stu-id="ec739-163">111</span></span>                       | <span data-ttu-id="ec739-164">83</span><span class="sxs-lookup"><span data-stu-id="ec739-164">83</span></span>                       | <span data-ttu-id="ec739-165">**83**</span><span class="sxs-lookup"><span data-stu-id="ec739-165">**83**</span></span>             |

<span data-ttu-id="ec739-166">คุณสามารถตั้งค่าคอนฟิกพารามิเตอร์นี้ตามความต้องการในการปฏิบัติตามกฎระเบียบจากหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="ec739-167">ข้อควรพิจารณาสำหรับการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="ec739-167">Upgrade Consideration</span></span>

<span data-ttu-id="ec739-168">คุณลักษณะจะใช้สำหรับธุรกรรมใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ec739-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="ec739-169">สำหรับธุรกรรมภาษีที่บันทึกไว้แล้วในตาราง TAXTRANS แล้วแต่ยังไม่ได้ชำระเงิน ระบบจะไม่คำนวณยอดภาษีในสกุลเงินภาษีใหม่ เนื่องจากอัตราแลกเปลี่ยน ณ จุดเวลาของภาษีการลงรายการบัญชีขาดหายไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="ec739-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="ec739-170">หากต้องการป้องกันสถานการณ์จำลองก่อนหน้านี้ เราขอแนะนำให้เปลี่ยนค่าพารามิเตอร์นี้ในรอบระยะเวลาการชำระภาษีใหม่ (ใหม่ทั้งหมด) ที่ไม่มีธุรกรรมภาษีที่ยังไม่ได้ชำระใดๆ</span><span class="sxs-lookup"><span data-stu-id="ec739-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="ec739-171">เมื่อต้องการเปลี่ยนค่านี้ในช่วงกลางของรอบระยะเวลาการจ่ายภาษี โปรดรันโปรแกรม "ชำระเงินและลงรายการบัญชีภาษีขาย" สำหรับรอบระยะเวลาการชำระภาษีปัจจุบัน ก่อนที่จะเปลี่ยนค่าพารามิเตอร์นี้</span><span class="sxs-lookup"><span data-stu-id="ec739-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="ec739-172">ติดตามยอดเงินภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="ec739-173">มีการเพิ่มฟิลด์ใหม่สามฟิลด์ให้กับตารางที่เกี่ยวข้องกับภาษี เพื่อติดตามยอดเงินในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="ec739-174">ฟิลด์เหล่านี้อยู่ภายในตาราง TAXUNCOMMITTED และ TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="ec739-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="ec739-175">TaxAmountRep: ยอดภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="ec739-176">TaxBaseAmountRep: ยอดเงินฐานในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="ec739-177">TaxInCostPriceRep: ยอดเงินที่ไม่สามารถหักได้ในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="ec739-178">สำหรับภาษีที่บันทึกไว้เฉพาะในตาราง TAXUNCOMMITTED แต่ยังไม่ได้ลงรายการบัญชี ระบบจะคำนวณยอดภาษีใหม่ในสกุลเงินการรายงานเมื่อลงรายการบัญชีและบันทึกในตาราง TAXTRANS</span><span class="sxs-lookup"><span data-stu-id="ec739-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="ec739-179">รุ่นที่นำออกใช้นี้จะไม่มีการเปลี่ยนแปลงในรายงานและฟอร์มที่แสดงยอดภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="ec739-180">การเปลี่ยนแปลงไปยังรายงานและฟอร์มจะถูกจัดส่งในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="ec739-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="ec739-181">ยอดดุลอัตโนมัติของการชำระภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="ec739-182">ถ้าการชำระภาษีไม่สมดุลในสกุลเงินการรายงานเนื่องจากเหตุผลบางประการ เช่น พาธการแปลงภาษีขายคือ "สกุลเงินทางบัญชี" หรือการเปลี่ยนแปลงอัตราแลกเปลี่ยนในรอบระยะเวลาการชำระภาษีหนึ่งๆ จากนั้น ระบบจะสร้างรายการการบัญชีโดยอัตโนมัติเพื่อปรับผลต่างของยอดเงินภาษีและออฟเซ็ตเทียบกับบัญชีกำไร/ขาดทุนที่รับรู้จากอัตราแลกเปลี่ยน ซึ่งถูกตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="ec739-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="ec739-183">การใช้ตัวอย่างก่อนหน้านี้แสดงให้เห็นถึงคุณลักษณะนี้ สมมติว่าข้อมูลในตาราง TAXTRANS ในเวลาที่ลงรายการบัญชีเป็นดังนี้</span><span class="sxs-lookup"><span data-stu-id="ec739-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="ec739-184">พารามิเตอร์การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="ec739-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="ec739-185">สกุลเงินของธุรกรรม (EUR)</span><span class="sxs-lookup"><span data-stu-id="ec739-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="ec739-186">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="ec739-186">Accounting currency (USD)</span></span> | <span data-ttu-id="ec739-187">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="ec739-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="ec739-188">สกุลเงินภาษี (GBP)</span><span class="sxs-lookup"><span data-stu-id="ec739-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="ec739-189">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="ec739-189">Accounting currency</span></span>             | <span data-ttu-id="ec739-190">100</span><span class="sxs-lookup"><span data-stu-id="ec739-190">100</span></span>                        | <span data-ttu-id="ec739-191">111</span><span class="sxs-lookup"><span data-stu-id="ec739-191">111</span></span>                       | <span data-ttu-id="ec739-192">83</span><span class="sxs-lookup"><span data-stu-id="ec739-192">83</span></span>                       | <span data-ttu-id="ec739-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="ec739-193">**83.25**</span></span>          |
| <span data-ttu-id="ec739-194">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec739-194">Reporting currency</span></span>              | <span data-ttu-id="ec739-195">100</span><span class="sxs-lookup"><span data-stu-id="ec739-195">100</span></span>                        | <span data-ttu-id="ec739-196">111</span><span class="sxs-lookup"><span data-stu-id="ec739-196">111</span></span>                       | <span data-ttu-id="ec739-197">83</span><span class="sxs-lookup"><span data-stu-id="ec739-197">83</span></span>                       | <span data-ttu-id="ec739-198">**83**</span><span class="sxs-lookup"><span data-stu-id="ec739-198">**83**</span></span>             |

<span data-ttu-id="ec739-199">เมื่อคุณรันโปรแกรมการชำระภาษีขายในช่วงสิ้นเดือน รายการบัญชีจะเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="ec739-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="ec739-200">สถานการณ์จำลอง: การแปลงภาษีขาย = "สกุลเงินทางบัญชี"</span><span class="sxs-lookup"><span data-stu-id="ec739-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="ec739-201">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="ec739-201">Main account</span></span>           | <span data-ttu-id="ec739-202">สกุลเงินของธุรกรรม (GBP)</span><span class="sxs-lookup"><span data-stu-id="ec739-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="ec739-203">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="ec739-203">Accounting currency (USD)</span></span> | <span data-ttu-id="ec739-204">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="ec739-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="ec739-205">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="ec739-206">-83.25</span><span class="sxs-lookup"><span data-stu-id="ec739-206">-83.25</span></span>                     | <span data-ttu-id="ec739-207">-111</span><span class="sxs-lookup"><span data-stu-id="ec739-207">-111</span></span>                      | <span data-ttu-id="ec739-208">-83.25</span><span class="sxs-lookup"><span data-stu-id="ec739-208">-83.25</span></span>                   |
| <span data-ttu-id="ec739-209">การชำระภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-209">Tax Settlement</span></span>         | <span data-ttu-id="ec739-210">83.25</span><span class="sxs-lookup"><span data-stu-id="ec739-210">83.25</span></span>                      | <span data-ttu-id="ec739-211">111</span><span class="sxs-lookup"><span data-stu-id="ec739-211">111</span></span>                       | <span data-ttu-id="ec739-212">83.25</span><span class="sxs-lookup"><span data-stu-id="ec739-212">83.25</span></span>                    |
| <span data-ttu-id="ec739-213">กำไร/ขาดทุนที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="ec739-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="ec739-214">0</span><span class="sxs-lookup"><span data-stu-id="ec739-214">0</span></span>                          | <span data-ttu-id="ec739-215">0</span><span class="sxs-lookup"><span data-stu-id="ec739-215">0</span></span>                         | <span data-ttu-id="ec739-216">-0.25</span><span class="sxs-lookup"><span data-stu-id="ec739-216">-0.25</span></span>                    |
| <span data-ttu-id="ec739-217">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="ec739-218">0</span><span class="sxs-lookup"><span data-stu-id="ec739-218">0</span></span>                          | <span data-ttu-id="ec739-219">0</span><span class="sxs-lookup"><span data-stu-id="ec739-219">0</span></span>                         | <span data-ttu-id="ec739-220">0.25</span><span class="sxs-lookup"><span data-stu-id="ec739-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="ec739-221">สถานการณ์จำลอง: การแปลงภาษีขาย = "สกุลเงินการรายงาน"</span><span class="sxs-lookup"><span data-stu-id="ec739-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="ec739-222">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="ec739-222">Main account</span></span>           | <span data-ttu-id="ec739-223">สกุลเงินของธุรกรรม (GBP)</span><span class="sxs-lookup"><span data-stu-id="ec739-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="ec739-224">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="ec739-224">Accounting currency (USD)</span></span> | <span data-ttu-id="ec739-225">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="ec739-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="ec739-226">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="ec739-227">-83</span><span class="sxs-lookup"><span data-stu-id="ec739-227">-83</span></span>                        | <span data-ttu-id="ec739-228">-110.67</span><span class="sxs-lookup"><span data-stu-id="ec739-228">-110.67</span></span>                   | <span data-ttu-id="ec739-229">-83</span><span class="sxs-lookup"><span data-stu-id="ec739-229">-83</span></span>                      |
| <span data-ttu-id="ec739-230">การชำระภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-230">Tax Settlement</span></span>         | <span data-ttu-id="ec739-231">83</span><span class="sxs-lookup"><span data-stu-id="ec739-231">83</span></span>                         | <span data-ttu-id="ec739-232">110.67</span><span class="sxs-lookup"><span data-stu-id="ec739-232">110.67</span></span>                    | <span data-ttu-id="ec739-233">83</span><span class="sxs-lookup"><span data-stu-id="ec739-233">83</span></span>                       |
| <span data-ttu-id="ec739-234">กำไร/ขาดทุนที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="ec739-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="ec739-235">0</span><span class="sxs-lookup"><span data-stu-id="ec739-235">0</span></span>                          | <span data-ttu-id="ec739-236">0.33</span><span class="sxs-lookup"><span data-stu-id="ec739-236">0.33</span></span>                      | <span data-ttu-id="ec739-237">0</span><span class="sxs-lookup"><span data-stu-id="ec739-237">0</span></span>                        |
| <span data-ttu-id="ec739-238">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="ec739-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="ec739-239">0</span><span class="sxs-lookup"><span data-stu-id="ec739-239">0</span></span>                          | <span data-ttu-id="ec739-240">-0.33</span><span class="sxs-lookup"><span data-stu-id="ec739-240">-0.33</span></span>                     | <span data-ttu-id="ec739-241">0</span><span class="sxs-lookup"><span data-stu-id="ec739-241">0</span></span>                        |



<span data-ttu-id="ec739-242">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ec739-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="ec739-243">สกุลเงินแบบคู่</span><span class="sxs-lookup"><span data-stu-id="ec739-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="ec739-244">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="ec739-244">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]