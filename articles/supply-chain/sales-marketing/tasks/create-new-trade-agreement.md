---
title: สร้างข้อตกลงทางการค้าใหม่
description: 'ขั้นตอนนี้แสดงวิธีการสร้างข้อตกลงทางการค้าที่คุณลงทะเบียนราคาขายใหม่ของผลิตภัณฑ์ซึ่งคุณได้ตกลงกับลูกค้าแต่ละราย '
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43426e77c30e46f4dd1cc117c38cf6ba5437655b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987376"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="207b4-103">สร้างข้อตกลงทางการค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="207b4-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="207b4-104">ขั้นตอนนี้แสดงวิธีการสร้างข้อตกลงทางการค้าที่คุณลงทะเบียนราคาขายใหม่ของผลิตภัณฑ์ซึ่งคุณได้ตกลงกับลูกค้าแต่ละราย </span><span class="sxs-lookup"><span data-stu-id="207b4-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="207b4-105">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="207b4-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="207b4-106">ถ้าคุณกำลังใช้ข้อมูลของคุณเอง ก่อนที่คุณเริ่มทำตามคำแนะนำนี้ คุณจำเป็นต้องแน่ใจว่าชื่อสมุดรายวันข้อตกลงทางการค้าปรากฎอยู่ที่ที่ความสัมพันธ์เริ่มต้นถูกตั้งค่าเป็น "ราคา (การขาย)"</span><span class="sxs-lookup"><span data-stu-id="207b4-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="207b4-107">สร้างและลงรายการสมุดรายวันข้อตกลงทางการค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="207b4-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="207b4-108">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การขายและการตลาด > ราคาและส่วนลด > สมุดรายวันข้อตกลงทางค้า**</span><span class="sxs-lookup"><span data-stu-id="207b4-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="207b4-109">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="207b4-109">Click **New**.</span></span>
3. <span data-ttu-id="207b4-110">ในฟิลด์ **ชื่อ** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="207b4-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="207b4-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="207b4-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="207b4-112">บน **บานหน้าต่างการดำเนินการ** คลิก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="207b4-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="207b4-113">ในฟิลด์ **รหัสบัญชี** เลือก 'ตาราง'</span><span class="sxs-lookup"><span data-stu-id="207b4-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="207b4-114">ในตัวอย่างนี้ คุณกำลังอัพเดตราคาสำหรับลูกค้าเฉพาะราย ซึ่งหมายความว่า คุณต้องเลือกตาราง </span><span class="sxs-lookup"><span data-stu-id="207b4-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="207b4-115">ถ้าคุณกำลังปรับปรุงราคาของรายการผลิตภัณฑ์ คุณจะต้องเลือก 'ทั้งหมด' เพื่อให้ราคาใหม่มีผลบังคับใช้สำหรับลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="207b4-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="207b4-116">ถ้าคุณได้รับความแตกต่างของราคาระหว่างเซ็กเมนต์ลูกค้าอื่น คุณจะต้องเลือกกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="207b4-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="207b4-117">เมื่อต้องการเลือกกลุ่ม คุณต้องตั้งค่าราคาของกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="207b4-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="207b4-118">ในฟิลด์ **การเลือกบัญชี** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="207b4-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="207b4-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="207b4-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="207b4-120">ในฟิลด์ **รหัสสินค้า** เลือก 'ตาราง'</span><span class="sxs-lookup"><span data-stu-id="207b4-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="207b4-121">เมื่อคุณป้อนข้อตกลงทางการค้าของชนิด 'ราคา (การขาย)' คุณต้องเลือกเฉพาะ 'ตาราง' ในฟิลด์ **รหัสสินค้า**</span><span class="sxs-lookup"><span data-stu-id="207b4-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="207b4-122">ทั้งนี้เนื่องจากราคาเป็นค่าจำนวนเต็ม และต้องไม่เหมือนกันสำหรับผลิตภัณฑ์ทั้งหมดหรือกลุ่มของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="207b4-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="207b4-123">ในฟิลด์ **ความสัมพันธ์ของสินค้า** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="207b4-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="207b4-124">ในรายการ เลือกผลิตภัณฑ์ที่คุณต้องการรวมไว้ในข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="207b4-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="207b4-125">ทำบันทึกของผลิตภัณฑ์ที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="207b4-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="207b4-126">ในฟิลด์ **เริ่มต้น** ให้ป้อนปริมาณต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="207b4-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="207b4-127">ถ้าลูกค้ามีใบสั่งปริมาณต่ำสุดก่อนที่จะสามารถแก้ไขสำหรับราคาใหม่ แล้วคุณจำเป็นต้องระบุปริมาณที่นี่</span><span class="sxs-lookup"><span data-stu-id="207b4-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="207b4-128">ป้อนค่าในฟิลด์ **สิ้นสุด** เพื่อระบุว่าปริมาณสูงสุดที่สูงกว่าราคาของข้อตกลงจะไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="207b4-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="207b4-129">ถ้าคุณเสนอราคาและส่วนลดตามการแบ่งปริมาณหลายรายการ จากนั้น ให้ระบุวงเล็บปริมาณแต่ละรายการเป็นคู่ของปริมาณต่ำสุดและสูงสุดในฟิลด์ **เริ่มต้น** และ **สิ้นสุด** ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="207b4-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="207b4-130">ในฟิลด์ **ยอดเงินในสกุลเงิน** ให้ป้อนราคา</span><span class="sxs-lookup"><span data-stu-id="207b4-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="207b4-131">ภายใต้ส่วน **รายละเอียด** ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่ที่ข้อตกลงนี้จะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="207b4-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="207b4-132">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="207b4-132">Click **Save**.</span></span>
16. <span data-ttu-id="207b4-133">คลิก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="207b4-133">Click **Validate**.</span></span>
17. <span data-ttu-id="207b4-134">คลิก **ตรวจสอบความถูกต้องรายการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="207b4-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="207b4-135">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="207b4-135">Click **OK**.</span></span>
19. <span data-ttu-id="207b4-136">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="207b4-136">Click **Post**.</span></span>
20. <span data-ttu-id="207b4-137">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="207b4-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="207b4-138">ดูข้อตกลงทางการค้าที่สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="207b4-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="207b4-139">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="207b4-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="207b4-140">ในรายการ ค้นหาและเลือกผลิตภัณฑ์ที่คุณอัพเดตราคา</span><span class="sxs-lookup"><span data-stu-id="207b4-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="207b4-141">ใน **บานหน้าต่างการดำเนินการ** คลิก **ขาย**</span><span class="sxs-lookup"><span data-stu-id="207b4-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="207b4-142">คลิก **ดูข้อตกลงทางการค้า**</span><span class="sxs-lookup"><span data-stu-id="207b4-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="207b4-143">ตรวจทานรายละเอียดของราคาที่ตกลงทางการค้าที่คุณเพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="207b4-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="207b4-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="207b4-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="207b4-145">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="207b4-145">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="207b4-146">บล็อกของชุมชน</span><span class="sxs-lookup"><span data-stu-id="207b4-146">Community blogs</span></span>
- [<span data-ttu-id="207b4-147">ราคาขายใน Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="207b4-147">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
