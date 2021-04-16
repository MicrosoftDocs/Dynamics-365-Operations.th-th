---
title: ตั้งค่าคอนฟิกภาษีขายสำหรับใบสั่งออนไลน์
description: หัวข้อนี้แสดงภาพรวมของการเลือกกลุ่มภาษีขายสำหรับชนิดใบสั่งออนไลน์ Dynamics 365 Commerce ต่าง ๆ ใน
author: gvrmohanreddy
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 68b7e59a1e1ea18bdcd4e7a9117e4892407f40ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791858"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="dfff5-103">ตั้งค่าคอนฟิกภาษีขายสำหรับใบสั่งออนไลน์</span><span class="sxs-lookup"><span data-stu-id="dfff5-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dfff5-104">หัวข้อนี้แสดงภาพรวมของการเลือกกลุ่มภาษีขายสำหรับชนิดใบสั่งออนไลน์ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="dfff5-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="dfff5-105">ช่องทางอิเล็กทรอนิกส์ของคุณอาจต้องการสนับสนุนตัวเลือก เช่น การจัดส่งหรือการเบิกสินค้าสำหรับใบสั่งซื้อออนไลน์</span><span class="sxs-lookup"><span data-stu-id="dfff5-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="dfff5-106">ความเกี่ยวข้องของภาษีขายจะขึ้นอยู่กับตัวเลือกที่ผู้ใช้ออนไลน์เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="dfff5-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="dfff5-107">เมื่อลูกค้าเลือกที่จะซื้อสินค้าออนไลน์และได้รับการจัดส่งไปยังที่อยู่ จะมีการกำหนดภาษีขายตามการตั้งค่ากลุ่มภาษีที่อยู่ในการจัดส่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="dfff5-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="dfff5-108">เมื่อลูกค้าต้องการรับสินค้าที่ซื้อที่ร้านค้า จะมีการกำหนดภาษีขายตามการตั้งค่ากลุ่มภาษีของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="dfff5-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="dfff5-109">จัดส่งคำสั่งซื้อไปยังที่อยู่ลูกค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="dfff5-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="dfff5-110">โดยทั่วไป ภาษีสำหรับใบสั่งซื้อออนไลน์ที่ที่อยู่ของลูกค้าจะถูกกำหนดโดยปลายทาง</span><span class="sxs-lookup"><span data-stu-id="dfff5-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="dfff5-111">กลุ่มภาษีขายแต่ละกลุ่มจะมีการตั้งค่าคอนฟิกการจัดทำภาษีตามปลายทางการขายปลีก ซึ่งธุรกิจของคุณสามารถกำหนดรายละเอียดปลายทาง เช่น เขต/ภูมิภาค รัฐ เขต และเมืองในฟอร์มลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="dfff5-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="dfff5-112">เมื่อมีการวางใบสั่งออนไลน์ ระบบภาษี Commerce จะใช้ที่อยู่ที่จัดส่งของสินค้าในบรรทัดทั้งหมดในใบสั่ง และค้นหากลุ่มภาษีขายที่มีเกณฑ์ภาษีตามปลายทางที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="dfff5-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="dfff5-113">ตัวอย่างเช่น สำหรับใบสั่งออนไลน์ที่มีที่อยู่ที่จัดส่งสินค้าในบรรทัดไปยังซานฟรานซิสโก รัฐแคลิฟอร์เนีย กลไกจัดการภาษีจะค้นหากลุ่มภาษีขายและรหัสภาษีขายสำหรับรัฐแคลิฟอร์เนียแล้วคำนวณภาษีสำหรับสินค้าแต่ละรายการตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="dfff5-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="dfff5-114">กลุ่มภาษีตามลูกค้า</span><span class="sxs-lookup"><span data-stu-id="dfff5-114">Customer-based tax groups</span></span>

<span data-ttu-id="dfff5-115">ในศูนย์ควบคุม Commerce มีสองสถานที่ที่มีการตั้งค่าคอนฟิกกลุ่มภาษีของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="dfff5-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="dfff5-116">**โพรไฟล์ของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="dfff5-116">**Customer's profile**</span></span>
- <span data-ttu-id="dfff5-117">**ที่อยู่จัดส่งของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="dfff5-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="dfff5-118">ถ้าโพรไฟล์ของลูกค้ามีกลุ่มภาษีที่มีการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="dfff5-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="dfff5-119">เรกคอร์ดของโพรไฟล์ของลูกค้าใน Retail Headquarters อาจมีการตั้งค่าคอนฟิกกลุ่มภาษีขายไว้อย่างไรก็ตามสำหรับใบสั่งซื้อที่มีการตั้งค่าคอนฟิกกลุ่มภาษีขายในโพรไฟล์ของลูกค้าจะไม่ถูกใช้โดยกลไกจัดการภาษี</span><span class="sxs-lookup"><span data-stu-id="dfff5-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="dfff5-120">ถ้าที่อยู่จัดส่งของลูกค้ามีกลุ่มภาษีที่มีการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="dfff5-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="dfff5-121">ถ้าเรกคอร์ดที่อยู่ที่จัดส่งของลูกค้ามีกลุ่มภาษีถูกตั้งค่าคอนฟิกและมีการจัดส่งสินค้าตามใบสั่งซื้อทางออนไลน์ (หรือสินค้าในรายการ) ให้กับที่อยู่ที่จัดส่งของลูกค้า กลุ่มภาษีที่ตั้งค่าคอนฟิกไว้ในเรกคอร์ดที่อยู่ของลูกค้าจะถูกใช้โดยกลไกจัดการภาษีสำหรับการคำนวณภาษี</span><span class="sxs-lookup"><span data-stu-id="dfff5-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="dfff5-122">ตั้งค่าคอนฟิกกลุ่มภาษีสำหรับเรกคอร์ดที่อยู่จัดส่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="dfff5-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="dfff5-123">เมื่อต้องการตั้งค่าคอนฟิกกลุ่มภาษีสำหรับเรกคอร์ดที่อยู่ที่จัดส่งของลูกค้าในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dfff5-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="dfff5-124">ไปที่ **ลูกค้าทั้งหมด** แล้วเลือกลูกค้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="dfff5-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="dfff5-125">บนแท็บด่วน **ที่อยู่** ให้เลือกที่อยู่ที่ต้องการ แล้วเลือก **ตัวเลือกเพิ่มเติม \> ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="dfff5-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="dfff5-126">ภายใต้แท็บ **ทั่วไป** บนหน้า **จัดการที่อยู่** ให้กำหนดมูลค่าภาษีขายตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="dfff5-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="dfff5-127">มีการกำหนดกลุ่มภาษีโดยใช้ที่อยู่ที่จัดส่งของบรรทัดใบสั่งและภาษีตามปลายทางจะได้รับการตั้งค่าคอนฟิกที่กลุ่มภาษีเอง</span><span class="sxs-lookup"><span data-stu-id="dfff5-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="dfff5-128">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าภาษีสำหรับร้านค้าออนไลน์ตามปลายทาง](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)</span><span class="sxs-lookup"><span data-stu-id="dfff5-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="dfff5-129">การเบิกสินค้าตามใบสั่งในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="dfff5-129">Order pickup in store</span></span>

<span data-ttu-id="dfff5-130">สำหรับรายการใบสั่งที่มีการเบิกสินค้าในร้านค้าหรือเท้าที่ระบุ กลุ่มภาษีจากร้านค้าเบิกสินค้าที่เลือกจะถูกนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="dfff5-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="dfff5-131">สำหรับรายละเอียดเกี่ยวกับวิธีการตั้งค่าคอนฟิกกลุ่มภาษีสำหรับร้านค้าที่กำหนด ให้ดูที่ [ตั้งค่าตัวเลือกภาษีอื่นๆสำหรับร้านค้า](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)</span><span class="sxs-lookup"><span data-stu-id="dfff5-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="dfff5-132">เมื่อมีการเบิกสินค้าตามบรรทัดใบสั่งที่ร้านค้า การตั้งค่าภาษีที่อยู่ของลูกค้า (ถ้าตั้งค่า) จะถูกละเว้นโดยกลไกจัดการภาษี และการตั้งค่าคอนฟิกภาษีของร้านค้าเบิกสินค้าจะถูกนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="dfff5-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="dfff5-133">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dfff5-133">Additional resources</span></span>

[<span data-ttu-id="dfff5-134">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="dfff5-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="dfff5-135">วิธีการคำนวณภาษีขายในฟิลด์จุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dfff5-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="dfff5-136">การกำหนดและการแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="dfff5-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="dfff5-137">ยอดเงินทั้งหมดและตัวเลือกการคำนวณช่วงเวลาสำหรับรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="dfff5-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="dfff5-138">การคำนวณการยกเว้นภาษี</span><span class="sxs-lookup"><span data-stu-id="dfff5-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]