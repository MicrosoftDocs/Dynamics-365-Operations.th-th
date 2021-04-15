---
title: " การปรับปรุงราคาในการขายปลีก"
description: ขั้นตอนนี้จะนำไปสู่การสร้างการปรับปรุงราคาทางการค้า
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e6ce8ca1d9f63e7ddf6af897a6de5544e4edd9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802586"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="728ad-103"> การปรับปรุงราคาในการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="728ad-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="728ad-104">ขั้นตอนนี้จะนำไปสู่การสร้างการปรับปรุงราคาทางการค้า</span><span class="sxs-lookup"><span data-stu-id="728ad-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="728ad-105">การปรับปรุงราคาสามารถตั้งค่าราคาขายของสินค้าโดยตรง หรือปรับเปลี่ยนราคาขายพื้นฐานหรือราคาขายตามข้อตกลงทางการค้าได้ </span><span class="sxs-lookup"><span data-stu-id="728ad-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="728ad-106">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="728ad-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="728ad-107">คลิกการจัดการการกำหนดราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="728ad-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="728ad-108">คลิกแท็บการปรับปรุงราคา</span><span class="sxs-lookup"><span data-stu-id="728ad-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="728ad-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="728ad-109">Click New.</span></span>
    * <span data-ttu-id="728ad-110">จากที่นี่ คุณสามารถสร้างกฎราคาและส่วนลดที่ใช้กันมากที่สุดได้ทั้งหมด รวมถึง กฎส่วนลด การปรับปรุงราคา สมุดรายวันข้อตกลงทางการค้า และกฎการกำหนดราคาประเภท</span><span class="sxs-lookup"><span data-stu-id="728ad-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="728ad-111">คลิกการปรับปรุงราคา</span><span class="sxs-lookup"><span data-stu-id="728ad-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="728ad-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="728ad-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="728ad-113">ขยายส่วนรายการ</span><span class="sxs-lookup"><span data-stu-id="728ad-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="728ad-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="728ad-114">Click Add.</span></span>
    * <span data-ttu-id="728ad-115">สำหรับตัวอย่างนี้ ป้อน '81126' ในฟิลด์ผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="728ad-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="728ad-116">จากนั้น ป้อน '10.0' ในฟิลด์เปอร์เซ็นต์ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="728ad-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="728ad-117">การปรับปรุงราคาส่วนลดชนิดเปอร์เซ็นต์จะลดฐานราคาขายหรือราคาขายตามข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="728ad-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="728ad-118">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="728ad-118">Click Add.</span></span>
    * <span data-ttu-id="728ad-119">สำหรับตัวอย่างนี้ ป้อน '81125' ในฟิลด์ผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="728ad-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="728ad-120">จากนั้น เลือก 'ยอดส่วนลดเงินสด' ในฟิลด์วิธีการให้ส่วนลดนั้น </span><span class="sxs-lookup"><span data-stu-id="728ad-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="728ad-121">ในตอนท้าย ป้อน '5.0' ในฟิลด์ยอดส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="728ad-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="728ad-122">ชนิดส่วนลดแบบยอดส่วนลดเงินสดเป็นยอดเงินที่นำออกจากราคาฐานหรือราคาข้อตกลงทางการค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="728ad-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="728ad-123">คลิกกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="728ad-123">Click Price groups.</span></span>
    * <span data-ttu-id="728ad-124">เลือก 'RP-Houston' ในฟิลด์กลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="728ad-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="728ad-125">ซึ่งนี่จะเชื่อมโยงการปรับปรุงราคาไปยังร้านค้า Houston</span><span class="sxs-lookup"><span data-stu-id="728ad-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="728ad-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="728ad-126">Click Save.</span></span>
11. <span data-ttu-id="728ad-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="728ad-127">Close the page.</span></span>
12. <span data-ttu-id="728ad-128">ในฟิลด์สถานะ เลือก 'เปิดใช้งานแล้ว'</span><span class="sxs-lookup"><span data-stu-id="728ad-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="728ad-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="728ad-129">Click Save.</span></span>
14. <span data-ttu-id="728ad-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="728ad-130">Close the page.</span></span>
15. <span data-ttu-id="728ad-131">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="728ad-131">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]