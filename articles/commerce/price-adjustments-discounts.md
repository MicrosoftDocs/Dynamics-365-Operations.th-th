---
title: การปรับปรุงราคาและส่วนลด
description: บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงราคาและส่วนลดใน Dynamics 365 Commerce
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240953"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="67a61-103">การปรับปรุงราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="67a61-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67a61-104">บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงราคาและส่วนลดใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="67a61-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="67a61-105">ในการค้า คุณสามารถทำการปรับราคาสินค้าและยังสามารถตั้งค่าส่วนลดที่ใช้กับรายการสินค้าหรือการทำธุรกรรมในระบบขายหน้าร้าน (POS) ในใบสั่งขายของศูนย์บริการหรือในใบสั่งซื้อออนไลน์</span><span class="sxs-lookup"><span data-stu-id="67a61-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="67a61-106">ทั้งการปรับปรุงทั้งราคาและส่วนลดสามารถเชื่อมโยงกับกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="67a61-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="67a61-107">สำหรับทั้งการปรับปรุงราคาและส่วนลด คุณสามารถระบุวันที่เริ่มต้นและวันที่สิ้นสุดวันเดียวหรือรอบระยะเวลาที่เกิดซ้ำ รหัสส่วนลด และคุณลักษณะเพิ่มเติมบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="67a61-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="67a61-108">การปรับปรุงราคาและส่วนลดสามารถใช้กับผลิตภัณฑ์ ตัวแปร หรือประเภท</span><span class="sxs-lookup"><span data-stu-id="67a61-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="67a61-109">ถ้าส่วนลดมากกว่าหนึ่งส่วนลดใช้กับผลิตภัณฑ์ ลูกค้าอาจได้รับส่วนลดหรือยอดส่วนลดที่รวม โดยขึ้นอยู่กับการตั้งค่าคอนฟิกของส่วนลด</span><span class="sxs-lookup"><span data-stu-id="67a61-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="67a61-110">การค้าใช้ส่วนลดหรือรวมส่วนลดที่ให้ราคาที่ดีที่สุดแก่ลูกค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="67a61-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="67a61-111">เมื่อคุณตั้งค่าการปรับปรุงราคาหรือส่วนลด ให้แน่ใจที่จะยืนยันว่า กลุ่มราคาถูกกำหนดให้กับช่องทางที่ถูกต้อง แค็ตตาล็อก การสังกัด หรือโปรแกรมตอบแทนลูกค้าสมาชิกที่คุณต้องการส่วนลดไปใช้ต่อ</span><span class="sxs-lookup"><span data-stu-id="67a61-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="67a61-112">นอกจากนี้ หากคุณต้องการสร้างรหัสส่วนลดโดยอัตโนมัติ ให้ตั้งค่าลำดับหมายเลขในหน้า **พารามิเตอร์การค้า** ก่อนที่คุณจะกำหนดการปรับราคาหรือส่วนลดใหม่</span><span class="sxs-lookup"><span data-stu-id="67a61-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="67a61-113">คุณสามารถลบการปรับปรุงราคาหรือส่วนลดได้ </span><span class="sxs-lookup"><span data-stu-id="67a61-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="67a61-114">อย่างไรก็ตาม ข้อมูลทางสถิติจะหายไป</span><span class="sxs-lookup"><span data-stu-id="67a61-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="67a61-115">ชนิดของส่วนลด</span><span class="sxs-lookup"><span data-stu-id="67a61-115">Types of discounts</span></span>

<span data-ttu-id="67a61-116">มีส่วนลดหลายชนิด:</span><span class="sxs-lookup"><span data-stu-id="67a61-116">There are many types of discounts:</span></span>

- <span data-ttu-id="67a61-117">**ส่วนลดแบบง่าย** – เปอร์เซ็นต์หรือยอดเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="67a61-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="67a61-118">**ส่วนลดปริมาณ**– ส่วนลดที่ถูกใช้เมื่อผลิตภัณฑ์สองอย่างขึ้นไปถูกซื้อไป</span><span class="sxs-lookup"><span data-stu-id="67a61-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="67a61-119">**ส่วนลดสำหรับการซื้อคละกัน**– ส่วนลดที่ถูกใช้เมื่อชุดที่ระบุของผลิตภัณฑ์ถูกซื้อไป</span><span class="sxs-lookup"><span data-stu-id="67a61-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="67a61-120">**ส่วนลดจำกัด**– ส่วนลดที่ถูกใช้เมื่อผลรวมของธุรกรรมมากกว่ายอดเงินที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="67a61-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="67a61-121">**ส่วนลดที่ใช้ในการชำระเงิน** – ส่วนลดที่ใช้เมื่อผลรวมของธุรกรรมมากกว่ายอดเงินที่ระบุและชนิดการชำระเงินเฉพาะ (ตัวอย่างเช่น เงินสด เครดิต หรือบัตรเดบิต) จะใช้สำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="67a61-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="67a61-122">**ส่วนลดในการจัดส่ง** – ส่วนลดที่ใช้เมื่อผลรวมของธุรกรรมมากกว่ายอดเงินที่ระบุและวิธีการจัดส่งเฉพาะ (ตัวอย่างเช่น การจัดส่งสินค้าหรือการจัดส่งข้ามคืนสองวัน) ที่ใช้ในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="67a61-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="67a61-123">ทั้งการปรับปรุงทั้งราคาและส่วนลดสามารถเชื่อมโยงกับกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="67a61-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="67a61-124">กลุ่มราคาสามารถเชื่อมโยงกับช่องทาง แค็ตตาล็อก สังกัด และโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="67a61-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="67a61-125">ส่วนลดการซื้อคละกันและส่วนลดเกณฑ์มีคุณสมบัติที่ชื่อ "นับสินค้าที่ไม่สามารถลดราคาได้" และ "นับสินค้าที่ไม่สามารถลดราคาได้ตามเกณฑ์" ตามลําดับ</span><span class="sxs-lookup"><span data-stu-id="67a61-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="67a61-126">หากเปิดใช้งานคุณสมบัติเหล่านี้ สินค้าที่ไม่มีสิทธิ์ส่วนลดใดๆ ยังสามารถกำหนดคุณสมบัติธุรกรรมสำหรับส่วนลดได้ แต่สินค้าที่ไม่มีสิทธิ์จะไม่ได้ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="67a61-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="67a61-127">ตัวอย่างเช่น ถ้าคุณสร้างส่วนลดสําหรับการซื้อคละกันที่มีสองรายการ คือ A และ B ซึ่งลูกค้าควรได้รับส่วนลด 10% สําหรับสินค้าทั้งสองรายการ แต่สินค้า A เลือกการกำหนดค่า "ป้องกันส่วนลดทั้งหมด" ซึ่งโดยปกติแล้ว จะหยุดไม่ให้สินค้า A รวมอยู่ในส่วนลด</span><span class="sxs-lookup"><span data-stu-id="67a61-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="67a61-128">อย่างไรก็ตาม หากเปิดใช้งานคุณสมบัติ "นับผลิตภัณฑ์ที่ไม่สามารถรับส่วนลดได้" ไว้ คุณจะสามารถใช้สินค้า A เพื่อมีสิทธิ์ได้รับส่วนลดสําหรับการซื้อคละกัน แต่ส่วนลด 10% จะใช้กับรายการ B เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="67a61-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="67a61-129">อย่างไรก็ตาม คุณสมบัติ "นับสินค้าที่ไม่สามารถลดราคาได้ตามเกณฑ์" มีความสามารถเพิ่มเติมเมื่อเปรียบเทียบกับคุณสมบัติ "นับผลิตภัณฑ์ที่ไม่สามารถลดราคาได้" ของส่วนลดสําหรับการซื้อคละกัน</span><span class="sxs-lookup"><span data-stu-id="67a61-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="67a61-130">ถ้าส่วนลดขีดจํากัดเปิดใช้งาน และถ้ามีสินค้าที่มีส่วนลดอยู่แล้ว ซึ่งจะป้องกันไม่ให้สินค้ามีส่วนลดอื่นๆ ราคาที่ชําระสําหรับรายการนี้จะมีคุณสมบัติตามเกณฑ์ แต่รายการนี้จะไม่ได้รับส่วนลดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="67a61-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
