---
title: การตั้งค่าบัตรเครดิต ตรวจสอบ และรวบรวมข้อมูล
description: บทความนี้แสดงภาพรวมของการอนุญาตให้ใช้บัตรเครดิตใน Microsoft Dynamics 365 Finance โดยจะมีข้อมูลเกี่ยวกับวิธีการตั้งค่าบริการชำระเงิน เพิ่มบัตรเครดิตให้ใบสั่งขาย และยกเลิกการตรวจสอบ
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0de35934e8bdb160f68f68dab118997d0141bf29
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448276"
---
# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="682ee-104">การตั้งค่าบัตรเครดิต ตรวจสอบ และรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="682ee-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="682ee-105">บทความนี้แสดงภาพรวมของการอนุญาตให้ใช้บัตรเครดิตใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="682ee-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="682ee-106">โดยจะมีข้อมูลเกี่ยวกับวิธีการตั้งค่าบริการชำระเงิน เพิ่มบัตรเครดิตให้ใบสั่งขาย และยกเลิกการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="682ee-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="682ee-107">การตั้งค่าบริการชำระเงินบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="682ee-108">ในการใช้บัตรเครดิต คุณต้องตั้งค่า และเรียกใช้บริการชำระเงินบนหน้าบริการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="682ee-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="682ee-109">บริการชำระเงินทำหน้าที่เป็นสะพานระหว่างนิติบุคคลและธนาคารที่ซึ่งประมวลผลค่าธรรมเนียมบัตรเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="682ee-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="682ee-110">คุณต้องทำงานกับผู้ให้บริการบัตรเครดิตซึ่งจะแสดงรายการอยู่ในฟิลด์ตัวเชื่อมต่อการชำระเงิน และตั้งค่าบัญชีผู้ใช้ที่ผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="682ee-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="682ee-111">คุณต้องตั้งค่าตัวเลือกอื่น ๆ ในหน้าบริการชำระเงิน ตั้งค่าชนิดของบัตรเครดิตสำหรับอเมริกันเอ็กซ์เพรส ดิสคัพเวอร์ มาสเตอร์การ์ด และค้นหาบนหน้าชนิดบัตรเครดิต แล้วเรียกใช้ผู้ให้บริการเป็นค่าผู้ให้บริการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="682ee-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="682ee-112">คุณยังต้องทำตามขั้นตอนเหล่านี้เพื่อทำให้การติดตั้งของคุณเสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="682ee-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="682ee-113">ในหน้าพารามิเตอร์บัญชีลูกหนี้ ระบุพารามิเตอร์สำหรับการใช้การตรวจสอบบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="682ee-114">ในหน้าเงื่อนไขการชำระเงิน ตั้งค่าเงื่อนไขการชำระเงินสำหรับบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="682ee-115">ในฟิลด์ประเภทการชำระเงิน ให้เลือกชนิดของบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="682ee-116">ในหน้าบัตรเครดิตของลูกค้า ให้ป้อนข้อมูลบัตรเครดิตสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="682ee-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="682ee-117">การเพิ่มบัตรเครดิตใหม่</span><span class="sxs-lookup"><span data-stu-id="682ee-117">Adding a new credit card</span></span>
<span data-ttu-id="682ee-118">คุณสามารถสร้างข้อมูลบัตรเครดิตใหม่ในหน้า ลูกค้า โดยเลือก ลูกค้า ตั้งค่า บัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="682ee-119">คุณยังสามารถสร้างบันทึกของข้อมูลบัตรเครดิตเมื่อคุณป้อนใบสั่งขายบนหน้าใบสั่งขาย โดยใช้การจัดการ ลูกค้า บัตรเครดิต ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="682ee-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>

<a name="adding-a-credit-card-to-a-sales-order"></a><span data-ttu-id="682ee-120">การเพิ่มบัตรเครดิตไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="682ee-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="682ee-121">คุณสามารถเพิ่มบัตรเครดิตในใบสั่งขายได้ โดยการเลือกบัตรเครดิตในการค้นหาบัตรเครดิตในแท็บด่วนราคาและส่วนลด บนหน้าใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="682ee-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="682ee-122">การตรวจสอบบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>

<a name="authorizing-a-credit-card"></a><span data-ttu-id="682ee-123">การตรวจสอบบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="682ee-124">เมื่อบัตรเครดิตได้รับอนุมัติการตรวจสอบ หมายเลขบัตรและชื่อของผู้ถือบัตรจะได้รับการตรวจสอบความถูกต้อง และยอดวงเงินที่ใช้ได้ในเครดิตก็จะได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="682ee-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="682ee-125">อีกทางหนึ่งคือ มูลค่าในการตรวจสอบบัตรและที่อยู่ของผู้ถือบัตรจะได้รับการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="682ee-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="682ee-126">ยอดวงเงินที่ใช้ได้ในเครดิตของลูกค้าจะลดลงตามยอดเงินในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="682ee-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="682ee-127">บริการชำระเงินจะทำการส่งข้อมูลว่า บัตรเครดิตนั้นได้รับการอนุมัติ หรือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="682ee-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="682ee-128">เมื่อออกอินวอยซ์ใบสั่งขาย บัตรเครดิตจะถูกคิดค่าธรรมเนียม (รวบรวม) ตามยอดเงินในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="682ee-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="682ee-129">ค่าการตรวจสอบความถูกต้องของบัตร</span><span class="sxs-lookup"><span data-stu-id="682ee-129">Card verification value</span></span>

<span data-ttu-id="682ee-130">คุณสามารถเรียกขอค่าที่ใช้ในการตรวจสอบบัตร ซึ่งบางครั้งเรียกว่ารหัสความปลอดภัยของบัตร</span><span class="sxs-lookup"><span data-stu-id="682ee-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="682ee-131">สำหรับอเมริกันเอ็กซ์เพรส รหัสจะเป็นค่าสี่หลัก</span><span class="sxs-lookup"><span data-stu-id="682ee-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="682ee-132">สำหรับดิสคัฟเวอร์ มาสเตอร์การ์ด และวีซ่า รหัสจะเป็นค่าสามหลัก</span><span class="sxs-lookup"><span data-stu-id="682ee-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="682ee-133">การตรวจสอบความถูกต้องของที่อยู่</span><span class="sxs-lookup"><span data-stu-id="682ee-133">Address verification</span></span>

<span data-ttu-id="682ee-134">จะมีส่งข้อมูลการตรวจสอบให้กับผู้ให้บริการด้านการชำระเงินเสมอ</span><span class="sxs-lookup"><span data-stu-id="682ee-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="682ee-135">คุณสามารถกำหนดได้ว่าจะต้องใช้ข้อมูลมากเท่าไรในการดำเนินธุรกรรมหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="682ee-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="682ee-136">ควรแน่ใจว่าได้ตรวจสอบกับผู้ให้บริการของคุณเพื่อกำหนดว่าจะสามารถยอมรับข้อมูลเหล่านี้ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="682ee-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="682ee-137">ต่อไปนี้เป็นตัวเลือกสำหรับการตรวจสอบที่อยู่:</span><span class="sxs-lookup"><span data-stu-id="682ee-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="682ee-138">**ยอมรับธุรกรรมเสมอ**– ยอมรับธุรกรรม โดยไม่คำนึงถึงผลลัพธ์การตรวจสอบที่อยู่</span><span class="sxs-lookup"><span data-stu-id="682ee-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="682ee-139">**เจ้าของบัญชี**– เปรียบเทียบชื่อของผู้ถือบัตรจากข้อมูลทางธุรกรรมจากบริษัทผู้ให้บริการบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="682ee-140">**ที่อยู่ในการเรียกเก็บเงิน**– เปรียบเทียบชื่อของผู้ถือบัตร และที่อยู่ในการเรียกเก็บเงิน กับข้อมูลทางธุรกรรมจากบริษัทผู้ให้บริการบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="682ee-141">**รหัสไปรษณีย์ในการเรียกเก็บเงิน**– เปรียบเทียบชื่อของผู้ถือบัตร ที่อยู่ และ รหัสไปรษณีย์ในการเรียกเก็บเงิน กับข้อมูลทางธุรกรรมจากบริษัทผู้ให้บริการบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="682ee-142">การสนับสนุนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="682ee-142">Data support</span></span>
<span data-ttu-id="682ee-143">สำหรับบัตรเครดิตแต่ละชนิดที่ได้รับการสนับสนุน คุณสามารถระบุระดับของข้อมูลสนับสนุนได้</span><span class="sxs-lookup"><span data-stu-id="682ee-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="682ee-144">ระดับเหล่านี้เป็นสิ่งที่ควบคุมจำนวนข้อมูลธุรกรรมที่จะถูกโอนย้ายไปยังบริการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="682ee-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="682ee-145">ตรวจสอบกับผู้ให้บริการของคุณให้แน่ใจว่าจะสามารถให้ข้อมูลเหล่านี้ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="682ee-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="682ee-146">ต่อไปนี้เป็นตัวเลือกสำหรับระดับการสนับสนุนข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="682ee-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="682ee-147">**ระดับ 1** – โอนย้ายข้อมูล วันทำธุรกรรม ยอดเงินในธุรกรรม และคำอธิบายของธุรกรรมนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="682ee-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="682ee-148">**ระดับ 2** – โอนย้ายข้อมูลระดับ 1 ทั้งหมด รวมทั้งที่อยู่จัดส่ง ที่อยุ่ผู้ขาย และข้อมูลทางภาษี</span><span class="sxs-lookup"><span data-stu-id="682ee-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="682ee-149">**ระดับ 3** – โอนย้ายข้อมูลระดับ 2 ทั้งหมด รวมทั้งข้อมูลรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="682ee-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="682ee-150">การชำระเงินบางส่วน</span><span class="sxs-lookup"><span data-stu-id="682ee-150">Partial payments</span></span>
<span data-ttu-id="682ee-151">ถ้าคุณจัดส่งสินค้าบางส่วนของใบสั่งแล้ว ยอดเงินของใบสั่งเป็นบางส่วนจะถูกรวบรวมไว้ และกระบวนการตรวจสอบ ซึ่งจะใช้ยอดของใบสั่งทั้งหมดจะถูกปิดลง</span><span class="sxs-lookup"><span data-stu-id="682ee-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="682ee-152">กระบวนการตรวจสอบจะถูกส่งใหม่ตามปริมาณใบสั่งซื้อที่ยังไม่ถูกจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="682ee-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="682ee-153">การยกเลิกกระบวนการตรวจสอบ </span><span class="sxs-lookup"><span data-stu-id="682ee-153">Voiding an authorization</span></span>
<span data-ttu-id="682ee-154">ในการยกเลิกการตรวจสอบบัตรเครดิต คุณสามารถเปลี่ยนวิธีการชำระเงินเป็นวิธีการอื่นที่ไม่มีประเภทการใช้บัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="682ee-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>





