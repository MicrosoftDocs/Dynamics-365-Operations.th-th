---
title: " ข้อตกลงทางการค้าและราคาพื้นฐาน"
description: 'ขั้นตอนนี้จะแนะนำการสร้างข้อตกลงทางการค้าของราคาขายเฉพาะช่องทาง '
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 022db9365f25c1d3e387870dd9d173077d864b3d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141533"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="0778c-103"> ข้อตกลงทางการค้าและราคาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0778c-103">Base price and trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0778c-104">ขั้นตอนนี้จะแนะนำการสร้างข้อตกลงทางการค้าของราคาขายเฉพาะช่องทาง </span><span class="sxs-lookup"><span data-stu-id="0778c-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="0778c-105">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="0778c-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="0778c-106">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล >การขายปลีกและการค้า > การกำหนดราคาและการจัดการส่วนลด > กลุ่มราคา > กลุ่มราคาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0778c-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="0778c-107">กลุ่มราคาคือวิธีที่ข้อตกลงทางการค้าถูกกำหนดไปยังช่องทางเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0778c-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="0778c-108">โดยใช้กลุ่มราคาเพื่อกำหนดข้อตกลงทางการค้าไปยังช่องทางที่เปิดใช้งานการกำหนดราคาเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="0778c-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="0778c-109">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0778c-109">Click **New**.</span></span>
3. <span data-ttu-id="0778c-110">ในฟิลด์ **กลุ่มราคา** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0778c-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="0778c-111">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0778c-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="0778c-112">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0778c-112">Click **Save**.</span></span>
6. <span data-ttu-id="0778c-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0778c-113">Close the page.</span></span>
7. <span data-ttu-id="0778c-114">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > Retail และ Commerce > ช่องทาง > ร้านค้า > ร้านค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0778c-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="0778c-115">ในรายการ ให้เลือก 'New York'</span><span class="sxs-lookup"><span data-stu-id="0778c-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="0778c-116">บนบานหน้าต่างการดำเนินการ คลิก **ร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="0778c-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="0778c-117">คลิก **กลุ่มราคา**</span><span class="sxs-lookup"><span data-stu-id="0778c-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="0778c-118">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0778c-118">Click **New**.</span></span>
12. <span data-ttu-id="0778c-119">ในฟิลด์ **กลุ่มราคา** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0778c-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="0778c-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0778c-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0778c-121">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0778c-121">Click **Save**.</span></span>
15. <span data-ttu-id="0778c-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0778c-122">Close the page.</span></span>
16. <span data-ttu-id="0778c-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0778c-123">Close the page.</span></span>
17. <span data-ttu-id="0778c-124">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > การขายปลีกและการค้า > ผลิตภัณฑ์และประเภท > ผลิตภัณฑ์ที่นำออกใช้ตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="0778c-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="0778c-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0778c-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="0778c-126">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="0778c-126">Click **Edit**.</span></span>
20. <span data-ttu-id="0778c-127">ขยาย fastTab ของ **การขาย**</span><span class="sxs-lookup"><span data-stu-id="0778c-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="0778c-128">ในฟิลด์ **ราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0778c-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="0778c-129">ราคานี้จะถูกใช้ถ้าไม่มีข้อตกลงทางการค้าที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="0778c-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="0778c-130">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0778c-130">Click **Save**.</span></span>
23. <span data-ttu-id="0778c-131">ใน **บานหน้าต่างการดำเนินการ** คลิก **ขาย**</span><span class="sxs-lookup"><span data-stu-id="0778c-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="0778c-132">คลิก **สร้างข้อตกลงทางการค้า**</span><span class="sxs-lookup"><span data-stu-id="0778c-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="0778c-133">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0778c-133">Click **New**.</span></span>
26. <span data-ttu-id="0778c-134">ในฟิลด์ **ชื่อ** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0778c-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="0778c-135">ในรายการ เลือก **การค้า**</span><span class="sxs-lookup"><span data-stu-id="0778c-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="0778c-136">ในข้อมูลสาธิต ชื่อสมุดรายวัน **การค้า** มีความสัมพันธ์เริ่มต้นของ **ราคา (ขาย)**</span><span class="sxs-lookup"><span data-stu-id="0778c-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="0778c-137">ซึ่งหมายความว่าบรรทัดรายการใหม่ทั้งหมดที่สร้างขึ้นจะเป็นค่าเริ่มต้นของข้อตกลงทางการค้าของราคาขาย</span><span class="sxs-lookup"><span data-stu-id="0778c-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="0778c-138">บน **บานหน้าต่างการดำเนินการ** คลิก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="0778c-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="0778c-139">ในฟิลด์ **รหัสบัญชี** เลือก 'กลุ่ม'</span><span class="sxs-lookup"><span data-stu-id="0778c-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="0778c-140">ในฟิลด์ **การเลือกบัญชี** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0778c-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="0778c-141">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0778c-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="0778c-142">ซึ่งนี่จะทำให้ลิงค์จากช่องทางไปยังกลุ่มราคากับข้อตกลงทางการค้าเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0778c-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="0778c-143">ในฟิลด์ **ความสัมพันธ์ของสินค้า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0778c-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="0778c-144">ในฟิลด์ **จำนวนในสกุลเงิน** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0778c-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="0778c-145">ใน fastTab **รายละเอียด** ให้เลือก หรือยกเลิกการเลือกกล่องกาเครื่องหมาย **ค้นหาถัดไป**</span><span class="sxs-lookup"><span data-stu-id="0778c-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="0778c-146">เมื่อ **ค้นหาถัดไป** ถูกตั้งค่าเป็น 'ใช่' กลไกการกำหนดราคาจะดำเนินต่อเพื่อค้นหาข้อตกลงทางการค้าที่ใช้ได้กับราคาขายที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="0778c-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="0778c-147">เมื่อ **ค้นหาถัดไป** ถูกตั้งค่าเป็น 'ไม่ใช่' กลไกการกำหนดราคาจะหยุดการค้นหา และใช้ข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="0778c-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="0778c-148">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="0778c-148">Click **Post**.</span></span>
36. <span data-ttu-id="0778c-149">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0778c-149">Click **OK**.</span></span>
37. <span data-ttu-id="0778c-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0778c-150">Close the page.</span></span>
38. <span data-ttu-id="0778c-151">บน **บานหน้าต่างการดำเนินการ** คลิกขาย</span><span class="sxs-lookup"><span data-stu-id="0778c-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="0778c-152">คลิก **ราคาขาย**</span><span class="sxs-lookup"><span data-stu-id="0778c-152">Click **Sales price**.</span></span>

