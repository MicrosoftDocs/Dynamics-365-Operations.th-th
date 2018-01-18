--- 
title: " การปรับปรุงราคาในการขายปลีก"
description: "ขั้นตอนนี้จะนำไปสู่การสร้างการปรับปรุงราคาขายปลีก "
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: ba6301329b23b8b4e167e292c1126806bf07d3ba
ms.contentlocale: th-th
ms.lasthandoff: 01/18/2018

---
# <a name="retail-price-adjustments"></a><span data-ttu-id="b61d7-103"> การปรับปรุงราคาในการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="b61d7-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b61d7-104">ขั้นตอนนี้จะนำไปสู่การสร้างการปรับปรุงราคาขายปลีก </span><span class="sxs-lookup"><span data-stu-id="b61d7-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="b61d7-105">การปรับปรุงราคาขายปลีกสามารถตั้งค่าราคาขายของสินค้าโดยตรง หรือปรับเปลี่ยนราคาขายพื้นฐานหรือราคาขายตามข้อตกลงทางการค้าได้ </span><span class="sxs-lookup"><span data-stu-id="b61d7-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="b61d7-106">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="b61d7-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="b61d7-107">คลิกการจัดการการกำหนดราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="b61d7-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="b61d7-108">คลิกแท็บการปรับปรุงราคา</span><span class="sxs-lookup"><span data-stu-id="b61d7-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="b61d7-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b61d7-109">Click New.</span></span>
    * <span data-ttu-id="b61d7-110">จากที่นี่ คุณสามารถสร้างกฎราคาและส่วนลดที่ใช้กันมากที่สุดได้ทั้งหมด รวมถึง ส่วนลดการขายปลีก การปรับปรุงราคา สมุดรายวันข้อตกลงทางการค้า และกฎการกำหนดราคาประเภท</span><span class="sxs-lookup"><span data-stu-id="b61d7-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="b61d7-111">คลิกการปรับปรุงราคา</span><span class="sxs-lookup"><span data-stu-id="b61d7-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="b61d7-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="b61d7-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="b61d7-113">ขยายส่วนรายการ</span><span class="sxs-lookup"><span data-stu-id="b61d7-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="b61d7-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b61d7-114">Click Add.</span></span>
    * <span data-ttu-id="b61d7-115">สำหรับตัวอย่างนี้ ป้อน '81126' ในฟิลด์ผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="b61d7-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="b61d7-116">จากนั้น ป้อน '10.0' ในฟิลด์เปอร์เซ็นต์ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="b61d7-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="b61d7-117">การปรับปรุงราคาส่วนลดชนิดเปอร์เซ็นต์จะลดฐานราคาขายหรือราคาขายตามข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="b61d7-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="b61d7-118">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b61d7-118">Click Add.</span></span>
    * <span data-ttu-id="b61d7-119">สำหรับตัวอย่างนี้ ป้อน '81125' ในฟิลด์ผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="b61d7-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="b61d7-120">จากนั้น เลือก 'ยอดส่วนลดเงินสด' ในฟิลด์วิธีการให้ส่วนลดนั้น </span><span class="sxs-lookup"><span data-stu-id="b61d7-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="b61d7-121">ในตอนท้าย ป้อน '5.0' ในฟิลด์ยอดส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="b61d7-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="b61d7-122">ชนิดส่วนลดแบบยอดส่วนลดเงินสดเป็นยอดเงินที่นำออกจากราคาฐานหรือราคาข้อตกลงทางการค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="b61d7-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="b61d7-123">คลิกกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="b61d7-123">Click Price groups.</span></span>
    * <span data-ttu-id="b61d7-124">เลือก 'RP-Houston' ในฟิลด์กลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="b61d7-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="b61d7-125">ซึ่งนี่จะเชื่อมโยงการปรับปรุงราคาไปยังร้านค้า Houston</span><span class="sxs-lookup"><span data-stu-id="b61d7-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="b61d7-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b61d7-126">Click Save.</span></span>
11. <span data-ttu-id="b61d7-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b61d7-127">Close the page.</span></span>
12. <span data-ttu-id="b61d7-128">ในฟิลด์สถานะ เลือก 'เปิดใช้งานแล้ว'</span><span class="sxs-lookup"><span data-stu-id="b61d7-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="b61d7-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b61d7-129">Click Save.</span></span>
14. <span data-ttu-id="b61d7-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b61d7-130">Close the page.</span></span>
15. <span data-ttu-id="b61d7-131">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="b61d7-131">Refresh the page.</span></span>


