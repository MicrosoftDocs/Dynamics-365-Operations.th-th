---
title: การแก้ปัญหาราคา ส่วนลด ข้อตกลง และเงินคืน
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบในระหว่างที่คุณทำงานกับราคา ส่วนลด ข้อตกลง และเงินคืน
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 5d17f2ec594901404fcd251e463f293258af051c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237166"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="b3ff5-103">การแก้ปัญหาราคา ส่วนลด ข้อตกลง และเงินคืน</span><span class="sxs-lookup"><span data-stu-id="b3ff5-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="b3ff5-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบในระหว่างที่คุณทำงานกับราคา ส่วนลด ข้อตกลง และเงินคืน</span><span class="sxs-lookup"><span data-stu-id="b3ff5-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="b3ff5-105">ฉันไม่สามารถเชื่อมโยงข้อตกลงการซื้อกับบรรทัดใบสั่งซื้อได้หลังจากที่สร้างใบสั่งซื้อแล้ว</span><span class="sxs-lookup"><span data-stu-id="b3ff5-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="b3ff5-106">ข้อตกลงการซื้อไม่สามารถเชื่อมโยงกับบรรทัดใบสั่งซื้อได้เมื่อสร้างใบสั่งซื้อแล้ว</span><span class="sxs-lookup"><span data-stu-id="b3ff5-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="b3ff5-107">มิฉะนั้นบรรทัดใบสั่งซื้อจะไม่สามารถเชื่อมโยงกับบรรทัดข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="b3ff5-108">การตรวจสอบอะไรที่ทริกเกอร์ข้อความ "อัปเดตราคาและส่วนลดที่ป้อนด้วยตนเองหรือเอกสารภายนอก"</span><span class="sxs-lookup"><span data-stu-id="b3ff5-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="b3ff5-109">เมื่อคุณเปลี่ยนวันที่จัดส่ง คุณอาจได้รับข้อความแจ้งว่า "อัปเดตราคาและส่วนลดที่ป้อนด้วยตนเองหรือเอกสารภายนอก"</span><span class="sxs-lookup"><span data-stu-id="b3ff5-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="b3ff5-110">คุณได้รับข้อความนี้เนื่องจากมีการเปลี่ยนแปลงวันที่จัดส่ง อาจมีการทริกเกอร์การค้าหรือข้อตกลงการขายที่แตกต่างกันและทำให้เกิดการเปลี่ยนแปลงราคา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="b3ff5-111">การเปลี่ยนแปลงวันที่จัดส่งอาจส่งผลกระทบต่อกำหนดการของคลังสินค้าและข้อมูลอื่นๆ ที่เกี่ยวข้องด้วย</span><span class="sxs-lookup"><span data-stu-id="b3ff5-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="b3ff5-112">ข้อความจะถูกทริกเกอร์เมื่อใดก็ตามที่มีการเปลี่ยนแปลงใดๆ ของวันที่หรือพารามิเตอร์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="b3ff5-113">วัตถุประสงค์ของข้อความคือเพื่อให้แน่ใจว่าคุณทราบถึงการเปลี่ยนแปลงราคาที่อาจเกิดขึ้นเนื่องจากการเปลี่ยนแปลงเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="b3ff5-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="b3ff5-114">ข้อความคือพร้อมต์การประเมินข้อตกลงทางการค้า (TAE)</span><span class="sxs-lookup"><span data-stu-id="b3ff5-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="b3ff5-115">สำหรับคำอธิบายเต็ม โปรดดู [นโยบายการประเมินข้อตกลงทางการค้า](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper)</span><span class="sxs-lookup"><span data-stu-id="b3ff5-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="b3ff5-116">ใบรับสินค้าตามใบสั่งซื้อไม่รวมค่าธรรมเนียมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b3ff5-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="b3ff5-117">สร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="b3ff5-117">Reproduce the issue</span></span>

<span data-ttu-id="b3ff5-118">กระบวนการต่อไปนี้แสดงวิธีหนึ่งที่จะสร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="b3ff5-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="b3ff5-119">บนหน้า **พารามิเตอร์การจัดซื้อและการจัดหา** บนแท็บ **การจัดส่ง** โปรดตรวจสอบให้แน่ใจว่าได้ตั้งค่าตัวเลือก **การสร้างค่าธรรมเนียมบนใบรับสินค้า** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="b3ff5-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="b3ff5-120">สร้างใบสั่งซื้อที่มีค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="b3ff5-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="b3ff5-121">ยืนยันใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="b3ff5-122">รับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="b3ff5-123">ดูยอดรวมการรับสินค้าและเปรียบเทียบกับผลรวมที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="b3ff5-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="b3ff5-124">โปรดสังเกตว่าค่าธรรมเนียมทั้งหมดจะรวมอยู่ในใบรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b3ff5-125">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-125">Issue resolution</span></span>

<span data-ttu-id="b3ff5-126">การแก้ไขขึ้นอยู่กับวิธีการตั้งค่าค่าธรรมเนียมเบ็ดเตล็ด</span><span class="sxs-lookup"><span data-stu-id="b3ff5-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="b3ff5-127">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าค่าธรรมเนียมเบ็ดเตล็ดเพื่อให้ตรงกับความต้องการของคุณ โปรดดูที่ประกาศบล็อกต่อไปนี้:  [ลงรายการบัญชีค่าธรรมเนียมเบ็ดเตล็ดในเวลาของใบรับสินค้า](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)</span><span class="sxs-lookup"><span data-stu-id="b3ff5-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="b3ff5-128">ราคาและส่วนลดของข้อตกลงทางการค้าใช้ไม่ได้กับบรรทัดใบสั่งขายหรือใบสั่งซื้อที่นำเข้าโดยใช้การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b3ff5-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b3ff5-129">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-129">Issue description</span></span>

<span data-ttu-id="b3ff5-130">ข้อตกลงทางการค้าที่ใช้ได้กับบรรทัดใบสั่งขายหรือใบสั่งซื้อใช้ไม่ได้กับบรรทัดที่นำเข้าโดยใช้การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b3ff5-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="b3ff5-131">อย่างไรก็ตาม ข้อตกลงทางการค้าเดียวกันจะใช้กับบรรทัดใบสั่งขายหรือใบสั่งซื้อที่สร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b3ff5-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="b3ff5-132">เหตุผลสำหรับปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-132">Reason for the issue</span></span>

<span data-ttu-id="b3ff5-133">ถ้าบรรทัดใบสั่งซื้อที่นำเข้าผ่านทางการจัดการข้อมูลรวมถึงข้อมูลราคาแล้ว ข้อตกลงทางการค้าจะไม่ได้รับการประเมินใหม่สำหรับบรรทัดเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="b3ff5-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="b3ff5-134">ตัวอย่างเช่น ถ้า **เปอร์เซ็นต์ส่วนลดต่อรายการสินค้า** หรือค่าราคาและส่วนลดใดๆ ถูกตั้งค่าไว้สำหรับรายการหนึ่ง ข้อตกลงทางการค้าจะไม่ถูกค้นหาสำหรับรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="b3ff5-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="b3ff5-135">วิธีการแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-135">Issue workaround</span></span>

<span data-ttu-id="b3ff5-136">ลักษณะการทำงานนี้คาดไว้แล้วและคล้ายกันสำหรับทั้งใบสั่งขายและใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="b3ff5-137">การแก้ปัญหาให้นำเข้าบรรทัดใบสั่งซื้อโดยไม่มีการตั้งค่าข้อมูลราคาใดๆ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="b3ff5-138">จะมีการใช้ข้อตกลงทางการค้าและบรรทัดใบสั่งซื้อจะได้รับการอัปเดตโดยยึดตามข้อตกลงทางการค้าที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="b3ff5-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="b3ff5-139">เงินคืนของผู้จัดจำหน่ายไม่ได้รับการสะสมตามใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b3ff5-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b3ff5-140">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-140">Issue description</span></span>

<span data-ttu-id="b3ff5-141">ถ้าใบแจ้งหนี้ที่ลงรายการบัญชีมีวันที่ครบกำหนดแตกต่างกัน ใบแจ้งหนี้เหล่านั้นจะไม่มีผลในเงินคืนของผู้จัดจำหน่ายที่สร้างขึ้นจากใบแจ้งหนี้ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="b3ff5-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b3ff5-142">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-142">Issue resolution</span></span>

<span data-ttu-id="b3ff5-143">ตามการออกแบบ เมื่อมีการคำนวณเงินคืนของผู้จัดจำหน่าย จะไม่คำนึงถึงวันที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="b3ff5-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="b3ff5-144">ให้พิจารณาการเลือกกำหนดระบบด้วยตนเองเพื่อให้วันที่ครบกำหนดและความสัมพันธ์กับใบแจ้งหนี้มีความเกี่ยวข้องกับเงินคืนของผู้จัดจำหน่ายจริงมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="b3ff5-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="b3ff5-145">ราคาต่อหน่วยในใบสั่งซื้อไม่ได้คำนวณตามการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="b3ff5-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b3ff5-146">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-146">Issue description</span></span>

<span data-ttu-id="b3ff5-147">เมื่อมีการเปลี่ยนหน่วยในใบสั่งซื้อ ราคาข้อตกลงทางการค้าจะไม่มีการคำนวณใหม่ตามข้อกำหนดของการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="b3ff5-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b3ff5-148">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-148">Issue resolution</span></span>

<span data-ttu-id="b3ff5-149">ราคาจะได้รับจากข้อตกลงทางการค้าเสมอ (หรือการตั้งค่าราคาอื่นๆ ในระบบ เช่น ข้อตกลงการขาย หรือราคาสินค้า) และตั้งค่าไว้สำหรับหนึ่งหน่วย</span><span class="sxs-lookup"><span data-stu-id="b3ff5-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="b3ff5-150">ถ้ามีการเปลี่ยนหน่วยในบรรทัดใบสั่ง ระบบจะค้นหาราคาสำหรับหน่วยใหม่และใช้ราคาดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="b3ff5-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="b3ff5-151">ถ้าไม่พบราคาสำหรับหน่วยนั้น ระบบจะไม่มีการใช้ราคา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="b3ff5-152">ไม่สามารถใช้การแปลงหน่วยเพื่อคำนวณราคาใหม่เป็นหน่วยอื่นได้</span><span class="sxs-lookup"><span data-stu-id="b3ff5-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="b3ff5-153">ในทางทฤษฎี ราคาสำหรับหนึ่งกล่องในสิบกล่องอาจไม่เท่ากับราคาสิบเท่าของกล่องเดียว</span><span class="sxs-lookup"><span data-stu-id="b3ff5-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="b3ff5-154">วิธีการแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-154">Issue workaround</span></span>

<span data-ttu-id="b3ff5-155">วิธีการหนึ่งในการหลีกเลี่ยงปัญหานี้คือตรวจสอบให้แน่ใจว่ามีข้อตกลงทางการค้าสำหรับหน่วยที่คุณคาดว่าจะใช้ในบรรทัดใบสั่งสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b3ff5-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="b3ff5-156">ปัญหาเกี่ยวกับการแปลงสกุลเงินเกิดขึ้นกับข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="b3ff5-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="b3ff5-157">ราคาข้อตกลงทางการค้าจะไม่มีการคำนวณใหม่อีกครั้งตามสกุลเงิน เมื่อสกุลเงินแตกต่างกันในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="b3ff5-158">ลักษณะการทำงานของ *สกุลเงินทั่วไป* ช่วยให้คุณสามารถกำหนดราคาและส่วนลดในสกุลเงินเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b3ff5-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="b3ff5-159">คุณสามารถแปลงเป็นสกุลเงินอื่นได้ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="b3ff5-160">นอกจากนี้คุณยังสามารถใช้คุณลักษณะการปัดเศษแบบชาญฉลาดได้โดยอัตโนมัติเมื่อมีการแปลงเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="b3ff5-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="b3ff5-161">เมื่อฉันเปิดหน้าข้อตกลงการซื้อในโหมดมุมมองบรรทัด ฉันจะไม่สามารถปรับแต่งหน้าได้โดยการเพิ่มฟิลด์หน่วยราคาในภาพรวมของบรรทัด</span><span class="sxs-lookup"><span data-stu-id="b3ff5-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="b3ff5-162">ฟิลด์บางฟิลด์ที่ใช้ร่วมกันในกรอบงานข้อตกลงไม่สามารถรวมอยู่ในบุคคล</span><span class="sxs-lookup"><span data-stu-id="b3ff5-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="b3ff5-163">ข้อจำกัดนี้เกิดขึ้นเนื่องจากแบบจำลองข้อมูลที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b3ff5-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="b3ff5-164">ดังนั้นคุณจึงไม่สามารถทำให้ฟิลด์ **หน่วยราคา** เป็นแบบส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="b3ff5-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="b3ff5-165">ขีดจำกัดสูงสุดจากข้อตกลงการซื้อไม่มีผลบังคับใช้กับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b3ff5-166">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-166">Issue description</span></span>

<span data-ttu-id="b3ff5-167">เมื่อใบสั่งซื้อเชื่อมโยงกับข้อตกลงการซื้อ ขีดจำกัดสูงสุดจากข้อตกลงการซื้อจะไม่มีผลบังคับในใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="b3ff5-168">มีการป้อนข้อมูลราคาเริ่มต้นไว้อย่างถูกต้อง แต่ไม่เกินขีดจำกัดสูงสุดของข้อตกลงการซื้อในใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b3ff5-169">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3ff5-169">Issue resolution</span></span>

<span data-ttu-id="b3ff5-170">ลักษณะการทำงานนี้คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="b3ff5-170">This behavior is expected.</span></span> <span data-ttu-id="b3ff5-171">เนื่องจากใบขอซื้อไม่ได้รับการอนุมัติเสมอ ปริมาณหรือจำนวนเงินจึงไม่ควรถูกสงวนในข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="b3ff5-172">ดังนั้นคุณจึงไม่สามารถตอบสนองขีดจำกัดสูงสุดจากข้อตกลงการซื้อได้</span><span class="sxs-lookup"><span data-stu-id="b3ff5-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="b3ff5-173">ข้อตกลงทางการค้าสามารถสร้างจาก RFQ ที่ถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="b3ff5-174">ดังนั้นระบบจึงไม่สามารถสร้างสมุดรายวันข้อตกลงทางการค้าที่ถูกสร้างขึ้นได้ถ้ายังไม่ได้ยอมรับรายการ RFQ</span><span class="sxs-lookup"><span data-stu-id="b3ff5-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="b3ff5-175">คุณสามารถสร้างข้อตกลงทางการค้าสำหรับการตอบคำขอใบเสนอราคา (RFQ) ใดๆ ก็ได้ ไม่ว่ามีการยอมรับหรือปฏิเสธคำขอใบเสนอราคาก็ตาม</span><span class="sxs-lookup"><span data-stu-id="b3ff5-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="b3ff5-176">สำหรับข้อมูลเพิ่มเติม ให้ดู [ภาพรวมคำขอใบเสนอราคา (RFQ)](request-quotations.md)</span><span class="sxs-lookup"><span data-stu-id="b3ff5-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]