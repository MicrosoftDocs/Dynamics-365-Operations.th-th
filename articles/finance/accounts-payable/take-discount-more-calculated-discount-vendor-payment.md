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
ms.openlocfilehash: c7ee74bad071d546724f6ffe336bbe3bdf47e2a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971914"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="56406-104">ใช้มากกว่าส่วนลดที่คำนวณได้สำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="56406-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56406-105">บทความนี้แนะนำคุณผ่านสถานการณ์สมมติเมื่อรับส่วนลดเงินสดสำหรับยอดเงินที่เพิ่มเติมจากส่วนลดที่มีไว้เดิมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="56406-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="56406-106">สถานการณ์นี้อาจเกิดขึ้นถ้าองค์กรตกลงกับผู้จัดจำหน่ายในการชำระเงินน้อยกว่าบนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="56406-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="56406-107">ผู้จัดจำหน่าย 3051 ให้ส่วนลดเงินสด 4 เปอร์เซ็นต์ แก่ Fabrikam หากใบแจ้งหนี้ถูกชำระภายในเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="56406-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="56406-108">ในวันที่ 29 มิถุนายน เดือนเมษายนป้อนใบแจ้งหนี้เป็นจำนวนเงิน 1,000.00</span><span class="sxs-lookup"><span data-stu-id="56406-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="56406-109">ผู้จัดจำหน่ายให้เดือนเมษายนใช้ส่วนลด 60.00 แทนที่เป็นส่วนลดเริ่มต้น 40.00 ที่พร้อมใช้งานสำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="56406-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="56406-110">เดือนเมษายนจะเรกคอร์ดการชำระเงินที่ใช้ครั้งเดียว โดยใช้สมุดรายวันการชำระเงินของบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="56406-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="56406-111">เธอป้อนการชำระเงินให้แก่ผู้จัดจำหน่าย และจากนั้น เปิดหน้า **ชำระธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="56406-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="56406-112">เธอทำเครื่องหมายใบแจ้งหนี้ และเปลี่ยนแปลงมูลค่าในฟิลด์ **จำนวนส่วนลดเงินสด** เป็น **60.00**</span><span class="sxs-lookup"><span data-stu-id="56406-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="56406-113">ทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="56406-113">Mark</span></span>     | <span data-ttu-id="56406-114">ใช้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="56406-114">Use cash discount</span></span> | <span data-ttu-id="56406-115">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="56406-115">Voucher</span></span>   | <span data-ttu-id="56406-116">บัญชี</span><span class="sxs-lookup"><span data-stu-id="56406-116">Account</span></span> | <span data-ttu-id="56406-117">วันที่</span><span class="sxs-lookup"><span data-stu-id="56406-117">Date</span></span>      | <span data-ttu-id="56406-118">วันที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="56406-118">Due date</span></span>  | <span data-ttu-id="56406-119">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="56406-119">Invoice</span></span> | <span data-ttu-id="56406-120">ยอดเงินในสกุลเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="56406-120">Amount in transaction currency</span></span> | <span data-ttu-id="56406-121">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="56406-121">Currency</span></span> | <span data-ttu-id="56406-122">ยอดเงินที่จะชำระ</span><span class="sxs-lookup"><span data-stu-id="56406-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="56406-123">เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="56406-123">Selected</span></span> | <span data-ttu-id="56406-124">ปกติ</span><span class="sxs-lookup"><span data-stu-id="56406-124">Normal</span></span>            | <span data-ttu-id="56406-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="56406-125">Inv-10040</span></span> | <span data-ttu-id="56406-126">3051</span><span class="sxs-lookup"><span data-stu-id="56406-126">3051</span></span>    | <span data-ttu-id="56406-127">วันที่ 29 มิถุนายน 2015</span><span class="sxs-lookup"><span data-stu-id="56406-127">6/29/2015</span></span> | <span data-ttu-id="56406-128">วันที่ 29 กรกฎาคม 2015</span><span class="sxs-lookup"><span data-stu-id="56406-128">7/29/2015</span></span> | <span data-ttu-id="56406-129">10040</span><span class="sxs-lookup"><span data-stu-id="56406-129">10040</span></span>   | <span data-ttu-id="56406-130">1,000.00</span><span class="sxs-lookup"><span data-stu-id="56406-130">1,000.00</span></span>                       | <span data-ttu-id="56406-131">USD</span><span class="sxs-lookup"><span data-stu-id="56406-131">USD</span></span>      | <span data-ttu-id="56406-132">940.00</span><span class="sxs-lookup"><span data-stu-id="56406-132">940.00</span></span>           |

<span data-ttu-id="56406-133">ข้อมูลส่วนลดที่ปรากฏขึ้นที่ด้านล่างของหน้า **ธุรกรรมการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="56406-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="56406-134">วันที่ให้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="56406-134">Cash discount date</span></span>           | <span data-ttu-id="56406-135">วันที่ 12 กรกฏาคม 2015</span><span class="sxs-lookup"><span data-stu-id="56406-135">7/12/2015</span></span> |
| <span data-ttu-id="56406-136">ยอดส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="56406-136">Cash discount amount</span></span>         | <span data-ttu-id="56406-137">60.00</span><span class="sxs-lookup"><span data-stu-id="56406-137">60.00</span></span>     |
| <span data-ttu-id="56406-138">ใช้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="56406-138">Use cash discount</span></span>            | <span data-ttu-id="56406-139">ปกติ</span><span class="sxs-lookup"><span data-stu-id="56406-139">Normal</span></span>    |
| <span data-ttu-id="56406-140">ส่วนลดเงินสดที่ใช้</span><span class="sxs-lookup"><span data-stu-id="56406-140">Cash discount taken</span></span>          | <span data-ttu-id="56406-141">0.00</span><span class="sxs-lookup"><span data-stu-id="56406-141">0.00</span></span>      |
| <span data-ttu-id="56406-142">ยอดส่วนลดเงินสดที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="56406-142">Cash discount amount to take</span></span> | <span data-ttu-id="56406-143">60.00</span><span class="sxs-lookup"><span data-stu-id="56406-143">60.00</span></span>     |

<span data-ttu-id="56406-144">เดือนเมษายนลงรายการบัญชีสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="56406-144">April posts the payment journal.</span></span> <span data-ttu-id="56406-145">ใบแจ้งหนี้ถูกชำระเต็มจำนวน โดยใช้การชำระเงิน 940.00 และส่วนลด 60.00</span><span class="sxs-lookup"><span data-stu-id="56406-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



