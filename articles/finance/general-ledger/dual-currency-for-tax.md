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
ms.author: vstehman
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 1ba4d09240888f0c533fb07614e75ffecea0742c
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124104"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="95c1e-103">การรองรับสกุลเงินแบบคู่สำหรับภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="95c1e-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="95c1e-104">หัวข้อนี้จะอธิบายถึงวิธีการขยายการบัญชีสกุลเงินแบบคู่สำหรับภาษีขายและผลกระทบต่อการคำนวณภาษีขาย การลงรายการบัญชี และการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="95c1e-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="95c1e-105">คุณลักษณะสกุลเงินแบบคู่สำหรับ Dynamics 365 Finance ได้รับการแนะนำในรุ่น 8.1 (ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="95c1e-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="95c1e-106">การทำเช่นนี้จะเปลี่ยนวิธีในการคำนวณเอนทิตีบัญชีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="95c1e-107">ในรุ่นก่อนหน้านี้ ธุรกรรมได้รับการแปลงเป็นสกุลเงินการรายงานในลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="95c1e-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

<span data-ttu-id="95c1e-108">มีการคำนวณผลรวมของธุรกรรมในสกุลเงินของธุรกรรม > ยอดเงินในธุรกรรมจะถูกแปลงเป็นสกุลเงินทางบัญชี > ยอดเงินในสกุลเงินทางบัญชีจะถูกแปลงเป็นสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="95c1e-109">หลังจากเปิดใช้งานคุณลักษณะสกุลเงินแบบคู่ ธุรกรรมจะถูกแปลงเป็นสกุลเงินการรายงานในลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="95c1e-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="95c1e-110">ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="95c1e-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสกุลเงินแบบคู่ โปรดอ้างอิง [สกุลเงินแบบคู่](dual-currency.md)</span><span class="sxs-lookup"><span data-stu-id="95c1e-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="95c1e-112">เนื่องจากการสนับสนุนสำหรับสกุลเงินแบบคู่ คุณลักษณะใหม่สองรายการจะพร้อมใช้งานในการจัดการคุณลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="95c1e-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="95c1e-113">การแปลงภาษีขาย (การนำออกใช้ในรุ่น 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="95c1e-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="95c1e-114">ยอดดุลอัตโนมัติของการชำระภาษีในสกุลเงินการรายงาน (การนำออกใช้ในรุ่น 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="95c1e-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="95c1e-115">การสนับสนุนสกุลเงินแบบคู่สำหรับภาษีขายจะช่วยให้มั่นใจว่าภาษีจะถูกคำนวณอย่างถูกต้องในสกุลเงินภาษี และมีการคำนวณยอดดุลการชำระภาษีขายอย่างถูกต้องทั้งในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

<span data-ttu-id="95c1e-116">มีการเปิดใช้งานคุณลักษณะใหม่สำหรับลูกค้าการแสดงตัวอย่างแบบส่วนตัวในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="95c1e-116">The new features are currently enabled for private preview customers.</span></span> <span data-ttu-id="95c1e-117">เมื่อต้องการเปิดใช้งานคุณลักษณะ ให้ขอบริการผ่านช่องทางที่ตรงกันกับ Microsoft</span><span class="sxs-lookup"><span data-stu-id="95c1e-117">To enable the features, raise a service request through corresponding channels to Microsoft.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="95c1e-118">การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="95c1e-118">Sales tax conversion</span></span>

<span data-ttu-id="95c1e-119">พารามิเตอร์ **การแปลงภาษีขาย** ให้ตัวเลือกสองรายการในการแปลงยอดเงินภาษีจากสกุลเงินของธุรกรรมเป็นสกุลเงินภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-119">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="95c1e-120">สกุลเงินทางบัญชี: พาธจะเป็น "ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินทางบัญชี > ยอดเงินในสกุลเงินภาษี"</span><span class="sxs-lookup"><span data-stu-id="95c1e-120">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="95c1e-121">ชนิดอัตราแลกเปลี่ยนสกุลเงินทางบัญชี (ที่ตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท) จะถูกใช้สำหรับการแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="95c1e-121">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="95c1e-122">สกุลเงินการรายงาน: พาธจะเป็น "ยอดเงินในสกุลเงินของธุรกรรม > ยอดเงินในสกุลเงินการรายงาน > ยอดเงินในสกุลเงินภาษี"</span><span class="sxs-lookup"><span data-stu-id="95c1e-122">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="95c1e-123">ชนิดอัตราแลกเปลี่ยนสกุลเงินการรายงาน (ที่ตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท) จะถูกใช้สำหรับการแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="95c1e-123">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="95c1e-124">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="95c1e-124">Example</span></span>

<span data-ttu-id="95c1e-125">ตัวอย่างแบบง่ายเพื่อสาธิตฟังก์ชันนี้คือ:</span><span class="sxs-lookup"><span data-stu-id="95c1e-125">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="95c1e-126">การตั้งค่าสกุลเงินสำหรับบัญชีแยกประเภทและภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-126">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="95c1e-127">สกุลเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="95c1e-127">Transaction currency</span></span> | <span data-ttu-id="95c1e-128">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="95c1e-128">Accounting currency</span></span> | <span data-ttu-id="95c1e-129">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-129">Reporting currency</span></span> | <span data-ttu-id="95c1e-130">สกุลเงินภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-130">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="95c1e-131">EUR</span><span class="sxs-lookup"><span data-stu-id="95c1e-131">EUR</span></span>                  | <span data-ttu-id="95c1e-132">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="95c1e-132">USD</span></span>                 | <span data-ttu-id="95c1e-133">GBP</span><span class="sxs-lookup"><span data-stu-id="95c1e-133">GBP</span></span>                | <span data-ttu-id="95c1e-134">GBP</span><span class="sxs-lookup"><span data-stu-id="95c1e-134">GBP</span></span>          |

<span data-ttu-id="95c1e-135">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="95c1e-135">Exchange rate</span></span>

| <span data-ttu-id="95c1e-136">สกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="95c1e-136">From currency</span></span> | <span data-ttu-id="95c1e-137">สกุลเงินปลายทาง</span><span class="sxs-lookup"><span data-stu-id="95c1e-137">To currency</span></span> | <span data-ttu-id="95c1e-138">แฟคเตอร์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-138">Factor</span></span> | <span data-ttu-id="95c1e-139">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="95c1e-139">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="95c1e-140">EUR</span><span class="sxs-lookup"><span data-stu-id="95c1e-140">EUR</span></span>           | <span data-ttu-id="95c1e-141">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="95c1e-141">USD</span></span>         | <span data-ttu-id="95c1e-142">1</span><span class="sxs-lookup"><span data-stu-id="95c1e-142">1</span></span>      | <span data-ttu-id="95c1e-143">1.11</span><span class="sxs-lookup"><span data-stu-id="95c1e-143">1.11</span></span>          |
| <span data-ttu-id="95c1e-144">EUR</span><span class="sxs-lookup"><span data-stu-id="95c1e-144">EUR</span></span>           | <span data-ttu-id="95c1e-145">GBP</span><span class="sxs-lookup"><span data-stu-id="95c1e-145">GBP</span></span>         | <span data-ttu-id="95c1e-146">1</span><span class="sxs-lookup"><span data-stu-id="95c1e-146">1</span></span>      | <span data-ttu-id="95c1e-147">0.83</span><span class="sxs-lookup"><span data-stu-id="95c1e-147">0.83</span></span>          |
| <span data-ttu-id="95c1e-148">ดอลลาร์สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="95c1e-148">USD</span></span>           | <span data-ttu-id="95c1e-149">GBP</span><span class="sxs-lookup"><span data-stu-id="95c1e-149">GBP</span></span>         | <span data-ttu-id="95c1e-150">1</span><span class="sxs-lookup"><span data-stu-id="95c1e-150">1</span></span>      | <span data-ttu-id="95c1e-151">0.75</span><span class="sxs-lookup"><span data-stu-id="95c1e-151">0.75</span></span>          |

<span data-ttu-id="95c1e-152">การคำนวณยอดภาษีในตัวเลือกพารามิเตอร์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="95c1e-152">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="95c1e-153">ยอดภาษี = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="95c1e-153">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="95c1e-154">พารามิเตอร์การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="95c1e-154">Sales tax conversion parameters</span></span> | <span data-ttu-id="95c1e-155">สกุลเงินของธุรกรรม (EUR)</span><span class="sxs-lookup"><span data-stu-id="95c1e-155">Transaction currency (EUR)</span></span> | <span data-ttu-id="95c1e-156">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="95c1e-156">Accounting currency (USD)</span></span> | <span data-ttu-id="95c1e-157">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="95c1e-157">Reporting currency (GBP)</span></span> | <span data-ttu-id="95c1e-158">สกุลเงินภาษี (GBP)</span><span class="sxs-lookup"><span data-stu-id="95c1e-158">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="95c1e-159">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="95c1e-159">Accounting currency</span></span>             | <span data-ttu-id="95c1e-160">100</span><span class="sxs-lookup"><span data-stu-id="95c1e-160">100</span></span>                        | <span data-ttu-id="95c1e-161">111</span><span class="sxs-lookup"><span data-stu-id="95c1e-161">111</span></span>                       | <span data-ttu-id="95c1e-162">83</span><span class="sxs-lookup"><span data-stu-id="95c1e-162">83</span></span>                       | <span data-ttu-id="95c1e-163">**83.25**</span><span class="sxs-lookup"><span data-stu-id="95c1e-163">**83.25**</span></span>          |
| <span data-ttu-id="95c1e-164">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-164">Reporting currency</span></span>              | <span data-ttu-id="95c1e-165">100</span><span class="sxs-lookup"><span data-stu-id="95c1e-165">100</span></span>                        | <span data-ttu-id="95c1e-166">111</span><span class="sxs-lookup"><span data-stu-id="95c1e-166">111</span></span>                       | <span data-ttu-id="95c1e-167">83</span><span class="sxs-lookup"><span data-stu-id="95c1e-167">83</span></span>                       | <span data-ttu-id="95c1e-168">**83**</span><span class="sxs-lookup"><span data-stu-id="95c1e-168">**83**</span></span>             |

<span data-ttu-id="95c1e-169">คุณสามารถตั้งค่าคอนฟิกพารามิเตอร์นี้ตามความต้องการในการปฏิบัติตามกฎระเบียบจากหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-169">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="95c1e-170">ข้อควรพิจารณาสำหรับการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="95c1e-170">Upgrade Consideration</span></span>

<span data-ttu-id="95c1e-171">คุณลักษณะจะใช้สำหรับธุรกรรมใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="95c1e-171">This feature will only apply for new transactions.</span></span> <span data-ttu-id="95c1e-172">สำหรับธุรกรรมภาษีที่บันทึกไว้แล้วในตาราง TAXTRANS แล้วแต่ยังไม่ได้ชำระเงิน ระบบจะไม่คำนวณยอดภาษีในสกุลเงินภาษีใหม่ เนื่องจากอัตราแลกเปลี่ยน ณ จุดเวลาของภาษีการลงรายการบัญชีขาดหายไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="95c1e-172">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="95c1e-173">หากต้องการป้องกันสถานการณ์จำลองก่อนหน้านี้ เราขอแนะนำให้เปลี่ยนค่าพารามิเตอร์นี้ในรอบระยะเวลาการชำระภาษีใหม่ (ใหม่ทั้งหมด) ที่ไม่มีธุรกรรมภาษีที่ยังไม่ได้ชำระใดๆ</span><span class="sxs-lookup"><span data-stu-id="95c1e-173">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="95c1e-174">เมื่อต้องการเปลี่ยนค่านี้ในช่วงกลางของรอบระยะเวลาการจ่ายภาษี โปรดรันโปรแกรม "ชำระเงินและลงรายการบัญชีภาษีขาย" สำหรับรอบระยะเวลาการชำระภาษีปัจจุบัน ก่อนที่จะเปลี่ยนค่าพารามิเตอร์นี้</span><span class="sxs-lookup"><span data-stu-id="95c1e-174">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="95c1e-175">ติดตามยอดเงินภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-175">Track reporting currency tax amount</span></span>

<span data-ttu-id="95c1e-176">มีการเพิ่มฟิลด์ใหม่สามฟิลด์ให้กับตารางที่เกี่ยวข้องกับภาษี เพื่อติดตามยอดเงินในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-176">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="95c1e-177">ฟิลด์เหล่านี้อยู่ภายในตาราง TAXUNCOMMITTED และ TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="95c1e-177">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="95c1e-178">TaxAmountRep: ยอดภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-178">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="95c1e-179">TaxBaseAmountRep: ยอดเงินฐานในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-179">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="95c1e-180">TaxInCostPriceRep: ยอดเงินที่ไม่สามารถหักได้ในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-180">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="95c1e-181">สำหรับภาษีที่บันทึกไว้เฉพาะในตาราง TAXUNCOMMITTED แต่ยังไม่ได้ลงรายการบัญชี ระบบจะคำนวณยอดภาษีใหม่ในสกุลเงินการรายงานเมื่อลงรายการบัญชีและบันทึกในตาราง TAXTRANS</span><span class="sxs-lookup"><span data-stu-id="95c1e-181">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="95c1e-182">รุ่นที่นำออกใช้นี้จะไม่มีการเปลี่ยนแปลงในรายงานและฟอร์มที่แสดงยอดภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-182">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="95c1e-183">การเปลี่ยนแปลงไปยังรายงานและฟอร์มจะถูกจัดส่งในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="95c1e-183">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="95c1e-184">ยอดดุลอัตโนมัติของการชำระภาษีในสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-184">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="95c1e-185">ถ้าการชำระภาษีไม่สมดุลในสกุลเงินการรายงานเนื่องจากเหตุผลบางประการ เช่น พาธการแปลงภาษีขายคือ "สกุลเงินทางบัญชี" หรือการเปลี่ยนแปลงอัตราแลกเปลี่ยนในรอบระยะเวลาการชำระภาษีหนึ่งๆ จากนั้น ระบบจะสร้างรายการบัญชีโดยอัตโนมัติเพื่อปรับผลต่างของยอดเงินภาษีและออฟเซ็ตเทียบกับบัญชีกำไร/ขาดทุนที่รับรู้จากอัตราแลกเปลี่ยน ซึ่งถูกตั้งค่าคอนฟิกในการตั้งค่าบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="95c1e-185">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="95c1e-186">การใช้ตัวอย่างก่อนหน้านี้แสดงให้เห็นถึงคุณลักษณะนี้ สมมติว่าข้อมูลในตาราง TAXTRANS ในเวลาที่ลงรายการบัญชีเป็นดังนี้</span><span class="sxs-lookup"><span data-stu-id="95c1e-186">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="95c1e-187">พารามิเตอร์การแปลงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="95c1e-187">Sales tax conversion parameters</span></span> | <span data-ttu-id="95c1e-188">สกุลเงินของธุรกรรม (EUR)</span><span class="sxs-lookup"><span data-stu-id="95c1e-188">Transaction currency (EUR)</span></span> | <span data-ttu-id="95c1e-189">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="95c1e-189">Accounting currency (USD)</span></span> | <span data-ttu-id="95c1e-190">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="95c1e-190">Reporting currency (GBP)</span></span> | <span data-ttu-id="95c1e-191">สกุลเงินภาษี (GBP)</span><span class="sxs-lookup"><span data-stu-id="95c1e-191">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="95c1e-192">สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="95c1e-192">Accounting currency</span></span>             | <span data-ttu-id="95c1e-193">100</span><span class="sxs-lookup"><span data-stu-id="95c1e-193">100</span></span>                        | <span data-ttu-id="95c1e-194">111</span><span class="sxs-lookup"><span data-stu-id="95c1e-194">111</span></span>                       | <span data-ttu-id="95c1e-195">83</span><span class="sxs-lookup"><span data-stu-id="95c1e-195">83</span></span>                       | <span data-ttu-id="95c1e-196">**83.25**</span><span class="sxs-lookup"><span data-stu-id="95c1e-196">**83.25**</span></span>          |
| <span data-ttu-id="95c1e-197">สกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="95c1e-197">Reporting currency</span></span>              | <span data-ttu-id="95c1e-198">100</span><span class="sxs-lookup"><span data-stu-id="95c1e-198">100</span></span>                        | <span data-ttu-id="95c1e-199">111</span><span class="sxs-lookup"><span data-stu-id="95c1e-199">111</span></span>                       | <span data-ttu-id="95c1e-200">83</span><span class="sxs-lookup"><span data-stu-id="95c1e-200">83</span></span>                       | <span data-ttu-id="95c1e-201">**83**</span><span class="sxs-lookup"><span data-stu-id="95c1e-201">**83**</span></span>             |

<span data-ttu-id="95c1e-202">เมื่อคุณรันโปรแกรมการชำระภาษีขายในช่วงสิ้นเดือน รายการบัญชีจะเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="95c1e-202">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="95c1e-203">สถานการณ์จำลอง: การแปลงภาษีขาย = "สกุลเงินทางบัญชี"</span><span class="sxs-lookup"><span data-stu-id="95c1e-203">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="95c1e-204">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="95c1e-204">Main account</span></span>           | <span data-ttu-id="95c1e-205">สกุลเงินของธุรกรรม (GBP)</span><span class="sxs-lookup"><span data-stu-id="95c1e-205">Transaction currency (GBP)</span></span> | <span data-ttu-id="95c1e-206">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="95c1e-206">Accounting currency (USD)</span></span> | <span data-ttu-id="95c1e-207">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="95c1e-207">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="95c1e-208">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-208">Tax Payable/Receivable</span></span> | <span data-ttu-id="95c1e-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="95c1e-209">-83.25</span></span>                     | <span data-ttu-id="95c1e-210">-111</span><span class="sxs-lookup"><span data-stu-id="95c1e-210">-111</span></span>                      | <span data-ttu-id="95c1e-211">-83.25</span><span class="sxs-lookup"><span data-stu-id="95c1e-211">-83.25</span></span>                   |
| <span data-ttu-id="95c1e-212">การชำระภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-212">Tax Settlement</span></span>         | <span data-ttu-id="95c1e-213">83.25</span><span class="sxs-lookup"><span data-stu-id="95c1e-213">83.25</span></span>                      | <span data-ttu-id="95c1e-214">111</span><span class="sxs-lookup"><span data-stu-id="95c1e-214">111</span></span>                       | <span data-ttu-id="95c1e-215">83.25</span><span class="sxs-lookup"><span data-stu-id="95c1e-215">83.25</span></span>                    |
| <span data-ttu-id="95c1e-216">กำไร/ขาดทุนที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="95c1e-216">Realized Gain/Loss</span></span>     | <span data-ttu-id="95c1e-217">0</span><span class="sxs-lookup"><span data-stu-id="95c1e-217">0</span></span>                          | <span data-ttu-id="95c1e-218">0</span><span class="sxs-lookup"><span data-stu-id="95c1e-218">0</span></span>                         | <span data-ttu-id="95c1e-219">-0.25</span><span class="sxs-lookup"><span data-stu-id="95c1e-219">-0.25</span></span>                    |
| <span data-ttu-id="95c1e-220">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-220">Tax Payable/Receivable</span></span> | <span data-ttu-id="95c1e-221">0</span><span class="sxs-lookup"><span data-stu-id="95c1e-221">0</span></span>                          | <span data-ttu-id="95c1e-222">0</span><span class="sxs-lookup"><span data-stu-id="95c1e-222">0</span></span>                         | <span data-ttu-id="95c1e-223">0.25</span><span class="sxs-lookup"><span data-stu-id="95c1e-223">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="95c1e-224">สถานการณ์จำลอง: การแปลงภาษีขาย = "สกุลเงินการรายงาน"</span><span class="sxs-lookup"><span data-stu-id="95c1e-224">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="95c1e-225">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="95c1e-225">Main account</span></span>           | <span data-ttu-id="95c1e-226">สกุลเงินของธุรกรรม (GBP)</span><span class="sxs-lookup"><span data-stu-id="95c1e-226">Transaction currency (GBP)</span></span> | <span data-ttu-id="95c1e-227">สกุลเงินการบัญชี (USD)</span><span class="sxs-lookup"><span data-stu-id="95c1e-227">Accounting currency (USD)</span></span> | <span data-ttu-id="95c1e-228">สกุลเงินการรายงาน (GBP)</span><span class="sxs-lookup"><span data-stu-id="95c1e-228">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="95c1e-229">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-229">Tax Payable/Receivable</span></span> | <span data-ttu-id="95c1e-230">-83</span><span class="sxs-lookup"><span data-stu-id="95c1e-230">-83</span></span>                        | <span data-ttu-id="95c1e-231">-110.67</span><span class="sxs-lookup"><span data-stu-id="95c1e-231">-110.67</span></span>                   | <span data-ttu-id="95c1e-232">-83</span><span class="sxs-lookup"><span data-stu-id="95c1e-232">-83</span></span>                      |
| <span data-ttu-id="95c1e-233">การชำระภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-233">Tax Settlement</span></span>         | <span data-ttu-id="95c1e-234">83</span><span class="sxs-lookup"><span data-stu-id="95c1e-234">83</span></span>                         | <span data-ttu-id="95c1e-235">110.67</span><span class="sxs-lookup"><span data-stu-id="95c1e-235">110.67</span></span>                    | <span data-ttu-id="95c1e-236">83</span><span class="sxs-lookup"><span data-stu-id="95c1e-236">83</span></span>                       |
| <span data-ttu-id="95c1e-237">กำไร/ขาดทุนที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="95c1e-237">Realized Gain/Loss</span></span>     | <span data-ttu-id="95c1e-238">0</span><span class="sxs-lookup"><span data-stu-id="95c1e-238">0</span></span>                          | <span data-ttu-id="95c1e-239">0.33</span><span class="sxs-lookup"><span data-stu-id="95c1e-239">0.33</span></span>                      | <span data-ttu-id="95c1e-240">0</span><span class="sxs-lookup"><span data-stu-id="95c1e-240">0</span></span>                        |
| <span data-ttu-id="95c1e-241">เจ้าหนี้/ลูกหนี้ภาษี</span><span class="sxs-lookup"><span data-stu-id="95c1e-241">Tax Payable/Receivable</span></span> | <span data-ttu-id="95c1e-242">0</span><span class="sxs-lookup"><span data-stu-id="95c1e-242">0</span></span>                          | <span data-ttu-id="95c1e-243">-0.33</span><span class="sxs-lookup"><span data-stu-id="95c1e-243">-0.33</span></span>                     | <span data-ttu-id="95c1e-244">0</span><span class="sxs-lookup"><span data-stu-id="95c1e-244">0</span></span>                        |



<span data-ttu-id="95c1e-245">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="95c1e-245">For more information, see the following topics:</span></span>

- [<span data-ttu-id="95c1e-246">สกุลเงินแบบคู่</span><span class="sxs-lookup"><span data-stu-id="95c1e-246">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="95c1e-247">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="95c1e-247">Sales tax overview</span></span>](indirect-taxes-overview.md)

