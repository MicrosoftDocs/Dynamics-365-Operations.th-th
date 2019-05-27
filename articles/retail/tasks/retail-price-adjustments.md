---
title: " การปรับปรุงราคาในการขายปลีก"
description: 'ขั้นตอนนี้จะนำไปสู่การสร้างการปรับปรุงราคาขายปลีก '
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9427d3955e5442e301c416e2960e071ca5d85a3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550052"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="11630-103"> การปรับปรุงราคาในการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="11630-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="11630-104">ขั้นตอนนี้จะนำไปสู่การสร้างการปรับปรุงราคาขายปลีก </span><span class="sxs-lookup"><span data-stu-id="11630-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="11630-105">การปรับปรุงราคาขายปลีกสามารถตั้งค่าราคาขายของสินค้าโดยตรง หรือปรับเปลี่ยนราคาขายพื้นฐานหรือราคาขายตามข้อตกลงทางการค้าได้ </span><span class="sxs-lookup"><span data-stu-id="11630-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="11630-106">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="11630-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="11630-107">คลิกการจัดการการกำหนดราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="11630-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="11630-108">คลิกแท็บการปรับปรุงราคา</span><span class="sxs-lookup"><span data-stu-id="11630-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="11630-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="11630-109">Click New.</span></span>
    * <span data-ttu-id="11630-110">จากที่นี่ คุณสามารถสร้างกฎราคาและส่วนลดที่ใช้กันมากที่สุดได้ทั้งหมด รวมถึง ส่วนลดการขายปลีก การปรับปรุงราคา สมุดรายวันข้อตกลงทางการค้า และกฎการกำหนดราคาประเภท</span><span class="sxs-lookup"><span data-stu-id="11630-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="11630-111">คลิกการปรับปรุงราคา</span><span class="sxs-lookup"><span data-stu-id="11630-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="11630-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="11630-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="11630-113">ขยายส่วนรายการ</span><span class="sxs-lookup"><span data-stu-id="11630-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="11630-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="11630-114">Click Add.</span></span>
    * <span data-ttu-id="11630-115">สำหรับตัวอย่างนี้ ป้อน '81126' ในฟิลด์ผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="11630-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="11630-116">จากนั้น ป้อน '10.0' ในฟิลด์เปอร์เซ็นต์ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="11630-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="11630-117">การปรับปรุงราคาส่วนลดชนิดเปอร์เซ็นต์จะลดฐานราคาขายหรือราคาขายตามข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="11630-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="11630-118">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="11630-118">Click Add.</span></span>
    * <span data-ttu-id="11630-119">สำหรับตัวอย่างนี้ ป้อน '81125' ในฟิลด์ผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="11630-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="11630-120">จากนั้น เลือก 'ยอดส่วนลดเงินสด' ในฟิลด์วิธีการให้ส่วนลดนั้น </span><span class="sxs-lookup"><span data-stu-id="11630-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="11630-121">ในตอนท้าย ป้อน '5.0' ในฟิลด์ยอดส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="11630-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="11630-122">ชนิดส่วนลดแบบยอดส่วนลดเงินสดเป็นยอดเงินที่นำออกจากราคาฐานหรือราคาข้อตกลงทางการค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="11630-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="11630-123">คลิกกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="11630-123">Click Price groups.</span></span>
    * <span data-ttu-id="11630-124">เลือก 'RP-Houston' ในฟิลด์กลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="11630-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="11630-125">ซึ่งนี่จะเชื่อมโยงการปรับปรุงราคาไปยังร้านค้า Houston</span><span class="sxs-lookup"><span data-stu-id="11630-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="11630-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="11630-126">Click Save.</span></span>
11. <span data-ttu-id="11630-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="11630-127">Close the page.</span></span>
12. <span data-ttu-id="11630-128">ในฟิลด์สถานะ เลือก 'เปิดใช้งานแล้ว'</span><span class="sxs-lookup"><span data-stu-id="11630-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="11630-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="11630-129">Click Save.</span></span>
14. <span data-ttu-id="11630-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="11630-130">Close the page.</span></span>
15. <span data-ttu-id="11630-131">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="11630-131">Refresh the page.</span></span>

