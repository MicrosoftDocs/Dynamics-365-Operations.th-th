---
title: การรองรับสกุลเงินแบบคู่สำหรับภาษี
description: หัวข้อนี้จะอธิบายถึงวิธีการขยายคุณลักษณะการบัญชีสกุลเงินแบบคู่ในโดเมนภาษีและผลกระทบต่อการคำนวณภาษีและการลงรายการบัญชี
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
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
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 9e5db8e4bbd14aa30196e3be617cdfcb72c091fd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977178"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="db938-103">การรองรับสกุลเงินแบบคู่สำหรับภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="db938-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="db938-104">หัวข้อนี้จะอธิบายถึงวิธีการขยายการบัญชีสกุลเงินแบบคู่สำหรับภาษีขายและผลกระทบต่อการคำนวณภาษีขาย การลงรายการบัญชี และการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="db938-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="db938-105">คุณลักษณะสกุลเงินแบบคู่สำหรับ Dynamics 365 Finance ได้รับการแนะนำในรุ่น 8.1 (ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="db938-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="db938-106">การทำเช่นนี้จะเปลี่ยนวิธีในการคำนวณเอนทิตีบัญชีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="db938-107">ในรุ่นก่อนหน้านี้ ธุรกรรมได้รับการแปลงเป็นสกุลเงินการรายงานในลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="db938-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="db938-108">มีการคำนวณผลรวมของธุรกรรมในสกุลเงินของธุรกรรม > ยอดเงินในธุรกรรมจะถูกแปลงเป็นสกุลเงินทางบัญชี > ยอดเงินในสกุลเงินทางบัญชีจะถูกแปลงเป็นสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="db938-109">หลังจากเปิดใช้งานคุณลักษณะสกุลเงินแบบคู่ ธุรกรรมจะถูกแปลงเป็นสกุลเงินการรายงานในลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="db938-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="db938-110">ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="db938-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสกุลเงินแบบคู่ โปรดอ้างอิง [สกุลเงินแบบคู่](dual-currency.md)</span><span class="sxs-lookup"><span data-stu-id="db938-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="db938-112">เนื่องจากการสนับสนุนสำหรับสกุลเงินแบบคู่ คุณลักษณะใหม่สองรายการจะพร้อมใช้งานในการจัดการคุณลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="db938-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="db938-113">การแปลงภาษีขาย (การนำออกใช้ในรุ่น 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="db938-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="db938-114">ยอดดุลอัตโนมัติของการชำระภาษีในสกุลเงินการรายงาน (การนำออกใช้ในรุ่น 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="db938-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="db938-115">การสนับสนุนสกุลเงินแบบคู่สำหรับภาษีขายจะช่วยให้มั่นใจว่าภาษีจะถูกคำนวณอย่างถูกต้องในสกุลเงินภาษี และมีการคำนวณยอดดุลการชำระภาษีขายอย่างถูกต้องทั้งในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="db938-116">การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="db938-116">Sales tax conversion</span></span>

<span data-ttu-id="db938-117">พารามิเตอร์ **การแปลงภาษีขาย** ให้ตัวเลือกสองรายการในการแปลงยอดเงินภาษีจากสกุลเงินของธุรกรรมเป็นสกุลเงินภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="db938-118">สกุลเงินทางบัญชี: พาธจะเป็น "ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินทางบัญชี > ยอดเงินในสกุลเงินภาษี"</span><span class="sxs-lookup"><span data-stu-id="db938-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="db938-119">ชนิดอัตราแลกเปลี่ยนสกุลเงินทางบัญชี (ที่ตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท) จะถูกใช้สำหรับการแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="db938-119">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="db938-120">สกุลเงินการรายงาน: พาธจะเป็น "ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินการรายงาน > ยอดเงินในสกุลเงินภาษี"</span><span class="sxs-lookup"><span data-stu-id="db938-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="db938-121">ชนิดอัตราแลกเปลี่ยนสกุลเงินการรายงาน (ที่ตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท) จะถูกใช้สำหรับการแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="db938-121">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="db938-122">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="db938-122">Example</span></span>

<span data-ttu-id="db938-123">ตัวอย่างแบบง่ายเพื่อสาธิตฟังก์ชันนี้คือ:</span><span class="sxs-lookup"><span data-stu-id="db938-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="db938-124">การตั้งค่าสกุลเงินสำหรับบัญชีแยกประเภทและภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="db938-125">สกุลเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="db938-125">Transaction currency</span></span> | <span data-ttu-id="db938-126">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="db938-126">Accounting currency</span></span> | <span data-ttu-id="db938-127">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-127">Reporting currency</span></span> | <span data-ttu-id="db938-128">สกุลเงินภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="db938-129">EUR</span><span class="sxs-lookup"><span data-stu-id="db938-129">EUR</span></span>                  | <span data-ttu-id="db938-130">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="db938-130">USD</span></span>                 | <span data-ttu-id="db938-131">GBP</span><span class="sxs-lookup"><span data-stu-id="db938-131">GBP</span></span>                | <span data-ttu-id="db938-132">GBP</span><span class="sxs-lookup"><span data-stu-id="db938-132">GBP</span></span>          |

<span data-ttu-id="db938-133">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="db938-133">Exchange rate</span></span>

| <span data-ttu-id="db938-134">สกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="db938-134">From currency</span></span> | <span data-ttu-id="db938-135">สกุลเงินปลายทาง</span><span class="sxs-lookup"><span data-stu-id="db938-135">To currency</span></span> | <span data-ttu-id="db938-136">แฟคเตอร์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="db938-136">Factor</span></span> | <span data-ttu-id="db938-137">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="db938-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="db938-138">EUR</span><span class="sxs-lookup"><span data-stu-id="db938-138">EUR</span></span>           | <span data-ttu-id="db938-139">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="db938-139">USD</span></span>         | <span data-ttu-id="db938-140">1</span><span class="sxs-lookup"><span data-stu-id="db938-140">1</span></span>      | <span data-ttu-id="db938-141">1.11</span><span class="sxs-lookup"><span data-stu-id="db938-141">1.11</span></span>          |
| <span data-ttu-id="db938-142">EUR</span><span class="sxs-lookup"><span data-stu-id="db938-142">EUR</span></span>           | <span data-ttu-id="db938-143">GBP</span><span class="sxs-lookup"><span data-stu-id="db938-143">GBP</span></span>         | <span data-ttu-id="db938-144">1</span><span class="sxs-lookup"><span data-stu-id="db938-144">1</span></span>      | <span data-ttu-id="db938-145">0.83</span><span class="sxs-lookup"><span data-stu-id="db938-145">0.83</span></span>          |
| <span data-ttu-id="db938-146">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="db938-146">USD</span></span>           | <span data-ttu-id="db938-147">GBP</span><span class="sxs-lookup"><span data-stu-id="db938-147">GBP</span></span>         | <span data-ttu-id="db938-148">1</span><span class="sxs-lookup"><span data-stu-id="db938-148">1</span></span>      | <span data-ttu-id="db938-149">0.75</span><span class="sxs-lookup"><span data-stu-id="db938-149">0.75</span></span>          |

<span data-ttu-id="db938-150">การคำนวณยอดภาษีในตัวเลือกพารามิเตอร์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="db938-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="db938-151">ยอดภาษี = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="db938-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="db938-152">พารามิเตอร์การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="db938-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="db938-153">สกุลเงินของธุรกรรม (EUR)</span><span class="sxs-lookup"><span data-stu-id="db938-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="db938-154">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="db938-154">Accounting currency (USD)</span></span> | <span data-ttu-id="db938-155">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="db938-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="db938-156">สกุลเงินภาษี (GBP)</span><span class="sxs-lookup"><span data-stu-id="db938-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="db938-157">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="db938-157">Accounting currency</span></span>             | <span data-ttu-id="db938-158">100</span><span class="sxs-lookup"><span data-stu-id="db938-158">100</span></span>                        | <span data-ttu-id="db938-159">111</span><span class="sxs-lookup"><span data-stu-id="db938-159">111</span></span>                       | <span data-ttu-id="db938-160">83</span><span class="sxs-lookup"><span data-stu-id="db938-160">83</span></span>                       | <span data-ttu-id="db938-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="db938-161">**83.25**</span></span>          |
| <span data-ttu-id="db938-162">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-162">Reporting currency</span></span>              | <span data-ttu-id="db938-163">100</span><span class="sxs-lookup"><span data-stu-id="db938-163">100</span></span>                        | <span data-ttu-id="db938-164">111</span><span class="sxs-lookup"><span data-stu-id="db938-164">111</span></span>                       | <span data-ttu-id="db938-165">83</span><span class="sxs-lookup"><span data-stu-id="db938-165">83</span></span>                       | <span data-ttu-id="db938-166">**83**</span><span class="sxs-lookup"><span data-stu-id="db938-166">**83**</span></span>             |

<span data-ttu-id="db938-167">คุณสามารถตั้งค่าคอนฟิกพารามิเตอร์นี้ตามความต้องการในการปฏิบัติตามกฎระเบียบจากหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="db938-168">ข้อควรพิจารณาสำหรับการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="db938-168">Upgrade Consideration</span></span>

<span data-ttu-id="db938-169">คุณลักษณะจะใช้สำหรับธุรกรรมใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="db938-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="db938-170">สำหรับธุรกรรมภาษีที่บันทึกไว้แล้วในตาราง TAXTRANS แล้วแต่ยังไม่ได้ชำระเงิน ระบบจะไม่คำนวณยอดภาษีในสกุลเงินภาษีใหม่ เนื่องจากอัตราแลกเปลี่ยน ณ จุดเวลาของภาษีการลงรายการบัญชีขาดหายไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="db938-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="db938-171">หากต้องการป้องกันสถานการณ์จำลองก่อนหน้านี้ เราขอแนะนำให้เปลี่ยนค่าพารามิเตอร์นี้ในรอบระยะเวลาการชำระภาษีใหม่ (ใหม่ทั้งหมด) ที่ไม่มีธุรกรรมภาษีที่ยังไม่ได้ชำระใดๆ</span><span class="sxs-lookup"><span data-stu-id="db938-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="db938-172">เมื่อต้องการเปลี่ยนค่านี้ในช่วงกลางของรอบระยะเวลาการจ่ายภาษี โปรดรันโปรแกรม "ชำระเงินและลงรายการบัญชีภาษีขาย" สำหรับรอบระยะเวลาการชำระภาษีปัจจุบัน ก่อนที่จะเปลี่ยนค่าพารามิเตอร์นี้</span><span class="sxs-lookup"><span data-stu-id="db938-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="db938-173">ติดตามยอดเงินภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-173">Track reporting currency tax amount</span></span>

<span data-ttu-id="db938-174">มีการเพิ่มฟิลด์ใหม่สามฟิลด์ให้กับตารางที่เกี่ยวข้องกับภาษี เพื่อติดตามยอดเงินในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-174">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="db938-175">ฟิลด์เหล่านี้อยู่ภายในตาราง TAXUNCOMMITTED และ TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="db938-175">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="db938-176">TaxAmountRep: ยอดภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-176">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="db938-177">TaxBaseAmountRep: ยอดเงินฐานในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-177">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="db938-178">TaxInCostPriceRep: ยอดเงินที่ไม่สามารถหักได้ในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-178">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="db938-179">สำหรับภาษีที่บันทึกไว้เฉพาะในตาราง TAXUNCOMMITTED แต่ยังไม่ได้ลงรายการบัญชี ระบบจะคำนวณยอดภาษีใหม่ในสกุลเงินการรายงานเมื่อลงรายการบัญชีและบันทึกในตาราง TAXTRANS</span><span class="sxs-lookup"><span data-stu-id="db938-179">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="db938-180">รุ่นที่นำออกใช้นี้จะไม่มีการเปลี่ยนแปลงในรายงานและฟอร์มที่แสดงยอดภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-180">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="db938-181">การเปลี่ยนแปลงไปยังรายงานและฟอร์มจะถูกจัดส่งในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="db938-181">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="db938-182">ยอดดุลอัตโนมัติของการชำระภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-182">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="db938-183">ถ้าการชำระภาษีไม่สมดุลในสกุลเงินการรายงานเนื่องจากเหตุผลบางประการ เช่น พาธการแปลงภาษีขายคือ "สกุลเงินทางบัญชี" หรือการเปลี่ยนแปลงอัตราแลกเปลี่ยนในรอบระยะเวลาการชำระภาษีหนึ่งๆ จากนั้น ระบบจะสร้างรายการบัญชีโดยอัตโนมัติเพื่อปรับผลต่างของยอดเงินภาษีและออฟเซ็ตเทียบกับบัญชีกำไร/ขาดทุนที่รับรู้จากอัตราแลกเปลี่ยน ซึ่งถูกตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="db938-183">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="db938-184">การใช้ตัวอย่างก่อนหน้านี้แสดงให้เห็นถึงคุณลักษณะนี้ สมมติว่าข้อมูลในตาราง TAXTRANS ในเวลาที่ลงรายการบัญชีเป็นดังนี้</span><span class="sxs-lookup"><span data-stu-id="db938-184">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="db938-185">พารามิเตอร์การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="db938-185">Sales tax conversion parameters</span></span> | <span data-ttu-id="db938-186">สกุลเงินของธุรกรรม (EUR)</span><span class="sxs-lookup"><span data-stu-id="db938-186">Transaction currency (EUR)</span></span> | <span data-ttu-id="db938-187">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="db938-187">Accounting currency (USD)</span></span> | <span data-ttu-id="db938-188">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="db938-188">Reporting currency (GBP)</span></span> | <span data-ttu-id="db938-189">สกุลเงินภาษี (GBP)</span><span class="sxs-lookup"><span data-stu-id="db938-189">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="db938-190">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="db938-190">Accounting currency</span></span>             | <span data-ttu-id="db938-191">100</span><span class="sxs-lookup"><span data-stu-id="db938-191">100</span></span>                        | <span data-ttu-id="db938-192">111</span><span class="sxs-lookup"><span data-stu-id="db938-192">111</span></span>                       | <span data-ttu-id="db938-193">83</span><span class="sxs-lookup"><span data-stu-id="db938-193">83</span></span>                       | <span data-ttu-id="db938-194">**83.25**</span><span class="sxs-lookup"><span data-stu-id="db938-194">**83.25**</span></span>          |
| <span data-ttu-id="db938-195">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="db938-195">Reporting currency</span></span>              | <span data-ttu-id="db938-196">100</span><span class="sxs-lookup"><span data-stu-id="db938-196">100</span></span>                        | <span data-ttu-id="db938-197">111</span><span class="sxs-lookup"><span data-stu-id="db938-197">111</span></span>                       | <span data-ttu-id="db938-198">83</span><span class="sxs-lookup"><span data-stu-id="db938-198">83</span></span>                       | <span data-ttu-id="db938-199">**83**</span><span class="sxs-lookup"><span data-stu-id="db938-199">**83**</span></span>             |

<span data-ttu-id="db938-200">เมื่อคุณรันโปรแกรมการชำระภาษีขายในช่วงสิ้นเดือน รายการบัญชีจะเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="db938-200">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="db938-201">สถานการณ์จำลอง: การแปลงภาษีขาย = "สกุลเงินทางบัญชี"</span><span class="sxs-lookup"><span data-stu-id="db938-201">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="db938-202">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="db938-202">Main account</span></span>           | <span data-ttu-id="db938-203">สกุลเงินของธุรกรรม (GBP)</span><span class="sxs-lookup"><span data-stu-id="db938-203">Transaction currency (GBP)</span></span> | <span data-ttu-id="db938-204">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="db938-204">Accounting currency (USD)</span></span> | <span data-ttu-id="db938-205">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="db938-205">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="db938-206">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-206">Tax Payable/Receivable</span></span> | <span data-ttu-id="db938-207">-83.25</span><span class="sxs-lookup"><span data-stu-id="db938-207">-83.25</span></span>                     | <span data-ttu-id="db938-208">-111</span><span class="sxs-lookup"><span data-stu-id="db938-208">-111</span></span>                      | <span data-ttu-id="db938-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="db938-209">-83.25</span></span>                   |
| <span data-ttu-id="db938-210">การชำระภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-210">Tax Settlement</span></span>         | <span data-ttu-id="db938-211">83.25</span><span class="sxs-lookup"><span data-stu-id="db938-211">83.25</span></span>                      | <span data-ttu-id="db938-212">111</span><span class="sxs-lookup"><span data-stu-id="db938-212">111</span></span>                       | <span data-ttu-id="db938-213">83.25</span><span class="sxs-lookup"><span data-stu-id="db938-213">83.25</span></span>                    |
| <span data-ttu-id="db938-214">กำไร/ขาดทุนที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="db938-214">Realized Gain/Loss</span></span>     | <span data-ttu-id="db938-215">0</span><span class="sxs-lookup"><span data-stu-id="db938-215">0</span></span>                          | <span data-ttu-id="db938-216">0</span><span class="sxs-lookup"><span data-stu-id="db938-216">0</span></span>                         | <span data-ttu-id="db938-217">-0.25</span><span class="sxs-lookup"><span data-stu-id="db938-217">-0.25</span></span>                    |
| <span data-ttu-id="db938-218">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-218">Tax Payable/Receivable</span></span> | <span data-ttu-id="db938-219">0</span><span class="sxs-lookup"><span data-stu-id="db938-219">0</span></span>                          | <span data-ttu-id="db938-220">0</span><span class="sxs-lookup"><span data-stu-id="db938-220">0</span></span>                         | <span data-ttu-id="db938-221">0.25</span><span class="sxs-lookup"><span data-stu-id="db938-221">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="db938-222">สถานการณ์จำลอง: การแปลงภาษีขาย = "สกุลเงินการรายงาน"</span><span class="sxs-lookup"><span data-stu-id="db938-222">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="db938-223">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="db938-223">Main account</span></span>           | <span data-ttu-id="db938-224">สกุลเงินของธุรกรรม (GBP)</span><span class="sxs-lookup"><span data-stu-id="db938-224">Transaction currency (GBP)</span></span> | <span data-ttu-id="db938-225">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="db938-225">Accounting currency (USD)</span></span> | <span data-ttu-id="db938-226">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="db938-226">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="db938-227">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-227">Tax Payable/Receivable</span></span> | <span data-ttu-id="db938-228">-83</span><span class="sxs-lookup"><span data-stu-id="db938-228">-83</span></span>                        | <span data-ttu-id="db938-229">-110.67</span><span class="sxs-lookup"><span data-stu-id="db938-229">-110.67</span></span>                   | <span data-ttu-id="db938-230">-83</span><span class="sxs-lookup"><span data-stu-id="db938-230">-83</span></span>                      |
| <span data-ttu-id="db938-231">การชำระภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-231">Tax Settlement</span></span>         | <span data-ttu-id="db938-232">83</span><span class="sxs-lookup"><span data-stu-id="db938-232">83</span></span>                         | <span data-ttu-id="db938-233">110.67</span><span class="sxs-lookup"><span data-stu-id="db938-233">110.67</span></span>                    | <span data-ttu-id="db938-234">83</span><span class="sxs-lookup"><span data-stu-id="db938-234">83</span></span>                       |
| <span data-ttu-id="db938-235">กำไร/ขาดทุนที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="db938-235">Realized Gain/Loss</span></span>     | <span data-ttu-id="db938-236">0</span><span class="sxs-lookup"><span data-stu-id="db938-236">0</span></span>                          | <span data-ttu-id="db938-237">0.33</span><span class="sxs-lookup"><span data-stu-id="db938-237">0.33</span></span>                      | <span data-ttu-id="db938-238">0</span><span class="sxs-lookup"><span data-stu-id="db938-238">0</span></span>                        |
| <span data-ttu-id="db938-239">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="db938-239">Tax Payable/Receivable</span></span> | <span data-ttu-id="db938-240">0</span><span class="sxs-lookup"><span data-stu-id="db938-240">0</span></span>                          | <span data-ttu-id="db938-241">-0.33</span><span class="sxs-lookup"><span data-stu-id="db938-241">-0.33</span></span>                     | <span data-ttu-id="db938-242">0</span><span class="sxs-lookup"><span data-stu-id="db938-242">0</span></span>                        |



<span data-ttu-id="db938-243">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="db938-243">For more information, see the following topics:</span></span>

- [<span data-ttu-id="db938-244">สกุลเงินแบบคู่</span><span class="sxs-lookup"><span data-stu-id="db938-244">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="db938-245">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="db938-245">Sales tax overview</span></span>](indirect-taxes-overview.md)

