--- 
title: "สร้างข้อตกลงทางการค้าใหม่"
description: "ขั้นตอนนี้แสดงวิธีการสร้างข้อตกลงทางการค้าที่คุณลงทะเบียนราคาขายใหม่ของผลิตภัณฑ์ซึ่งคุณได้ตกลงกับลูกค้าแต่ละราย "
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="a98d6-103">สร้างข้อตกลงทางการค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="a98d6-103">Create a new trade agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a98d6-104">ขั้นตอนนี้แสดงวิธีการสร้างข้อตกลงทางการค้าที่คุณลงทะเบียนราคาขายใหม่ของผลิตภัณฑ์ซึ่งคุณได้ตกลงกับลูกค้าแต่ละราย </span><span class="sxs-lookup"><span data-stu-id="a98d6-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="a98d6-105">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="a98d6-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a98d6-106">ถ้าคุณกำลังใช้ข้อมูลของคุณเอง ก่อนที่คุณเริ่มทำตามคำแนะนำนี้ คุณจำเป็นต้องแน่ใจว่าชื่อสมุดรายวันข้อตกลงทางการค้าปรากฎอยู่ที่ที่ความสัมพันธ์เริ่มต้นถูกตั้งค่าเป็น "ราคา (ขาย)"</span><span class="sxs-lookup"><span data-stu-id="a98d6-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="a98d6-107">สร้างและลงรายการสมุดรายวันข้อตกลงทางการค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="a98d6-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="a98d6-108">ไปยัง การขายและการตลาด > ราคาและส่วนลด > สมุดรายวันข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="a98d6-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="a98d6-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a98d6-109">Click New.</span></span>
3. <span data-ttu-id="a98d6-110">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a98d6-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a98d6-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a98d6-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a98d6-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a98d6-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a98d6-113">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="a98d6-113">Click Lines.</span></span>
7. <span data-ttu-id="a98d6-114">ในฟิลด์รหัสบัญชี เลือก 'ตาราง' </span><span class="sxs-lookup"><span data-stu-id="a98d6-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="a98d6-115">ในตัวอย่างนี้ คุณกำลังอัพเดตราคาสำหรับลูกค้าเฉพาะราย ซึ่งหมายความว่า คุณต้องเลือกตาราง </span><span class="sxs-lookup"><span data-stu-id="a98d6-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="a98d6-116">ถ้าคุณกำลังอัพเดทราคาของรายการผลิตภัณฑ์ คุณจะต้องเลือกทั้งหมด เพื่อให้ราคาใหม่มีผลบังคับใช้สำหรับลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a98d6-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="a98d6-117">ถ้าคุณได้รับความแตกต่างของราคาระหว่างเซ็กเมนต์ลูกค้าอื่น คุณจะต้องเลือกกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="a98d6-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="a98d6-118">เมื่อต้องการเลือกกลุ่ม คุณต้องตั้งค่าราคาของกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a98d6-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="a98d6-119">ในฟิลด์การเลือกบัญชี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a98d6-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a98d6-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a98d6-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a98d6-121">ในฟิลด์รหัสสินค้า ให้เลือก 'ตาราง'</span><span class="sxs-lookup"><span data-stu-id="a98d6-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="a98d6-122">เมื่อคุณป้อนข้อตกลงทางการค้าของชนิด 'ราคา (ขาย)' คุณต้องเลือกเฉพาะ 'ตาราง' ในฟิลด์รหัสสินค้า </span><span class="sxs-lookup"><span data-stu-id="a98d6-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="a98d6-123">ทั้งนี้เนื่องจากราคาเป็นค่าจำนวนเต็ม และต้องไม่เหมือนกันสำหรับผลิตภัณฑ์ทั้งหมดหรือกลุ่มของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a98d6-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="a98d6-124">ในฟิลด์ความสัมพันธ์ของสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a98d6-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="a98d6-125">ในรายการ เลือกผลิตภัณฑ์ที่คุณต้องการรวมไว้ในข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="a98d6-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="a98d6-126">ทำบันทึกของผลิตภัณฑ์ที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="a98d6-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="a98d6-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a98d6-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a98d6-128">ในฟิลด์เริ่มต้น ป้อนปริมาณต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="a98d6-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="a98d6-129">ถ้าลูกค้าต้องการสั่งสินค้าในปริมาณต่ำสุดก่อนที่จะสามารถมีสิทธิได้รับราคาใหม่ คุณจำเป็นต้องระบุปริมาณที่นี่</span><span class="sxs-lookup"><span data-stu-id="a98d6-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="a98d6-130">ป้อนค่าในฟิลด์ To เพื่อระบุปริมาณสูงสุดสำหรับราคาตามข้อตกลงที่จะไม่ถูกบังคับใช้ </span><span class="sxs-lookup"><span data-stu-id="a98d6-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="a98d6-131">หากคุณเสนอราคาและส่วนลดที่ขึ้นอยู่กับหลายตัวแบ่งปริมาณ แล้วระบุแต่ละวงเล็บของปริมาณเป็นคู่ของปริมาณต่ำสุดและสูงสุดในฟิลด์ 'เริ่มต้น' และ 'สิ้นสุด' ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="a98d6-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="a98d6-132">ในจำนวนในฟิลด์สกุลเงิน ป้อนราคา</span><span class="sxs-lookup"><span data-stu-id="a98d6-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="a98d6-133">ในฟิลด์วันเริ่มต้น ป้อนวันเริ่มต้นซึ่งข้อตกลงนี้จะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="a98d6-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="a98d6-134">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="a98d6-134">Click Save.</span></span>
18. <span data-ttu-id="a98d6-135">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a98d6-135">Click Validate.</span></span>
19. <span data-ttu-id="a98d6-136">คลิกตรวจสอบความถูกต้องรายการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a98d6-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="a98d6-137">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a98d6-137">Click OK.</span></span>
21. <span data-ttu-id="a98d6-138">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="a98d6-138">Click Post.</span></span>
22. <span data-ttu-id="a98d6-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a98d6-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="a98d6-140">ดูข้อตกลงทางการค้าที่สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a98d6-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="a98d6-141">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="a98d6-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a98d6-142">ในรายการ ค้นหาและเลือกผลิตภัณฑ์ที่คุณอัพเดตราคา</span><span class="sxs-lookup"><span data-stu-id="a98d6-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="a98d6-143">ในบานหน้าต่างการดำเนินการ คลิกขาย</span><span class="sxs-lookup"><span data-stu-id="a98d6-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="a98d6-144">คลิกดูข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="a98d6-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="a98d6-145">ตรวจทานรายละเอียดของราคาที่ตกลงทางการค้าที่คุณเพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="a98d6-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="a98d6-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a98d6-146">Close the page.</span></span>


