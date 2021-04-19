---
title: การปรับปรุงราคาและส่วนลด
description: บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงราคาและส่วนลดใน Dynamics 365 Commerce
author: scott-tucker
ms.date: 11/16/2020
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
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802802"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="9c835-103">การปรับปรุงราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="9c835-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9c835-104">บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงราคาและส่วนลดใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9c835-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9c835-105">ในการค้า คุณสามารถทำการปรับราคาสินค้าและยังสามารถตั้งค่าส่วนลดที่ใช้กับรายการสินค้าหรือการทำธุรกรรมในระบบขายหน้าร้าน (POS) ในใบสั่งขายของศูนย์บริการหรือในใบสั่งซื้อออนไลน์</span><span class="sxs-lookup"><span data-stu-id="9c835-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="9c835-106">ทั้งการปรับปรุงทั้งราคาและส่วนลดสามารถเชื่อมโยงกับกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="9c835-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="9c835-107">สำหรับทั้งการปรับปรุงราคาและส่วนลด คุณสามารถระบุวันที่เริ่มต้นและวันที่สิ้นสุดวันเดียวหรือรอบระยะเวลาที่เกิดซ้ำ รหัสส่วนลด และคุณลักษณะเพิ่มเติมบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="9c835-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="9c835-108">การปรับปรุงราคาและส่วนลดสามารถใช้กับผลิตภัณฑ์ ตัวแปร หรือประเภท</span><span class="sxs-lookup"><span data-stu-id="9c835-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="9c835-109">ถ้าส่วนลดมากกว่าหนึ่งส่วนลดใช้กับผลิตภัณฑ์ ลูกค้าอาจได้รับส่วนลดหรือยอดส่วนลดที่รวม โดยขึ้นอยู่กับการตั้งค่าคอนฟิกของส่วนลด</span><span class="sxs-lookup"><span data-stu-id="9c835-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="9c835-110">การค้าใช้ส่วนลดหรือรวมส่วนลดที่ให้ราคาที่ดีที่สุดแก่ลูกค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9c835-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="9c835-111">เมื่อคุณตั้งค่าการปรับปรุงราคาหรือส่วนลด ให้แน่ใจที่จะยืนยันว่า กลุ่มราคาถูกกำหนดให้กับช่องทางที่ถูกต้อง แค็ตตาล็อก การสังกัด หรือโปรแกรมตอบแทนลูกค้าสมาชิกที่คุณต้องการส่วนลดไปใช้ต่อ</span><span class="sxs-lookup"><span data-stu-id="9c835-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="9c835-112">นอกจากนี้ หากคุณต้องการสร้างรหัสส่วนลดโดยอัตโนมัติ ให้ตั้งค่าลำดับหมายเลขในหน้า **พารามิเตอร์การค้า** ก่อนที่คุณจะกำหนดการปรับราคาหรือส่วนลดใหม่</span><span class="sxs-lookup"><span data-stu-id="9c835-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="9c835-113">คุณสามารถลบการปรับปรุงราคาหรือส่วนลดได้ </span><span class="sxs-lookup"><span data-stu-id="9c835-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="9c835-114">อย่างไรก็ตาม ข้อมูลทางสถิติจะหายไป</span><span class="sxs-lookup"><span data-stu-id="9c835-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="9c835-115">ชนิดของส่วนลด</span><span class="sxs-lookup"><span data-stu-id="9c835-115">Types of discounts</span></span>

<span data-ttu-id="9c835-116">มีส่วนลดหลายชนิด:</span><span class="sxs-lookup"><span data-stu-id="9c835-116">There are many types of discounts:</span></span>

- <span data-ttu-id="9c835-117">**ส่วนลดแบบง่าย** – เปอร์เซ็นต์หรือยอดเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="9c835-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="9c835-118">**ส่วนลดปริมาณ**– ส่วนลดที่ถูกใช้เมื่อผลิตภัณฑ์สองอย่างขึ้นไปถูกซื้อไป</span><span class="sxs-lookup"><span data-stu-id="9c835-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="9c835-119">**ส่วนลดสำหรับการซื้อคละกัน**– ส่วนลดที่ถูกใช้เมื่อชุดที่ระบุของผลิตภัณฑ์ถูกซื้อไป</span><span class="sxs-lookup"><span data-stu-id="9c835-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="9c835-120">**ส่วนลดจำกัด**– ส่วนลดที่ถูกใช้เมื่อผลรวมของธุรกรรมมากกว่ายอดเงินที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="9c835-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="9c835-121">**ส่วนลดที่ใช้ในการชำระเงิน** – ส่วนลดที่ใช้เมื่อผลรวมของธุรกรรมมากกว่ายอดเงินที่ระบุและชนิดการชำระเงินเฉพาะ (ตัวอย่างเช่น เงินสด เครดิต หรือบัตรเดบิต) จะใช้สำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9c835-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="9c835-122">**ส่วนลดในการจัดส่ง** – ส่วนลดที่ใช้เมื่อผลรวมของธุรกรรมมากกว่ายอดเงินที่ระบุและวิธีการจัดส่งเฉพาะ (ตัวอย่างเช่น การจัดส่งสินค้าหรือการจัดส่งข้ามคืนสองวัน) ที่ใช้ในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="9c835-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="9c835-123">ทั้งการปรับปรุงทั้งราคาและส่วนลดสามารถเชื่อมโยงกับกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="9c835-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="9c835-124">กลุ่มราคาสามารถเชื่อมโยงกับช่องทาง แค็ตตาล็อก สังกัด และโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="9c835-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]