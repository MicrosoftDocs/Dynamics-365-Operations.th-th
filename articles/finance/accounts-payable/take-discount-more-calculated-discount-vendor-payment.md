---
title: ใช้มากกว่าส่วนลดที่คำนวณได้สำหรับการชำระเงินของผู้จัดจำหน่าย
description: บทความนี้แนะนำคุณผ่านสถานการณ์สมมติเมื่อรับส่วนลดเงินสดสำหรับยอดเงินที่เพิ่มเติมจากส่วนลดที่มีไว้เดิมในใบแจ้งหนี้ สถานการณ์นี้อาจเกิดขึ้นถ้าองค์กรตกลงกับผู้จัดจำหน่ายในการชำระเงินน้อยกว่าบนใบแจ้งหนี้
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2a56331f76867aeac0bad0912749d96f959513e0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235896"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="90b9c-104">ใช้มากกว่าส่วนลดที่คำนวณได้สำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="90b9c-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90b9c-105">บทความนี้แนะนำคุณผ่านสถานการณ์สมมติเมื่อรับส่วนลดเงินสดสำหรับยอดเงินที่เพิ่มเติมจากส่วนลดที่มีไว้เดิมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90b9c-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="90b9c-106">สถานการณ์นี้อาจเกิดขึ้นถ้าองค์กรตกลงกับผู้จัดจำหน่ายในการชำระเงินน้อยกว่าบนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90b9c-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="90b9c-107">ผู้จัดจำหน่าย 3051 ให้ส่วนลดเงินสด 4 เปอร์เซ็นต์ แก่ Fabrikam หากใบแจ้งหนี้ถูกชำระภายในเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="90b9c-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="90b9c-108">ในวันที่ 29 มิถุนายน เดือนเมษายนป้อนใบแจ้งหนี้เป็นจำนวนเงิน 1,000.00</span><span class="sxs-lookup"><span data-stu-id="90b9c-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="90b9c-109">ผู้จัดจำหน่ายให้เดือนเมษายนใช้ส่วนลด 60.00 แทนที่เป็นส่วนลดเริ่มต้น 40.00 ที่พร้อมใช้งานสำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90b9c-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="90b9c-110">เดือนเมษายนจะเรกคอร์ดการชำระเงินที่ใช้ครั้งเดียว โดยใช้สมุดรายวันการชำระเงินของบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="90b9c-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="90b9c-111">เธอป้อนการชำระเงินให้แก่ผู้จัดจำหน่าย และจากนั้น เปิดหน้า **ชำระธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="90b9c-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="90b9c-112">เธอทำเครื่องหมายใบแจ้งหนี้ และเปลี่ยนแปลงมูลค่าในฟิลด์ **จำนวนส่วนลดเงินสด** เป็น **60.00**</span><span class="sxs-lookup"><span data-stu-id="90b9c-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="90b9c-113">ทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="90b9c-113">Mark</span></span>     | <span data-ttu-id="90b9c-114">ใช้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="90b9c-114">Use cash discount</span></span> | <span data-ttu-id="90b9c-115">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="90b9c-115">Voucher</span></span>   | <span data-ttu-id="90b9c-116">บัญชี</span><span class="sxs-lookup"><span data-stu-id="90b9c-116">Account</span></span> | <span data-ttu-id="90b9c-117">วันที่</span><span class="sxs-lookup"><span data-stu-id="90b9c-117">Date</span></span>      | <span data-ttu-id="90b9c-118">วันที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="90b9c-118">Due date</span></span>  | <span data-ttu-id="90b9c-119">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90b9c-119">Invoice</span></span> | <span data-ttu-id="90b9c-120">ยอดเงินในสกุลเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="90b9c-120">Amount in transaction currency</span></span> | <span data-ttu-id="90b9c-121">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="90b9c-121">Currency</span></span> | <span data-ttu-id="90b9c-122">ยอดเงินที่จะชำระ</span><span class="sxs-lookup"><span data-stu-id="90b9c-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="90b9c-123">เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="90b9c-123">Selected</span></span> | <span data-ttu-id="90b9c-124">ปกติ</span><span class="sxs-lookup"><span data-stu-id="90b9c-124">Normal</span></span>            | <span data-ttu-id="90b9c-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="90b9c-125">Inv-10040</span></span> | <span data-ttu-id="90b9c-126">3051</span><span class="sxs-lookup"><span data-stu-id="90b9c-126">3051</span></span>    | <span data-ttu-id="90b9c-127">วันที่ 29 มิถุนายน 2015</span><span class="sxs-lookup"><span data-stu-id="90b9c-127">6/29/2015</span></span> | <span data-ttu-id="90b9c-128">วันที่ 29 กรกฎาคม 2015</span><span class="sxs-lookup"><span data-stu-id="90b9c-128">7/29/2015</span></span> | <span data-ttu-id="90b9c-129">10040</span><span class="sxs-lookup"><span data-stu-id="90b9c-129">10040</span></span>   | <span data-ttu-id="90b9c-130">1,000.00</span><span class="sxs-lookup"><span data-stu-id="90b9c-130">1,000.00</span></span>                       | <span data-ttu-id="90b9c-131">USD</span><span class="sxs-lookup"><span data-stu-id="90b9c-131">USD</span></span>      | <span data-ttu-id="90b9c-132">940.00</span><span class="sxs-lookup"><span data-stu-id="90b9c-132">940.00</span></span>           |

<span data-ttu-id="90b9c-133">ข้อมูลส่วนลดที่ปรากฏขึ้นที่ด้านล่างของหน้า **ธุรกรรมการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="90b9c-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="90b9c-134">วันที่ให้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="90b9c-134">Cash discount date</span></span>           | <span data-ttu-id="90b9c-135">วันที่ 12 กรกฏาคม 2015</span><span class="sxs-lookup"><span data-stu-id="90b9c-135">7/12/2015</span></span> |
| <span data-ttu-id="90b9c-136">ยอดส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="90b9c-136">Cash discount amount</span></span>         | <span data-ttu-id="90b9c-137">60.00</span><span class="sxs-lookup"><span data-stu-id="90b9c-137">60.00</span></span>     |
| <span data-ttu-id="90b9c-138">ใช้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="90b9c-138">Use cash discount</span></span>            | <span data-ttu-id="90b9c-139">ปกติ</span><span class="sxs-lookup"><span data-stu-id="90b9c-139">Normal</span></span>    |
| <span data-ttu-id="90b9c-140">ส่วนลดเงินสดที่ใช้</span><span class="sxs-lookup"><span data-stu-id="90b9c-140">Cash discount taken</span></span>          | <span data-ttu-id="90b9c-141">0.00</span><span class="sxs-lookup"><span data-stu-id="90b9c-141">0.00</span></span>      |
| <span data-ttu-id="90b9c-142">ยอดส่วนลดเงินสดที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="90b9c-142">Cash discount amount to take</span></span> | <span data-ttu-id="90b9c-143">60.00</span><span class="sxs-lookup"><span data-stu-id="90b9c-143">60.00</span></span>     |

<span data-ttu-id="90b9c-144">เดือนเมษายนลงรายการบัญชีสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="90b9c-144">April posts the payment journal.</span></span> <span data-ttu-id="90b9c-145">ใบแจ้งหนี้ถูกชำระเต็มจำนวน โดยใช้การชำระเงิน 940.00 และส่วนลด 60.00</span><span class="sxs-lookup"><span data-stu-id="90b9c-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]