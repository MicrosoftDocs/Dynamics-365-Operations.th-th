---
title: การคํานวณภาษีในใบสั่งออนไลน์ไม่ถูกต้อง
description: หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการคํานวณภาษีในใบสั่งออนไลน์ที่ไม่ถูกต้อง หรือเมื่อตั้งค่ากลุ่มภาษีบนรายการขายไม่ถูกต้อง
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801422"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="96002-103">การคํานวณภาษีในใบสั่งออนไลน์ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96002-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96002-104">หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการคํานวณภาษีในใบสั่งออนไลน์ที่ไม่ถูกต้อง หรือเมื่อตั้งค่ากลุ่มภาษีบนรายการขายไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96002-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="96002-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="96002-105">Description</span></span>

<span data-ttu-id="96002-106">เมื่อวางใบสั่งอีคอมเมิร์ซ ภาษีจะคํานวณไม่ถูกต้อง หรือกลุ่มภาษีบนรายการขายจะตั้งค่าไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96002-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="96002-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="96002-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="96002-108">ตั้งค่าคอนฟิกภาษีขายจากร้านค้าปลีกในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="96002-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="96002-109">ในการตั้งค่าคอนฟิกภาษีขายจากร้านค้าปลีกในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="96002-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="96002-110">ไปยัง **Retail และ Commerce \> ช่องทาง \> ร้านค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="96002-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="96002-111">เลือกร้านค้าที่จะตั้งค่าคอนฟิกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="96002-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="96002-112">บนแท็บด่วน **ทั่วไป** ในส่วน **ภาษีขาย** ให้ตั้งค่าคอนฟิกข้อมูลภาษีขายของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="96002-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="96002-113">สำหรับการเบิกสินค้าจากร้านค้า กลุ่มภาษีจะมาจากร้านค้าที่เลือกเพื่อเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="96002-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="96002-114">ดูข้อมูลเพิ่มเติมที่ [ตั้งค่าตัวเลือกภาษีอื่นๆ สำหรับร้านค้า](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)</span><span class="sxs-lookup"><span data-stu-id="96002-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="96002-115">ตั้งค่าคอนฟิกภาษีขายสำหรับที่อยู่ของลูกค้าในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="96002-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="96002-116">ในการตั้งค่าคอนฟิกภาษีขายจากที่อยู่ของลูกค้าในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="96002-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="96002-117">ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="96002-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="96002-118">เลือกลูกค้าเพื่อกำหนดค่าคอนฟิกที่จะสร้างใบสั่งขายให้</span><span class="sxs-lookup"><span data-stu-id="96002-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="96002-119">บนแท็บด่วน **ที่อยู่** ให้เลือกที่อยู่ที่จะตั้งค่าคอนฟิกภาษีขาย ให้เลือก **ตัวเลือกเพิ่มเติม** แล้วเลือก **ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="96002-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="96002-120">บนแท็บด่วน **ทั่วไป** ให้เลือก **กลุ่มภาษี**</span><span class="sxs-lookup"><span data-stu-id="96002-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="96002-121">ในฟิลด์ **ภาษีขาย** ให้เลือกค่าที่เหมาะสม:</span><span class="sxs-lookup"><span data-stu-id="96002-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="96002-122">การจัดส่งที่เกี่ยวข้องกับภาษีขายตามที่อยู่ของลูกค้า ที่อยู่ที่จัดส่งของบรรทัดจะระบุกลุ่มภาษีสำหรับรายการ</span><span class="sxs-lookup"><span data-stu-id="96002-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="96002-123">หากลูกค้าได้รับการจัดส่งไปยังที่อยู่ที่มีอยู่ ซึ่งมีกลุ่มภาษีที่ตั้งค่าคอนฟิกไว้แล้ว ระบบจะใช้กลุ่มภาษีที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="96002-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="96002-124">ตามค่าเริ่มต้น ที่อยู่จะไม่มีกลุ่มภาษีเมื่อสร้างที่อยู่</span><span class="sxs-lookup"><span data-stu-id="96002-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="96002-125">ตั้งค่าคอนฟิกกลุ่มภาษีขายทั่วไปในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="96002-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="96002-126">หากต้องการตั้งค่าคอนฟิกกลุ่มภาษีขายทั่วไปในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="96002-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="96002-127">ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีขาย \> กลุ่มภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="96002-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="96002-128">ในการนําทางด้านซ้าย ให้เลือกกลุ่มภาษีที่จะตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="96002-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="96002-129">บนแท็บด่วน **ภาษีตามปลายทางการขายปลีก** ให้ตั้งค่าคอนฟิกภาษีของกลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="96002-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="96002-130">การจัดส่งที่ไม่เกี่ยวข้องกับภาษีขายในที่อยู่ของลูกค้า ที่อยู่ที่จัดส่งในบรรทัดและภาษีฐานปลายทางซึ่งตั้งค่าคอนฟิกไว้สำหรับกลุ่มภาษีจะกําหนดกลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="96002-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="96002-131">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าภาษีสำหรับร้านค้าออนไลน์ตามปลายทาง](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)</span><span class="sxs-lookup"><span data-stu-id="96002-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96002-132">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="96002-132">Additional resources</span></span>

[<span data-ttu-id="96002-133">ตั้งค่าคอนฟิกภาษีขายสำหรับใบสั่งออนไลน์</span><span class="sxs-lookup"><span data-stu-id="96002-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
