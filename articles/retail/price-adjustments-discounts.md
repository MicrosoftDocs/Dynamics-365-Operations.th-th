---
title: การปรับปรุงราคาและส่วนลด
description: บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงราคาและส่วนลดใน Microsoft Dynamics 365 for Retail
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 61ac8e5fbdc4d91bb5bc5372a7fb96633043473a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549463"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="06043-103">การปรับปรุงราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="06043-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06043-104">บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงราคาและส่วนลดใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="06043-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="06043-105">ใน Dynamics 365 for Retail คุณสามารถทำการปรับราคาไปยังผลิตภัณฑ์ และยังสามารถตั้งค่าส่วนลดที่ใช้กับสินค้าในรายการ หรือธุรกรรมที่ point of sale (POS) ในใบสั่งขายของศูนย์บริการ หรือในใบสั่งออนไลน์</span><span class="sxs-lookup"><span data-stu-id="06043-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="06043-106">ทั้งการปรับปรุงทั้งราคาและส่วนลดสามารถเชื่อมโยงกับกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="06043-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="06043-107">สำหรับทั้งการปรับปรุงราคาและส่วนลด คุณสามารถระบุวันที่เริ่มต้นและวันที่สิ้นสุดวันเดียวหรือรอบระยะเวลาที่เกิดซ้ำ รหัสส่วนลด และคุณลักษณะเพิ่มเติมบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="06043-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="06043-108">การปรับปรุงราคาและส่วนลดสามารถใช้กับผลิตภัณฑ์ ตัวแปร หรือประเภท</span><span class="sxs-lookup"><span data-stu-id="06043-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="06043-109">ถ้าส่วนลดมากกว่าหนึ่งส่วนลดใช้กับผลิตภัณฑ์ ลูกค้าอาจได้รับส่วนลดหรือยอดส่วนลดที่รวม โดยขึ้นอยู่กับการตั้งค่าคอนฟิกของส่วนลด</span><span class="sxs-lookup"><span data-stu-id="06043-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="06043-110">Dynamics 365 for Retail นำส่วนลดหรือชุดข้อมูลของส่วนลดที่ให้ราคาที่ดีที่สุดไปใช้กับลูกค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="06043-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="06043-111">เมื่อคุณตั้งค่าการปรับปรุงราคาหรือส่วนลด ให้แน่ใจที่จะยืนยันว่า กลุ่มราคาถูกกำหนดให้กับช่องทางที่ถูกต้อง แค็ตตาล็อก การสังกัด หรือโปรแกรมตอบแทนลูกค้าสมาชิกที่คุณต้องการส่วนลดไปใช้ต่อ</span><span class="sxs-lookup"><span data-stu-id="06043-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="06043-112">นอกจากนี้ ถ้าคุณต้องการสร้างรหัสส่วนลดโดยอัตโนมัติ ตั้งค่าลำดับหมายเลขบนหน้า **พารามิเตอร์การขายปลีก** ก่อนที่คุณกำหนดการปรับปรุงราคาใหม่หรือส่วนลด</span><span class="sxs-lookup"><span data-stu-id="06043-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="06043-113">คุณสามารถลบการปรับปรุงราคาหรือส่วนลดได้ </span><span class="sxs-lookup"><span data-stu-id="06043-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="06043-114">อย่างไรก็ตาม ข้อมูลทางสถิติจะหายไป</span><span class="sxs-lookup"><span data-stu-id="06043-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="06043-115">ชนิดของส่วนลด</span><span class="sxs-lookup"><span data-stu-id="06043-115">Types of discounts</span></span>

<span data-ttu-id="06043-116">มีส่วนลดการขายปลีกสี่ชนิด:</span><span class="sxs-lookup"><span data-stu-id="06043-116">There are four types of retail discounts:</span></span>

- <span data-ttu-id="06043-117">**ส่วนลดแบบง่าย** – เปอร์เซ็นต์หรือยอดเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="06043-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="06043-118">**ส่วนลดปริมาณ**– ส่วนลดที่ถูกใช้เมื่อผลิตภัณฑ์สองอย่างขึ้นไปถูกซื้อไป</span><span class="sxs-lookup"><span data-stu-id="06043-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="06043-119">**ส่วนลดสำหรับการซื้อคละกัน**– ส่วนลดที่ถูกใช้เมื่อชุดที่ระบุของผลิตภัณฑ์ถูกซื้อไป</span><span class="sxs-lookup"><span data-stu-id="06043-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="06043-120">**ส่วนลดจำกัด**– ส่วนลดที่ถูกใช้เมื่อผลรวมของธุรกรรมมากกว่ายอดเงินที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="06043-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="06043-121">ทั้งการปรับปรุงทั้งราคาและส่วนลดสามารถเชื่อมโยงกับกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="06043-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="06043-122">กลุ่มราคาสามารถเชื่อมโยงกับช่องทาง แค็ตตาล็อก สังกัด และโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="06043-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
