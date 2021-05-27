---
title: การชำระเงินล่วงหน้าของลูกค้า
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและดำเนินการชำระเงินล่วงหน้าของลูกค้า (หรือที่เรียกอีกอย่างว่าเงินฝากลูกค้า)
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019431"
---
# <a name="customer-prepayments"></a><span data-ttu-id="62d0e-103">การชำระเงินล่วงหน้าของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62d0e-104">การชำระเงินล่วงหน้าของลูกค้าจะใช้เมื่อคุณได้รับการชำระเงินจากลูกค้า แต่จะไม่มีใบแจ้งหนี้ที่การชำระเงินนั้นสามารถชำระได้</span><span class="sxs-lookup"><span data-stu-id="62d0e-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="62d0e-105">ชนิดการชำระเงินเหล่านี้เรียกอีกอย่างว่า เงินฝากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="62d0e-106">กระบวนการในการตั้งค่าและการทำงานกับการชำระเงินล่วงหน้าของลูกค้าประกอบด้วยขั้นตอนพื้นฐานดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="62d0e-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="62d0e-107">สร้างโปรไฟล์การลงบัญชีของลูกค้าสำหรับการชำระเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="62d0e-108">ตั้งค่าพารามิเตอร์ **โปรไฟล์การลงรายการบัญชีที่มีใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า**</span><span class="sxs-lookup"><span data-stu-id="62d0e-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="62d0e-109">สร้างสมุดรายวันการชำระเงินล่วงหน้าของลูกค้า และเลือกกล่องกาเครื่องหมาย **ใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า** ในแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="62d0e-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="62d0e-110">ลงรายการบัญชีสมุดรายวันการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="62d0e-111">เมื่อสร้างใบแจ้งหนี้แล้ว ให้ชำระการชำระเงินล่วงหน้าโดยใช้หน้า **ชำระธุรกรรมที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="62d0e-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="62d0e-112">สร้างโปรไฟล์การลงบัญชีของลูกค้าสำหรับการชำระเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="62d0e-113">โดยทั่วไป เมื่อคุณยอมรับการชำระเงินล่วงหน้าหรือเงินฝากจากลูกค้าก่อนที่จะจัดส่งสินค้าหรือบริการ หรือก่อนที่จะมีใบแจ้งหนี้อยู่ในระบบของคุณ คุณจะต้องการบันทึกเงินสดเป็นหนี้สินแทนสินทรัพย์ในผังบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="62d0e-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="62d0e-114">อย่างไรก็ตาม ข้อกำหนดของพวกเขาในการบันทึกจํานวนเงินเหล่านี้ในบัญชีแยกประเภททั่วไปของคุณอาจแตกต่างกันไป ขึ้นอยู่กับประเทศหรือภูมิภาคของคุณ</span><span class="sxs-lookup"><span data-stu-id="62d0e-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="62d0e-115">ดังนั้น ควรปรึกษาผู้บัญชีของคุณเกี่ยวกับข้อบังคับท้องถิ่นต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="62d0e-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="62d0e-116">โดยทั่วไป กระบวนการสร้างโปรไฟล์การลงบัญชีที่สามารถใช้สำหรับการชำระเงินล่วงหน้าเหมือนกับกระบวนการสร้างโปรไฟล์การลงบัญชีอื่น</span><span class="sxs-lookup"><span data-stu-id="62d0e-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="62d0e-117">ความแตกต่างหลักคือบัญชีหลักที่คุณเลือกในฟิลด์ **บัญชีสรุป**</span><span class="sxs-lookup"><span data-stu-id="62d0e-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="62d0e-118">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โปรไฟล์การลงรายการบัญชีลูกค้า](customer-posting-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="62d0e-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="62d0e-119">กําหนดพารามิเตอร์การชำระเงินล่วงหน้าของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="62d0e-120">มีพารามิเตอร์บัญชีลูกหนี้หลักสองพารามิเตอร์ที่คุณต้องพิจารณาเมื่อคุณตั้งค่าคอนฟิกระบบการชำระเงินล่วงหน้าของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="62d0e-121">ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าคอนฟิกพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="62d0e-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="62d0e-122">ไปที่ **บัญชีลูกหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="62d0e-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="62d0e-123">ไม่บังคับ: บนแท็บ **บัญชีแยกประเภทและภาษีขาย** บนแท็บด่วน **การชำระเงิน** ให้ตั้งค่าตัวเลือก **ภาษีขายในใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="62d0e-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="62d0e-124">ในฟิลด์ **โปรไฟล์การลงรายการบัญชีที่มีใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า** ให้เลือกโปรไฟล์การลงรายการบัญชีลูกค้าที่จะใช้เมื่อลงรายการบัญชีการชำระเงินล่วงหน้าของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="62d0e-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="62d0e-126">สร้างใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="62d0e-127">เมื่อคุณสร้างสมุดรายวันการชำระเงินล่วงหน้าของลูกค้าสำหรับการชำระเงินล่วงหน้าทุกรายการ คุณต้องตั้งค่าตัวเลือก **ใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า** เป็น **ใช่** บนหน้า **สมุดรายวันการชำระเงินล่วงหน้าของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="62d0e-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="62d0e-128">ทำตามขั้นตอนเหล่านี้เพื่อสร้างการชำระเงินล่วงหน้าของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="62d0e-129">ไปที่ **บัญชีเจ้าหนี้ \> การชำระเงิน \> สมุดรายวันการชำระเงินล่วงหน้าของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="62d0e-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="62d0e-130">เลือก **สร้าง** เพื่อสร้างสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="62d0e-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="62d0e-131">ในฟิลด์ **ชื่อ** ให้เลือกชื่อสมุดรายวันที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="62d0e-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="62d0e-132">ถ้าคุณตั้งค่าตัวเลือก **ภาษีขายในใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า** เป็น **ใช่** ในขั้นตอนก่อนหน้านี้ คุณต้องเลือกชื่อสมุดรายวันที่มีการเลือกพารามิเตอร์ **ยอดเงินรวมภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="62d0e-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="62d0e-133">ไม่จำเป็น: ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบายโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="62d0e-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="62d0e-134">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="62d0e-134">Select **Lines**.</span></span>
6. <span data-ttu-id="62d0e-135">ถ้าไม่มีรายการว่างเปล่าอยู่ ให้เลือก **สร้าง** เพื่อสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="62d0e-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="62d0e-136">ในฟิลด์ **ข้อมูล** ป้อนวันที่ที่การชำระเงินล่วงหน้าควรลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="62d0e-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="62d0e-137">ในฟิลด์ **บัญชี** เลือกลูกค้าสำหรับการชำระเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="62d0e-138">ไม่จำเป็น: ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบายโดยละเอียดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="62d0e-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="62d0e-139">ในฟิลด์ **เครดิต** ป้อนยอดเงินของการชำระเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="62d0e-140">ในฟิลด์ **บัญชีตรงข้าม** ให้เลือกบัญชีที่จะออฟเซ็ตการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="62d0e-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="62d0e-141">ตัวอย่างเช่น เลือกธนาคารหรือบัญชีหลักที่จะลงรายการบัญชีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="62d0e-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="62d0e-142">ในฟิลด์ **วิธีการชำระเงิน** เลือกวิธีการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62d0e-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="62d0e-143">บนแท็บ **การชำระเงิน** ให้ตั้งค่าตัวเลือก **ใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="62d0e-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="62d0e-144">ทําซ้ำขั้นตอนที่ 7 ถึง 13 สําหรับการชำระเงินล่วงหน้าเพิ่มเติมแต่ละรายการที่ต้องลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="62d0e-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="62d0e-145">เลือก **ลงรายการบัญชี** เพื่อจบสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="62d0e-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="62d0e-146">ชำระการชำระเงินล่วงหน้ากับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="62d0e-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="62d0e-147">คุณสามารถใช้พื้นที่ทำงาน **การชำระเงินล่วงหน้าของลูกค้า** เพื่อค้นหาและชำระเงินซึ่งยังไม่ได้มีการชำระอย่างครบถ้วนได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="62d0e-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="62d0e-148">บนแดชบอร์ด **หน้าแรก** ให้เลือกไทล์ **การชำระเงินล่วงหน้าของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="62d0e-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="62d0e-149">ในส่วน **ธุรกรรมของลูกค้า** บนแท็บ **การชำระเงินที่ยังไม่ได้ชำระ** ให้ค้นหาและเลือกการชำระเงินที่จะชำระ</span><span class="sxs-lookup"><span data-stu-id="62d0e-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="62d0e-150">เลือก **ชำระเงินธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="62d0e-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="62d0e-151">เลือกกล่องกาเครื่องหมาย **ทำเครื่องหมาย** ของใบแจ้งหนี้และการชำระเงินที่จะชำระ</span><span class="sxs-lookup"><span data-stu-id="62d0e-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="62d0e-152">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="62d0e-152">Select **Post**.</span></span>

<span data-ttu-id="62d0e-153">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีสรุปการชำระเงินธุรกรรม โปรดดูที่ [ภาพรวมของการชำระเงิน](/cash-bank-management/settlement-overview.md)</span><span class="sxs-lookup"><span data-stu-id="62d0e-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
