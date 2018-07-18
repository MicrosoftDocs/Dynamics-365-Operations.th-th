---
title: "โฮมเพจบัญชีลูกหนี้"
description: "ใช้บัญชีลูกหนี้เพื่อติดตามใบแจ้งหนี้ของลูกค้าและการชำระเงินขาเข้า"
author: twheeloc
manager: AnnBe
ms.date: 08/18/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustomerInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 20671
ms.assetid: 1040678e-ffcb-47fb-a1bc-626db8046504
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b8f2f3a33dc19c2ebc941d1a504eae0c276f3cdf
ms.openlocfilehash: 9fcf106b03cd1abdd135681ceefbb7877f07c773
ms.contentlocale: th-th
ms.lasthandoff: 06/25/2018

---

# <a name="accounts-receivable-home-page"></a><span data-ttu-id="20773-103">โฮมเพจบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="20773-103">Accounts receivable home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20773-104">ใช้บัญชีลูกหนี้เพื่อติดตามใบแจ้งหนี้ของลูกค้าและการชำระเงินขาเข้า</span><span class="sxs-lookup"><span data-stu-id="20773-104">Use Accounts receivable to track customer invoices and incoming payments.</span></span> 

<span data-ttu-id="20773-105">คุณสามารถสร้างใบแจ้งหนี้ของลูกค้าที่ขึ้นอยู่กับใบสั่งขายหรือบันทึกการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="20773-105">You can create customer invoices that are based on sales orders or packing slips.</span></span> <span data-ttu-id="20773-106">คุณยังสามารถป้อนใบแจ้งหนี้ข้อความอิสระที่ไม่เกี่ยวข้องกับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="20773-106">You can also enter free text invoices that are not related to sales orders.</span></span> <span data-ttu-id="20773-107">คุณสามารถรับการชำระเงินโดยใช้การชำระเงินที่แตกต่างกันหลายชนิด</span><span class="sxs-lookup"><span data-stu-id="20773-107">You can receive payments by using several different payment types.</span></span> <span data-ttu-id="20773-108">ซึ่งรวมถึงตั๋วแลกเงิน เงินสด เช็ค บัตรเครดิต และการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="20773-108">These include bills of exchange, cash, checks, credit cards, and electronic payments.</span></span> <span data-ttu-id="20773-109">ถ้าองค์กรของคุณรวมนิติบุคคลหลายราย คุณสามารถใช้การชำระเงินส่วนกลางเพื่อบันทึกการชำระเงินในนิติบุคคลเดี่ยวในนามของนิติบุคคลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="20773-109">If your organization includes multiple legal entities, you can use centralized payments to record payments in a single legal entity on behalf of the other legal entities.</span></span>


<span data-ttu-id="20773-110">**กระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="20773-110">**Business processes**</span></span>

<span data-ttu-id="20773-111">[![กระบวนการทางธุรกิจ](./media/AR-process.PNG)](./media/AR-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="20773-111">[![Business process](./media/AR-process.PNG)](./media/AR-process.PNG)</span></span>

## <a name="set-up-accounts-receivable"></a><span data-ttu-id="20773-112">ตั้งค่าบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="20773-112">Set up Accounts receivable</span></span>

<span data-ttu-id="20773-113">ใช้บัญชีลูกหนี้เพื่อติดตามใบแจ้งหนี้ของลูกค้าและการชำระเงินที่คุณได้รับจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="20773-113">Use Accounts receivable to track customer invoices and payments that you receive from customers.</span></span> <span data-ttu-id="20773-114">คุณสามารถตั้งค่ากลุ่มลูกค้า ลูกค้า โพรไฟล์การลงบัญชี ตัวเลือกการชำระเงินต่างๆ ดอกเบี้ยตั๋วเงิน จดหมายเรียกเก็บเงิน ค่าส่งเสริมการขายให้แก่ผู้ขาย และพารามิเตอร์ที่เกี่ยวข้องกับลูกค้า ค่าธรรมเนียม การจัดส่งและปลายทาง ตั๋วแลกเงิน และข้อมูลบัญชีลูกหนี้ชนิดอื่น</span><span class="sxs-lookup"><span data-stu-id="20773-114">You can set up customer groups, customers, posting profiles, interest notes, collection letters, commissions, and parameters regarding customers, charges, deliveries and destinations, bills of exchange, and other types of Accounts receivable information.</span></span> 

<span data-ttu-id="20773-115">:::แถว::: :::คอลัมน์::: - [การกระจายการลงบัญชีและรายการสมุดรายวันของบัญชีแยกประเภทย่อยสำหรับใบแจ้งหนี้ข้อความอิสระ](accounting-distributions-subledger-journal-entries-free-text-invoices.md)
        - [โพรไฟล์การลงรายการบัญชีลูกค้า](customer-posting-profiles.md)
        - [การตั้งค่าบัตรเครดิต ตรวจสอบ และรวบรวมข้อมูล](credit-card-authorizations.md)
        - [สร้างใบแจ้งหนี้ของลูกค้า](configure-customer-invoices.md)
        - [ตั้งค่า และประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ](set-up-process-recurring-invoices.md)
        - [แก้ไขใบแจ้งหนี้ข้อความอิสระ](correct-free-text-invoice.md) :::สิ้นสุดคอลัมน์::: :::คอลัมน์::: - [ตั้งค่าตั๋วแลกเงิน](set-up-bills-exchange.md)
        - [การตั้งค่าอัตราดอกเบี้ยสำหรับรหัสดอกเบี้ย](set-up-interest-rates-interest-code.md)
        - [ยกเว้น กลับมาคิด หรือย้อนกลับรายการค่าธรรมเนียมดอกเบี้ย](waive-reinstate-reverse-interest-fees.md)
        - [ภาพรวมการหักบัญชีเงินฝากอัตโนมัติ SEPA](sepa-direct-debit-overview.md)
        - [ตั้งค่าข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ SEPA](sepa-direct-debit-mandate.md)
        - [ปิดบัญชีลูกหนี้](close-accounts-receivable.md) :::สิ้นสุดคอลัมน์::: :::สิ้นสุดแถว:::</span><span class="sxs-lookup"><span data-stu-id="20773-115">:::row::: :::column::: - [Accounting distributions and subledger journal entries for free text invoices](accounting-distributions-subledger-journal-entries-free-text-invoices.md)
        - [Customer posting profiles](customer-posting-profiles.md)
        - [Credit card setup, authorization, and capture](credit-card-authorizations.md)
        - [Create a customer invoice](configure-customer-invoices.md)
        - [Set up and process recurring invoices](set-up-process-recurring-invoices.md)
        - [Correct a free text invoice](correct-free-text-invoice.md) :::column-end::: :::column::: - [Set up bills of exchange](set-up-bills-exchange.md)
        - [Set up interest rates for an interest code](set-up-interest-rates-interest-code.md)
        - [Waive, reinstate, or reverse interest fees](waive-reinstate-reverse-interest-fees.md)
        - [SEPA direct debit overview](sepa-direct-debit-overview.md)
        - [Set up SEPA direct debit mandate](sepa-direct-debit-mandate.md)
        - [Close Accounts receivable](close-accounts-receivable.md) :::column-end::: :::row-end:::</span></span>


## <a name="set-up-credit-and-collections"></a><span data-ttu-id="20773-116">การตั้งค่าสินเชื่อและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="20773-116">Set up credit and collections</span></span>

<span data-ttu-id="20773-117">ข้อมูลการเรียกเก็บเงินบัญชีลูกหนี้ถูกจัดการในมุมมองส่วนกลางหนึ่งมุมมอง ในหน้าการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="20773-117">Accounts receivable collections information is managed in one central view, the Collections page.</span></span> <span data-ttu-id="20773-118">ผู้จัดการฝ่ายสินเชื่อและการเรียกเก็บเงินสามารถใช้มุมมองส่วนกลางนี้ เพื่อจัดการการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="20773-118">Credit and collections managers can use this central view to manage collections.</span></span> <span data-ttu-id="20773-119">ตัวแทนเรียกเก็บเงินจะเริ่มกระบวนการเรียกเก็บเงินจากรายชื่อลูกค้า ที่ถูกสร้างขึ้นโดยการใช้เกณฑ์การเรียกเก็บเงินที่กำหนดไว้ล่วงหน้า หรือจากหน้าลูกค้า</span><span class="sxs-lookup"><span data-stu-id="20773-119">Collections agents can begin the collections process from customer lists that are generated by using predefined collection criteria, or from the Customers page.</span></span>

[<span data-ttu-id="20773-120">สินเชื่อและการเรียกเก็บเงินในบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="20773-120">Credit and collections in Accounts receivable</span></span>](collections-credit-accounts-receivable.md)

[<span data-ttu-id="20773-121">ตั้งค่าคอนฟิกบัญชีลูกหนี้และสินเชื่อและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="20773-121">Configure Accounts receivables and Credit and collections</span></span>](accounts-receivables-set-up-overview.md)

[<span data-ttu-id="20773-122">การตั้งค่าสินเชื่อและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="20773-122">Set up Credit and collections</span></span>](set-up-collections.md)

## <a name="set-up-payments-and-settlements"></a><span data-ttu-id="20773-123">ตั้งค่าการชำระเงินและการตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="20773-123">Set up payments and settlements</span></span>

<span data-ttu-id="20773-124">ยอมรับการชำระเงินจากลูกค้า เช่นตั๋วแลกเงิน เงินสด เช็ค บัตรเครดิต และการชำระเงินทางอิเล็กทรอนิกส์ชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="20773-124">Accept different types of payments from customers, such as bills of exchange, cash, checks, credit cards, and electronic payments.</span></span> 

<span data-ttu-id="20773-125">:::แถว::: :::คอลัมน์::: - [ใช้การชำระเงินของลูกค้าเพื่อชำระใบแจ้งหนี้หลายใบที่ครอบคลุมรอบระยะเวลาส่วนลดหลายรายการ](customer-payment-settle-multiple-invoices-multiple-discount-periods.md)
        - [การชำระเงินส่วนกลางสำหรับบัญชีลูกหนี้](centralized-payments-accounts-receivable.md)
        - [ชำระเงินบางส่วนของลูกค้า และการชำระเงินครั้งสุดท้ายเต็มจำนวนก่อนวันที่ให้ส่วนลด](../accounts-payable/settle-partial-customer-payment-or-final-payment-before-discount.md)
        - [การชำระเงินบางส่วนของผู้ซิ้อก่อนวันที่ให้ส่วนลดกับการชำระเงินครั้งสุดท้ายหลังจากวันที่ให้ส่วนลด](settle-partial-customer-payment-before-discount-or-final-payment-after.md) :::สิ้นสุดคอลัมน์::: :::คอลัมน์::: - [การชำระเงินบางส่วนของผู้ซิ้อที่มีส่วนลดในใบลดหนี้](settle-partial-customer-payment-discounts-credit-notes.md)
        - [ชำระการชำระเงินของลูกค้าบางส่วนที่มีรอบระยะเวลาส่วนลดหลายรอบ](settle-partial-customer-payment-multiple-discount-periods.md)
        - [ชำระเงินคืนลูกค้า](reimburse-customers.md)
        - [การชำระเงินของลูกค้าสำหรับยอดเงินบางส่วน](customer-payments-partial-amount.md) :::สิ้นสุดคอลัมน์::: :::สิ้นสุดแถว:::</span><span class="sxs-lookup"><span data-stu-id="20773-125">:::row::: :::column::: - [Use a customer payment to settle multiple invoices that span multiple discount periods](customer-payment-settle-multiple-invoices-multiple-discount-periods.md)
        - [Centralized payments for Accounts receivable](centralized-payments-accounts-receivable.md)
        - [Settle a partial customer payment and the final payment in full before the discount date](../accounts-payable/settle-partial-customer-payment-or-final-payment-before-discount.md)
        - [Settle a partial customer payment before the discount date with a final payment after the discount date](settle-partial-customer-payment-before-discount-or-final-payment-after.md) :::column-end::: :::column::: - [Settle a partial customer payment that has discounts on credit notes](settle-partial-customer-payment-discounts-credit-notes.md)
        - [Settle a partial customer payment that has multiple discount periods](settle-partial-customer-payment-multiple-discount-periods.md)
        - [Reimburse customers](reimburse-customers.md)
        - [Customer payments for a partial amount](customer-payments-partial-amount.md) :::column-end::: :::row-end:::</span></span>


### <a name="additional-resources"></a><span data-ttu-id="20773-126">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="20773-126">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="20773-127">มีอะไรใหม่และอะไรที่กำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="20773-127">What's new and in development</span></span>

<span data-ttu-id="20773-128">ไปที่ [แผนการทำงาน Microsoft Dynamics 365](https://roadmap.dynamics.com/) เพื่อดูว่ามีการนำคุณลักษณะใหม่ใดออกใช้ และมีคุณลักษณะใหม่ใดบ้างที่กำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="20773-128">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="20773-129">บล็อก</span><span class="sxs-lookup"><span data-stu-id="20773-129">Blogs</span></span>

<span data-ttu-id="20773-130">คุณสามารถค้นหาความคิดเห็น ข่าวสาร และข้อมูลอื่นๆ เกี่ยวกับบัญชีลูกหนี้และการแก้ไขปัญหาอื่นๆ ได้ใน [บล็อก Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise)</span><span class="sxs-lookup"><span data-stu-id="20773-130">You can find opinions, news, and other information about Accounts receivable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="20773-131">มีโพสต์ต่างๆ เกี่ยวกับบัญชีลูกหนี้ใน [บล็อกทีมงานผลิตภัณฑ์ Microsoft Dynamics AX](https://blogs.msdn.microsoft.com/dax/)</span><span class="sxs-lookup"><span data-stu-id="20773-131">There are many posts about Accounts receivable on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="20773-132">แม้ว่าโพสต์เหล่านี้ถูกเขียนขึ้นสำหรับบัญชีลูกหนี้ในรุ่นก่อนหน้านี้ แต่ยังคงใช้แนวคิดเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="20773-132">Although some of these posts were written for the previous version of Accounts receivable, the same concepts still apply.</span></span> <span data-ttu-id="20773-133">และขั้นตอนจะเหมือนกันในรุ่นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="20773-133">and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="20773-134">[บล็อกชุมชนคู่ค้า Microsoft Dynamics Operations](https://community.dynamics.com/partner/b/operationspartnercommunityblog) มอบทรัพยากรเดียวให้กับคู่ค้า Microsoft Dynamics สำหรับเรียนรู้สิ่งใหม่และแนวโน้มต่างๆ ใน MBS Operations</span><span class="sxs-lookup"><span data-stu-id="20773-134">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="task-guides"></a><span data-ttu-id="20773-135">คู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="20773-135">Task guides</span></span>
<span data-ttu-id="20773-136">วิธีใช้เพิ่มเติมพร้อมใช้เป็นคู่มืองานภายใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20773-136">Additional help is available as task guides inside Finance and Operations.</span></span> <span data-ttu-id="20773-137">ในการเข้าถึงคู่มืองาน ให้คลิกปุ่มวิธีใช้บนหน้าใดๆ</span><span class="sxs-lookup"><span data-stu-id="20773-137">To access task guides, click the Help button on any page.</span></span>

#### <a name="videos"></a><span data-ttu-id="20773-138">วิดีโอ</span><span class="sxs-lookup"><span data-stu-id="20773-138">Videos</span></span>

<span data-ttu-id="20773-139">ดูวิดีโอวิธีการที่ตอนนี้มีอยู่บน [ช่อง YouTube ของ Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)</span><span class="sxs-lookup"><span data-stu-id="20773-139">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>








