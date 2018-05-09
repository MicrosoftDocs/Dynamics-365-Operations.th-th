--- 
title: " ข้อตกลงทางการค้าและราคาพื้นฐาน"
description: "ขั้นตอนนี้จะแนะนำการสร้างข้อตกลงทางการค้าของราคาขายเฉพาะช่องทาง "
author: josaw1
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f730ef8e9c9c089b4ee209d8e54011e6d8798399
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="2673b-103"> ข้อตกลงทางการค้าและราคาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="2673b-103">Base price and trade agreements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2673b-104">ขั้นตอนนี้จะแนะนำการสร้างข้อตกลงทางการค้าของราคาขายเฉพาะช่องทาง </span><span class="sxs-lookup"><span data-stu-id="2673b-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="2673b-105">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="2673b-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="2673b-106">ไปยังการขายปลีกและการค้า > การกำหนดราคาและส่วนลด > กลุ่มราคา > กลุ่มราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2673b-106">Go to Retail and commerce > Pricing and discounts > Price groups > All price groups.</span></span>
    * <span data-ttu-id="2673b-107">กลุ่มราคาคือวิธีที่ข้อตกลงทางการค้าถูกกำหนดไปยังช่องทางเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2673b-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="2673b-108">โดยใช้กลุ่มราคาเพื่อกำหนดข้อตกลงทางการค้าไปยังช่องทางที่เปิดใช้งานการกำหนดราคาเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="2673b-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="2673b-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2673b-109">Click New.</span></span>
3. <span data-ttu-id="2673b-110">ในฟิลด์กลุ่มราคา ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2673b-110">In the Price groups field, type a value.</span></span>
4. <span data-ttu-id="2673b-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="2673b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2673b-112">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2673b-112">Click Save.</span></span>
6. <span data-ttu-id="2673b-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2673b-113">Close the page.</span></span>
7. <span data-ttu-id="2673b-114">ไปยังการขายปลีกและการค้า > ช่องทาง > ร้านค้าปลีก > ร้านค้าปลีกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2673b-114">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
8. <span data-ttu-id="2673b-115">ในรายการ ให้เลือก 'New York'</span><span class="sxs-lookup"><span data-stu-id="2673b-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="2673b-116">ในบานหน้าต่างการดำเนินการ คลิกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="2673b-116">On the Action Pane, click Store.</span></span>
10. <span data-ttu-id="2673b-117">คลิก กลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="2673b-117">Click Price groups.</span></span>
11. <span data-ttu-id="2673b-118">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2673b-118">Click New.</span></span>
12. <span data-ttu-id="2673b-119">ในฟิลด์กลุ่มราคา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2673b-119">In the Price groups field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2673b-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2673b-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="2673b-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2673b-121">Click Save.</span></span>
15. <span data-ttu-id="2673b-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2673b-122">Close the page.</span></span>
16. <span data-ttu-id="2673b-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2673b-123">Close the page.</span></span>
17. <span data-ttu-id="2673b-124">ไปยังการขายปลีกและการค้า > ผลิตภัณฑ์และประเภท > ผลิตภัณฑ์ที่นำออกใช้ตามประเภท</span><span class="sxs-lookup"><span data-stu-id="2673b-124">Go to Retail and commerce > Products and categories > Released products by category.</span></span>
18. <span data-ttu-id="2673b-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2673b-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="2673b-126">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="2673b-126">Click Edit.</span></span>
20. <span data-ttu-id="2673b-127">เปิดปิดการขยายของส่วนขาย</span><span class="sxs-lookup"><span data-stu-id="2673b-127">Toggle the expansion of the Sell section.</span></span>
21. <span data-ttu-id="2673b-128">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="2673b-128">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="2673b-129">ราคานี้จะถูกใช้ถ้าไม่มีข้อตกลงทางการค้าที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="2673b-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="2673b-130">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2673b-130">Click Save.</span></span>
23. <span data-ttu-id="2673b-131">ในบานหน้าต่างการดำเนินการ คลิกขาย</span><span class="sxs-lookup"><span data-stu-id="2673b-131">On the Action Pane, click Sell.</span></span>
24. <span data-ttu-id="2673b-132">คลิกสร้างข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="2673b-132">Click Create trade agreements.</span></span>
25. <span data-ttu-id="2673b-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2673b-133">Click New.</span></span>
26. <span data-ttu-id="2673b-134">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2673b-134">In the Name field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="2673b-135">ในรายการ เลือก 'การขายปลีก'</span><span class="sxs-lookup"><span data-stu-id="2673b-135">In the list, select 'Retail'.</span></span>
    * <span data-ttu-id="2673b-136">ในข้อมูลสาธิต ชื่อสมุดรายวัน 'การขายปลีก' มีความสัมพันธ์เริ่มต้นของ 'ราคา (ขาย)' </span><span class="sxs-lookup"><span data-stu-id="2673b-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="2673b-137">ซึ่งหมายความว่าบรรทัดรายการใหม่ทั้งหมดที่สร้างขึ้นจะเป็นค่าเริ่มต้นของข้อตกลงทางการค้าของราคาขาย</span><span class="sxs-lookup"><span data-stu-id="2673b-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="2673b-138">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="2673b-138">Click Lines.</span></span>
29. <span data-ttu-id="2673b-139">ในฟิลด์รหัสบัญชี เลือก 'กลุ่ม'</span><span class="sxs-lookup"><span data-stu-id="2673b-139">In the Account code field, select 'Group'.</span></span>
30. <span data-ttu-id="2673b-140">ในฟิลด์การเลือกบัญชี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2673b-140">In the Account selection field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="2673b-141">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2673b-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2673b-142">ซึ่งนี่จะทำให้ลิงค์จากช่องทางไปยังกลุ่มราคากับข้อตกลงทางการค้าเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2673b-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="2673b-143">ในฟิลด์หมายเลขความสัมพันธ์ของสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2673b-143">In the Item relation field, type a value.</span></span>
33. <span data-ttu-id="2673b-144">ในฟิลด์จำนวนในสกุลเงิน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="2673b-144">In the Amount in currency field, enter a number.</span></span>
34. <span data-ttu-id="2673b-145">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="2673b-145">Check or uncheck the Find next checkbox.</span></span>
    * <span data-ttu-id="2673b-146">เมื่อค้นหาถัดไปถูกตั้งค่าเป็น 'ใช่' กลไกจัดการการกำหนดราคาจะดำเนินต่อเพื่อค้นหาข้อตกลงทางการค้าที่ใช้ได้กับราคาขายที่ต่ำกว่า </span><span class="sxs-lookup"><span data-stu-id="2673b-146">When Find next is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="2673b-147">เมื่อค้นหาถัดไปถูกตั้งค่าเป็น 'ไม่ใช่' กลไกจัดการราคาก็จะหยุดการค้นหา และใช้ข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="2673b-147">When Find next is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="2673b-148">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2673b-148">Click Post.</span></span>
36. <span data-ttu-id="2673b-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2673b-149">Click OK.</span></span>
37. <span data-ttu-id="2673b-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2673b-150">Close the page.</span></span>
38. <span data-ttu-id="2673b-151">ในบานหน้าต่างการดำเนินการ คลิกขาย</span><span class="sxs-lookup"><span data-stu-id="2673b-151">On the Action Pane, click Sell.</span></span>
39. <span data-ttu-id="2673b-152">คลิก ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="2673b-152">Click Sales price.</span></span>


