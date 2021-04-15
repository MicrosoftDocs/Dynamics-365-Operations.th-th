---
title: ใช้มากกว่าส่วนลดที่คำนวณได้สำหรับการชำระเงินของผู้จัดจำหน่าย
description: บทความนี้แนะนำคุณผ่านสถานการณ์สมมติเมื่อรับส่วนลดเงินสดสำหรับยอดเงินที่เพิ่มเติมจากส่วนลดที่มีไว้เดิมในใบแจ้งหนี้ สถานการณ์นี้อาจเกิดขึ้นถ้าองค์กรตกลงกับผู้จัดจำหน่ายในการชำระเงินน้อยกว่าบนใบแจ้งหนี้
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810257"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="50c0f-104">ใช้มากกว่าส่วนลดที่คำนวณได้สำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="50c0f-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50c0f-105">บทความนี้แนะนำคุณผ่านสถานการณ์สมมติเมื่อรับส่วนลดเงินสดสำหรับยอดเงินที่เพิ่มเติมจากส่วนลดที่มีไว้เดิมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="50c0f-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="50c0f-106">สถานการณ์นี้อาจเกิดขึ้นถ้าองค์กรตกลงกับผู้จัดจำหน่ายในการชำระเงินน้อยกว่าบนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="50c0f-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="50c0f-107">ผู้จัดจำหน่าย 3051 ให้ส่วนลดเงินสด 4 เปอร์เซ็นต์ แก่ Fabrikam หากใบแจ้งหนี้ถูกชำระภายในเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="50c0f-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="50c0f-108">ในวันที่ 29 มิถุนายน เดือนเมษายนป้อนใบแจ้งหนี้เป็นจำนวนเงิน 1,000.00</span><span class="sxs-lookup"><span data-stu-id="50c0f-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="50c0f-109">ผู้จัดจำหน่ายให้เดือนเมษายนใช้ส่วนลด 60.00 แทนที่เป็นส่วนลดเริ่มต้น 40.00 ที่พร้อมใช้งานสำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="50c0f-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="50c0f-110">เดือนเมษายนจะเรกคอร์ดการชำระเงินที่ใช้ครั้งเดียว โดยใช้สมุดรายวันการชำระเงินของบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="50c0f-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="50c0f-111">เธอป้อนการชำระเงินให้แก่ผู้จัดจำหน่าย และจากนั้น เปิดหน้า **ชำระธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="50c0f-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="50c0f-112">เธอทำเครื่องหมายใบแจ้งหนี้ และเปลี่ยนแปลงมูลค่าในฟิลด์ **จำนวนส่วนลดเงินสด** เป็น **60.00**</span><span class="sxs-lookup"><span data-stu-id="50c0f-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="50c0f-113">ทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="50c0f-113">Mark</span></span>     | <span data-ttu-id="50c0f-114">ใช้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="50c0f-114">Use cash discount</span></span> | <span data-ttu-id="50c0f-115">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="50c0f-115">Voucher</span></span>   | <span data-ttu-id="50c0f-116">บัญชี</span><span class="sxs-lookup"><span data-stu-id="50c0f-116">Account</span></span> | <span data-ttu-id="50c0f-117">วันที่</span><span class="sxs-lookup"><span data-stu-id="50c0f-117">Date</span></span>      | <span data-ttu-id="50c0f-118">วันที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="50c0f-118">Due date</span></span>  | <span data-ttu-id="50c0f-119">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="50c0f-119">Invoice</span></span> | <span data-ttu-id="50c0f-120">ยอดเงินในสกุลเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="50c0f-120">Amount in transaction currency</span></span> | <span data-ttu-id="50c0f-121">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="50c0f-121">Currency</span></span> | <span data-ttu-id="50c0f-122">ยอดเงินที่จะชำระ</span><span class="sxs-lookup"><span data-stu-id="50c0f-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="50c0f-123">เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="50c0f-123">Selected</span></span> | <span data-ttu-id="50c0f-124">ปกติ</span><span class="sxs-lookup"><span data-stu-id="50c0f-124">Normal</span></span>            | <span data-ttu-id="50c0f-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="50c0f-125">Inv-10040</span></span> | <span data-ttu-id="50c0f-126">3051</span><span class="sxs-lookup"><span data-stu-id="50c0f-126">3051</span></span>    | <span data-ttu-id="50c0f-127">วันที่ 29 มิถุนายน 2015</span><span class="sxs-lookup"><span data-stu-id="50c0f-127">6/29/2015</span></span> | <span data-ttu-id="50c0f-128">วันที่ 29 กรกฎาคม 2015</span><span class="sxs-lookup"><span data-stu-id="50c0f-128">7/29/2015</span></span> | <span data-ttu-id="50c0f-129">10040</span><span class="sxs-lookup"><span data-stu-id="50c0f-129">10040</span></span>   | <span data-ttu-id="50c0f-130">1,000.00</span><span class="sxs-lookup"><span data-stu-id="50c0f-130">1,000.00</span></span>                       | <span data-ttu-id="50c0f-131">USD</span><span class="sxs-lookup"><span data-stu-id="50c0f-131">USD</span></span>      | <span data-ttu-id="50c0f-132">940.00</span><span class="sxs-lookup"><span data-stu-id="50c0f-132">940.00</span></span>           |

<span data-ttu-id="50c0f-133">ข้อมูลส่วนลดที่ปรากฏขึ้นที่ด้านล่างของหน้า **ธุรกรรมการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="50c0f-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

| <span data-ttu-id="50c0f-134">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="50c0f-134">Field</span></span>                        | <span data-ttu-id="50c0f-135">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="50c0f-135">Value</span></span>     |
|------------------------------|-----------|
| <span data-ttu-id="50c0f-136">วันที่ให้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="50c0f-136">Cash discount date</span></span>           | <span data-ttu-id="50c0f-137">วันที่ 12 กรกฏาคม 2015</span><span class="sxs-lookup"><span data-stu-id="50c0f-137">7/12/2015</span></span> |
| <span data-ttu-id="50c0f-138">ยอดส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="50c0f-138">Cash discount amount</span></span>         | <span data-ttu-id="50c0f-139">60.00</span><span class="sxs-lookup"><span data-stu-id="50c0f-139">60.00</span></span>     |
| <span data-ttu-id="50c0f-140">ใช้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="50c0f-140">Use cash discount</span></span>            | <span data-ttu-id="50c0f-141">ปกติ</span><span class="sxs-lookup"><span data-stu-id="50c0f-141">Normal</span></span>    |
| <span data-ttu-id="50c0f-142">ส่วนลดเงินสดที่ใช้</span><span class="sxs-lookup"><span data-stu-id="50c0f-142">Cash discount taken</span></span>          | <span data-ttu-id="50c0f-143">0.00</span><span class="sxs-lookup"><span data-stu-id="50c0f-143">0.00</span></span>      |
| <span data-ttu-id="50c0f-144">ยอดส่วนลดเงินสดที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="50c0f-144">Cash discount amount to take</span></span> | <span data-ttu-id="50c0f-145">60.00</span><span class="sxs-lookup"><span data-stu-id="50c0f-145">60.00</span></span>     |

<span data-ttu-id="50c0f-146">เดือนเมษายนลงรายการบัญชีสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="50c0f-146">April posts the payment journal.</span></span> <span data-ttu-id="50c0f-147">ใบแจ้งหนี้ถูกชำระเต็มจำนวน โดยใช้การชำระเงิน 940.00 และส่วนลด 60.00</span><span class="sxs-lookup"><span data-stu-id="50c0f-147">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]