---
title: "ส่วนลดเงินสด"
description: "บัญชีเจ้าหนี้และบัญชีลูกหนี้มีการกำหนดและใช้ส่วนลดเงินสดร่วมกัน  ส่วนลดเงินสดสามารถกำหนดในใบแจ้งหนี้ของลูกค้าหรือใบแจ้งหนี้ของผู้จัดจำหน่าย และจะได้รับหากชำระใบแจ้งหนี้ภายในวันที่ให้ส่วนลดเงินสด"
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 52e6003dfddc398c19055405bf936195febe0737
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="cash-discounts"></a><span data-ttu-id="e5bf7-104">ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="e5bf7-104">Cash discounts</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e5bf7-105">บัญชีเจ้าหนี้และบัญชีลูกหนี้มีการกำหนดและใช้ส่วนลดเงินสดร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="e5bf7-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="e5bf7-106">ส่วนลดเงินสดสามารถกำหนดในใบแจ้งหนี้ของลูกค้าหรือใบแจ้งหนี้ของผู้จัดจำหน่าย และจะได้รับหากชำระใบแจ้งหนี้ภายในวันที่ให้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="e5bf7-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

<a name="cash-discounts"></a><span data-ttu-id="e5bf7-107">ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="e5bf7-107">Cash discounts</span></span>
--------------

<span data-ttu-id="e5bf7-108">สามารถสร้างส่วนลดเงินสดสำหรับทั้งลูกค้าหรือผู้จัดจำหน่ายในหน้าส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="e5bf7-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="e5bf7-109">คุณยังสามารถกำหนด โดยการใช้ฟิลด์รหัสส่วนลดถัดไป ชุดของส่วนลดเงินสดที่สำเร็จอื่นๆตามวันหมดอายุส่วนลดเงินสดก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="e5bf7-110">สำหรับข้อมูลเพิ่มเติม ดู "ตัวอย่าง: ชุดของส่วนลดเงินสด" ภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="e5bf7-111">ถ้าใบแจ้งหนี้ ธุรกรรมเครดิต (การชำระเงินหรือใบลดหนี้), หรือทั้งสองอย่างถูกป้อนในสกุลเงินอื่นนอกเหนือจากสกุลเงินทางบัญชีของนิติบุคคล ส่วนลดเงินสดจะถูกคำนวณโดยการใช้อัตราแลกเปลี่ยน ตามวันที่ของการชำระเงินหรือใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="e5bf7-112">ถ้ามีป้อนเอกสารใบแจ้งหนี้และเครดิตในนิติบุคคลอื่น และถ้าสกุลเงินทางบัญชีสำหรับนิติบุคคลแตกต่างกัน อัตราแลกเปลี่ยนจะนำมาจากนิติบุคคลของใบแจ้งหนี้ ตามวันที่ของเอกสารเครดิต</span><span class="sxs-lookup"><span data-stu-id="e5bf7-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="e5bf7-113">สำหรับข้อมูลเพิ่มเติม ดู "ตัวอย่าง: อัตราแลกเปลี่ยนสำหรับส่วนลดเงินสด" ภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>
<span data-ttu-id="e5bf7-114">ค่าเริ่มต้นใบสั่งของบัญชีหลักของส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="e5bf7-114">Defaulting order of cash discount main account</span></span>
----------------------------------------------

<span data-ttu-id="e5bf7-115">ถ้ามีการชำระเงินตามใบแจ้งหนี้ภายในเวลาที่จะได้รับส่วนลดเงินสด จะมีการลงรายการบัญชีส่วนลดเงินสดโดยอัตโนมัติที่บัญชีหลักของส่วนลดเงินสดตามระดับความสำคัญของค่าเริ่มต้นต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="e5bf7-116">บัญชีหลักที่ระบุในฟิลด์บัญชีส่วนลดเงินสดอื่นบนหน้าชำระธุรกรรมที่ค้างอยู่ของลูกค้าหรือหน้าชำระธุรกรรมที่ค้างอยู่ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e5bf7-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="e5bf7-117">บัญชีหลักที่ระบุในฟิลด์ส่วนลดเงินสดสำหรับลูกค้าหรือฟิลด์ส่วนลดเงินสดของผู้จัดจำหน่ายของกลุ่มการลงรายการบัญชีแยกประเภทที่กำหนดให้กับรหัสภาษีขายของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="e5bf7-118">ตั้งค่ากลุ่มการลงรายการบัญชีแยกประเภทบนหน้ากลุ่มการลงรายการบัญชีแยกประเภทและกำหนดให้กับรหัสภาษีขายในหน้ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e5bf7-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="e5bf7-119">บัญชีลงรายการบัญชีหลักบนหน้าส่วนลดเงินสดในบัญชีหลักสำหรับฟิลด์ส่วนลดของลูกค้าหรือบัญชีหลักสำหรับฟิลด์ส่วนลดของผู้จัดจำหน่ายสำหรับรหัสส่วนลดเงินสดที่อยู่บนใบแจ้งหนี้ที่ชำระแล้ว</span><span class="sxs-lookup"><span data-stu-id="e5bf7-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="e5bf7-120">บัญชีหลักสำหรับส่วนลดเงินสด ตามที่กำหนดไว้ในหน้าบัญชีสำหรับธุรกรรมอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e5bf7-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="e5bf7-121"> ตัวอย่าง: ชุดของส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="e5bf7-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="e5bf7-122">ตั้งค่ารหัสส่วนลดเงินสดสามรหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="e5bf7-123">รหัส 5D10% - ส่วนลดเงินสด 10% เมื่อชำระเงินภายใน 5 วัน</span><span class="sxs-lookup"><span data-stu-id="e5bf7-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="e5bf7-124">รหัส 10D5% - ส่วนลดเงินสด 5% เมื่อชำระเงินภายใน 10 วัน</span><span class="sxs-lookup"><span data-stu-id="e5bf7-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="e5bf7-125">รหัส 14D2% - ส่วนลดเงินสด 2% เมื่อชำระเงินภายใน 14 วัน</span><span class="sxs-lookup"><span data-stu-id="e5bf7-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="e5bf7-126">ในฟิลด์รหัสส่วนลดถัดไป:</span><span class="sxs-lookup"><span data-stu-id="e5bf7-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="e5bf7-127">สำหรับรหัส 5D10% ให้เลือก 10D5%</span><span class="sxs-lookup"><span data-stu-id="e5bf7-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="e5bf7-128">สำหรับรหัส 10D5% ให้เลือก 14D2%</span><span class="sxs-lookup"><span data-stu-id="e5bf7-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="e5bf7-129">สำหรับรหัส 14D2% ให้ปล่อยให้ฟิลด์รหัสส่วนลดถัดไปเว้นว่างไว้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="e5bf7-130">ส่วนลดเงินสดทั้งสามจะต่อเนื่องกันตามวันชำระเงินเกินวันส่วนลดเงินสดก่อนหน้านี้บนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="e5bf7-131">มีการให้ส่วนลดเงินสดเพียงส่วนลดเดียวเท่านั้นเมื่อมีการชำระเงินตามใบแจ้งหนี้ ตามวันของส่วนลดเงินสดที่จะเป็นไปตามลำดับส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="e5bf7-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="e5bf7-132"> ตัวอย่าง: อัตราแลกเปลี่ยนสำหรับส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="e5bf7-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="e5bf7-133">สกุลเงินทางบัญชีนิติบุคคลของคุณคือ EUR และอัตราแลกเปลี่ยนต่อไปนี้จะระบุสำหรับ USD:</span><span class="sxs-lookup"><span data-stu-id="e5bf7-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="e5bf7-134">กุมภาพันธ์ 1 = 110</span><span class="sxs-lookup"><span data-stu-id="e5bf7-134">February 1 = 110</span></span>
-   <span data-ttu-id="e5bf7-135">1 มีนาคม = 80</span><span class="sxs-lookup"><span data-stu-id="e5bf7-135">March 1 = 80</span></span>

<span data-ttu-id="e5bf7-136">ใบแจ้งหนี้สำหรับ USD 1000 กับเงื่อนไขส่วนลดเงินสดของ 20D2% ที่ลงรายการบัญชีในวันที่ 15 กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="e5bf7-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="e5bf7-137">ยอดเงินสกุลเงินทางบัญชีของใบแจ้งหนี้เป็น 1100 EUR</span><span class="sxs-lookup"><span data-stu-id="e5bf7-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="e5bf7-138">การชำระเงินสำหรับ USD 980 ที่มีการชำระด้วยใบแจ้งหนี้ในวันที่ 1 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="e5bf7-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="e5bf7-139">ยอดส่วนลดเงินสดคือ USD 20</span><span class="sxs-lookup"><span data-stu-id="e5bf7-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="e5bf7-140">ยอดเงินในสกุลเงินทางบัญชีของการชำระเงินคือ 784 EUR</span><span class="sxs-lookup"><span data-stu-id="e5bf7-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="e5bf7-141">ยอดเงินในสกุลเงินทางบัญชีของส่วนลดเงินสดจะคำนวณโดยการใช้อัตราแลกเปลี่ยน ณ วันที่ 1 มีนาคม: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="e5bf7-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

| <span data-ttu-id="e5bf7-142">**หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="e5bf7-142">**Note**</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5bf7-143">คำนวณส่วนลดเงินสดสำหรับตัวเลือกการชำระเงินบางส่วนที่ถูกเลือกในหน้าพารามิเตอร์บัญชีลูกหนี้หรือพารามิเตอร์บัญชีเจ้าหนี้ อัตราแลกเปลี่ยนที่มีผลบังคับในวันที่ของ แต่ละการชำระเงินบางส่วนจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="e5bf7-143">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> |

 
=

 




