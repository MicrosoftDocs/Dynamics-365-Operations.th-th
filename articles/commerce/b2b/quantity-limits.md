---
title: ตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์เกี่ยวกับไซต์อีคอมเมิร์ซของ B2B
description: หัวข้อนี้อธิบายวิธีการตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์สำหรับไซต์อีคอมเมิร์ซระหว่างธุรกิจ (B2B)
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211188"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="9803f-103">ตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์เกี่ยวกับไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="9803f-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9803f-104">หัวข้อนี้อธิบายวิธีการตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์สำหรับไซต์อีคอมเมิร์ซระหว่างธุรกิจ (B2B)</span><span class="sxs-lookup"><span data-stu-id="9803f-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="9803f-105">ผลิตภัณฑ์ส่วนใหญ่มีหน่วยวัดที่กําหนดการจัดกลุ่มของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9803f-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="9803f-106">การจัดกลุ่มจะมีผลต่อการขายผลิตภัณฑ์อย่างไร</span><span class="sxs-lookup"><span data-stu-id="9803f-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="9803f-107">ผลิตภัณฑ์บางรายการอาจมีการจัดกลุ่มปริมาณเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9803f-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="9803f-108">การจัดกลุ่มนี้จะระบุว่าผลิตภัณฑ์สามารถขายเป็นแต่ละหน่วยหรือหลายหน่วย และระบุว่าต้องมีขีดจํากัดปริมาณการสั่งต่สุดหรือสูงสุดที่ต้องปฏิบัติตาม</span><span class="sxs-lookup"><span data-stu-id="9803f-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="9803f-109">คุณลักษณะการใช้งานการกําหนดขีดจํากัดปริมาณช่วยให้มั่นใจว่าปริมาณต่ำสุด สูงสุด หลายรายการ และปริมาณมาตรฐาน ที่ตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce (ในการตั้งค่าใบสั่งเริ่มต้น หรือการตั้งค่าไซต์โปรแกรมสร้างไซต์ของ Commerce) จะใช้กับใบสั่งของลูกค้าที่จัดวางบนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="9803f-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="9803f-110">ปัจจุบันไม่สนับสนุนขีดจํากัดปริมาณผลิตภัณฑ์ในการขายหน้าร้าน (POS) และศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="9803f-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="9803f-111">ผู้ค้าปลีกหลายรายมีตัวเลือกสำหรับใบสั่งของลูกค้า (หรือใบสั่งพิเศษ) เพื่อให้ตรงกับผลิตภัณฑ์ที่หลากหลายและความต้องการในการเติมเต็ม</span><span class="sxs-lookup"><span data-stu-id="9803f-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="9803f-112">ต่อไปนี้เป็นสถานการณ์ทั่วไปบางส่วน:</span><span class="sxs-lookup"><span data-stu-id="9803f-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="9803f-113">ลูกค้าต้องการผลิตภัณฑ์ของผลิตภัณฑ์ย่อยเฉพาะเพื่อขายในหลายผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9803f-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="9803f-114">ลูกค้าต้องการรับผลิตภัณฑ์จากร้านค้าหรือสถานที่ที่ไม่ใช่ร้านค้าหรือสถานที่ที่ลูกค้าสั่งซื้อผลิตภัณฑ์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="9803f-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="9803f-115">อย่างไรก็ตาม มาตรฐานการบรรจุของร้านค้าจะแตกต่างจากมาตรฐานการบรรจุในการกระจายการขายทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="9803f-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="9803f-116">ลูกค้าต้องการซื้อผลิตภัณฑ์ที่มีข้อจํากัดที่มีขีดจํากัดปริมาณสูงสุดต่อสินค้าที่สามารถซื้อได้</span><span class="sxs-lookup"><span data-stu-id="9803f-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="9803f-117">เปิดคุณลักษณะการตั้งค่าใบสั่งเริ่มต้นในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="9803f-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="9803f-118">ก่อนที่คุณจะสามารถตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์ได้ ต้องเปิดคุณลักษณะการตั้งค่าใบสั่งเริ่มต้นในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="9803f-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="9803f-119">หากต้องการเปิดใช้งานคุณลักษณะการตั้งค่าใบสั่งเริ่มต้น ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9803f-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="9803f-120">ไปที่ **การดูแลระบบ \> พื้นที่ทำงาน \> การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="9803f-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="9803f-121">ค้นหาและเลือกคุณลักษณะ **สนับสนุนไซต์และการตั้งค่าใบสั่งเริ่มต้นในใบสั่งของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="9803f-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="9803f-122">ที่ด้านล่างของบานหน้าต่างด้านขวา ให้เลือก **เปิดใช้งานทันที**</span><span class="sxs-lookup"><span data-stu-id="9803f-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="9803f-123">กําหนดการตั้งค่าปริมาณ</span><span class="sxs-lookup"><span data-stu-id="9803f-123">Define quantity settings</span></span> 

<span data-ttu-id="9803f-124">คุณสามารถกำหนดการตั้งค่าปริมาณในหน้า **การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="9803f-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="9803f-125">ในการกําหนดการตั้งค่าปริมาณ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9803f-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="9803f-126">ไปที่ผลิตภัณฑ์ **Retail และ Commerce \> ผลิตภัณฑ์และประเภท \> ผลิตภัณฑ์ที่นำออกใช้ตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="9803f-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="9803f-127">ค้นหาผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="9803f-127">Select a released product.</span></span>
1. <span data-ttu-id="9803f-128">บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการสินค้างคงคลัง** ในกลุ่ม **การตั้งค่าใบสั่ง** ให้เลือก **การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="9803f-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="9803f-129">บนหน้า **การตั้งค่าใบสั่งเริ่มต้น** บนแท็บด่วน **ใบสั่งขาย** ในส่วน **ปริมาณการขาย** ให้ตั้งค่าปริมาณการขายของผลิตภัณฑ์ดังนี้</span><span class="sxs-lookup"><span data-stu-id="9803f-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="9803f-130">**หลากหลาย** - ปริมาณที่สามารถซื้อผลิตภัณฑ์ได้หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="9803f-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="9803f-131">**ปริมาณการสั่งขั้นต่ำ** – จํานวนต่ำสุดของผลิตภัณฑ์ที่ต้องซื้อ</span><span class="sxs-lookup"><span data-stu-id="9803f-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="9803f-132">**ปริมาณการสั่งสูงสุด** – จํานวนสูงสุดของผลิตภัณฑ์ที่สามารถซื้อได้</span><span class="sxs-lookup"><span data-stu-id="9803f-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="9803f-133">**ปริมาณการสั่งมาตรฐาน** – ปริมาณเริ่มต้นที่จะป้อนโดยอัตโนมัติเมื่อเลือกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9803f-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="9803f-134">เปิดคุณลักษณะขีดจํากัดปริมาณใบสั่ง B2B ของโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="9803f-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="9803f-135">หากต้องการเปิดคุณลักษณะขีดจํากัดปริมาณใบสั่ง B2B ของโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9803f-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9803f-136">ไปที่ **การตั้งค่าไซต์\> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="9803f-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="9803f-137">ภายใต้ **เปิดใช้งานขีดจํากัดปริมาณการสั่ง** ให้เลือก **ที่เปิดใช้งานของลูกค้า B2B** ในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="9803f-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="9803f-138">การตั้งค่าโปรแกรมสร้างไซต์ที่อัพเดตจะมีผลเฉพาะหลังจากที่อัปเดตไฟล์ app.settings.json แล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9803f-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="9803f-139">สำหรับข้อมูลเพิ่มเติม โปรดดู [SDK และอัปเดตไลบรารีโมดูล](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)</span><span class="sxs-lookup"><span data-stu-id="9803f-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9803f-140">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9803f-140">Additional resources</span></span>

[<span data-ttu-id="9803f-141">ตั้งค่าไซต์อีคอมเมิร์ซ B2B</span><span class="sxs-lookup"><span data-stu-id="9803f-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="9803f-142">สร้างลำดับชั้นการจำลององค์กรขององค์กร B2B</span><span class="sxs-lookup"><span data-stu-id="9803f-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="9803f-143">จัดการผู้ใช้คู่ค้าทางธุรกิจบนไซต์อีคอมเมิร์ซ B2B</span><span class="sxs-lookup"><span data-stu-id="9803f-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="9803f-144">ตั้งค่าคอนฟิกวิธีการชำระเงินด้วยบัญชีลูกค้าสำหรับไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="9803f-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]