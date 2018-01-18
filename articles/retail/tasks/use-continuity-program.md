--- 
title: " ใช้โปรแกรมความต่อเนื่อง"
description: "กระบวนงานนี้แนะนำการขายโปรแกรมความต่อเนื่อง และการประมวลผลใบสั่งขายที่เกี่ยวข้อง "
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 111aa3c653f7733031e7c43a52a33ad9219530c5
ms.contentlocale: th-th
ms.lasthandoff: 01/18/2018

---
# <a name="use-a-continuity-program"></a><span data-ttu-id="2b280-103"> ใช้โปรแกรมความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="2b280-103">Use a continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2b280-104">กระบวนงานนี้แนะนำการขายโปรแกรมความต่อเนื่อง และการประมวลผลใบสั่งขายที่เกี่ยวข้อง </span><span class="sxs-lookup"><span data-stu-id="2b280-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="2b280-105">เมื่อต้องการดำเนินกระบวนงานนี้ให้เสร็จสมบูรณ์ จะต้องตั้งค่าผู้ใช้เป็นผู้ใช้ศูนย์บริการ </span><span class="sxs-lookup"><span data-stu-id="2b280-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="2b280-106">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="2b280-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="2b280-107">ไปที่ การขายปลีกและการค้าขายสินค้า > ลูกค้า > บริการลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2b280-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="2b280-108">ในฟิลด์ SearchText พิมพ์ 'Karen' จากนั้น กดคีย์ Tab</span><span class="sxs-lookup"><span data-stu-id="2b280-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="2b280-109">กล่องโต้ตอบการค้นหาขั้นสูงควรป๊อปอัพขึ้นมา </span><span class="sxs-lookup"><span data-stu-id="2b280-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="2b280-110">หากไม่ป๊อปอัพขึ้นมา ให้คลิก ค้นหา ที่ด้านขวาของฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="2b280-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="2b280-111">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2b280-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2b280-112">ควรมีเพียงแถวเดียวที่แสดง Karen Berg </span><span class="sxs-lookup"><span data-stu-id="2b280-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="2b280-113">เลือกแถวโดยคลิกที่คอลัมน์เครื่องหมายเลือกทางด้านซ้ายสุดของกริด</span><span class="sxs-lookup"><span data-stu-id="2b280-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="2b280-114">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="2b280-114">Click Select.</span></span>
5. <span data-ttu-id="2b280-115">คลิกใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="2b280-115">Click New sales order.</span></span>
    * <span data-ttu-id="2b280-116">เป็นความคิดที่ดีที่จะบันทึกหมายเลขใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="2b280-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="2b280-117">คุณจะจำเป็นต้องใช้ในกระบวนงานนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="2b280-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="2b280-118">ในฟิลด์หมายเลขสินค้า พิมพ์ '88000' จากนั้น กดคีย์ Tab</span><span class="sxs-lookup"><span data-stu-id="2b280-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="2b280-119">นี่คือสินค้าที่ต่อเนื่องในข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="2b280-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="2b280-120">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2b280-120">Click Complete.</span></span>
8. <span data-ttu-id="2b280-121">ในฟิลด์วิธีการชำระเงิน ให้ป้อน 'Visa'</span><span class="sxs-lookup"><span data-stu-id="2b280-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="2b280-122">คลิก เพิ่มบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="2b280-122">Click Add credit card.</span></span>
    * <span data-ttu-id="2b280-123">ป้อนข้อมูลบัตรเครดิตที่จำเป็นในหน้านี้</span><span class="sxs-lookup"><span data-stu-id="2b280-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="2b280-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2b280-124">Click OK.</span></span>
11. <span data-ttu-id="2b280-125">ขยายส่วนการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2b280-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="2b280-126">เมื่อต้องการส่งใบสั่งศูนย์บริการ จะต้องป้อนการชำระเงินสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2b280-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="2b280-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2b280-127">Click OK.</span></span>
13. <span data-ttu-id="2b280-128">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="2b280-128">Click Submit.</span></span>
    * <span data-ttu-id="2b280-129">คุณดำเนินการสร้างใบสั่งที่มีความต่อเนื่องใหม่เสร็จแล้ว </span><span class="sxs-lookup"><span data-stu-id="2b280-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="2b280-130">ถัดไป คุณจะรันการประมวลผลชุดงานสองรายการที่จะใช้ในการประมวลผลใบสั่งที่มีความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="2b280-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="2b280-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2b280-131">Close the page.</span></span>
15. <span data-ttu-id="2b280-132">ไปที่ การขายปลีกและการค้า > ความต่อเนื่อง > ดำเนินการชำระเงินที่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="2b280-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="2b280-133">ในฟิลด์สินค้าที่ต่อเนื่อง พิมพ์ '88000' จากนั้น กดคีย์ Tab</span><span class="sxs-lookup"><span data-stu-id="2b280-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="2b280-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2b280-134">Click OK.</span></span>
18. <span data-ttu-id="2b280-135">ไปที่ การขายปลีกและการค้า > ความต่อเนื่อง > สร้างใบสั่งรองที่มีความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="2b280-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="2b280-136">กระบวนการนี้จะสร้างใบสั่งขายใหม่ที่ขึ้นอยู่กับการตั้งค่าของโปรแกรมความต่อเนื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b280-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="2b280-137">ในฟิลด์สินค้าที่ต่อเนื่อง พิมพ์ '88000' จากนั้น กดคีย์ Tab</span><span class="sxs-lookup"><span data-stu-id="2b280-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="2b280-138">สินค้า '88000' คือสินค้าที่ต่อเนื่องในข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="2b280-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="2b280-139">ในฟิลด์ใบสั่งขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2b280-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="2b280-140">ป้อนหมายเลขใบสั่งขายที่คุณบันทึกไว้ก่อนหน้านี้ในกระบวนงาน </span><span class="sxs-lookup"><span data-stu-id="2b280-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="2b280-141">ซึ่งจะทำให้ใช้เวลาในการประมวลผลสำหรับกระบวนงานนี้น้อยที่สุด </span><span class="sxs-lookup"><span data-stu-id="2b280-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="2b280-142">ฟิลด์ใบสั่งขายไม่จำเป็นต้องระบุ--คุณสามารถประมวลผลใบสั่งทั้งหมดสำหรับโปรแกรมหนึ่งๆ ได้</span><span class="sxs-lookup"><span data-stu-id="2b280-142">The Sales order field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="2b280-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2b280-143">Click OK.</span></span>


