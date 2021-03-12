---
title: สร้างผลิตภัณฑ์นำออกใช้สำหรับบริษัทเดียว
description: 'ขั้นตอนนี้แนะนำวิธีการสร้างผลิตภัณฑ์เดี่ยวที่นำออกใช้ในบริบทของหน่วยกฎหมายเดี่ยว '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79d5252d950cd83dfd1307ffb661948405102593
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999692"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="088ed-103">สร้างผลิตภัณฑ์นำออกใช้สำหรับบริษัทเดียว</span><span class="sxs-lookup"><span data-stu-id="088ed-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="088ed-104">ขั้นตอนนี้แนะนำวิธีการสร้างผลิตภัณฑ์เดี่ยวที่นำออกใช้ในบริบทของหน่วยกฎหมายเดี่ยว </span><span class="sxs-lookup"><span data-stu-id="088ed-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="088ed-105">หลังจากที่มีการสร้างผลิตภัณฑ์นำออกใช้ซึ่ง จะพร้อมใช้งานทันทีในหน่วยนี้เท่านั้น </span><span class="sxs-lookup"><span data-stu-id="088ed-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="088ed-106">คุณสามารถแนะนำขั้นตอนนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="088ed-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="088ed-107">โดยปกติผู้ออกแบบผลิตภัณฑ์จะเป็นผู้ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="088ed-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="088ed-108">สร้างผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="088ed-108">Create a released product</span></span>
1. <span data-ttu-id="088ed-109">ไปที่ผลิตภัณฑ์ที่จะนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="088ed-109">Go to Released products.</span></span>
2. <span data-ttu-id="088ed-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="088ed-110">Click New.</span></span>
3. <span data-ttu-id="088ed-111">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="088ed-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="088ed-112">ถ้าไม่มีการป้อนหมายเลขผลิตภัณฑ์โดยอัตโนมัติในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์หมายเลขผลิตภัณฑ์เฉพาะ </span><span class="sxs-lookup"><span data-stu-id="088ed-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="088ed-113">จะใช้ขั้นตอนนี้ในกรณีที่ไม่มีการตั้งค่าลำดับหมายเลขสำหรับหมายเลขผลิตภัณฑ์ไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="088ed-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="088ed-114">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="088ed-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="088ed-115">ชื่อผลิตภัณฑ์ถูกตั้งค่าเริ่มต้นเป็นชื่อการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="088ed-116">ถ้าจำเป็น คุณสามารถเลือกที่จะเปลี่ยนชื่อการค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="088ed-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="088ed-117">ในฟิลด์กลุ่มแบบจำลองสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-118">กลุ่มแบบจำลองสินค้าประกอบด้วย การตั้งค่าที่กำหนดวิธีการควบคุมและจัดการสินค้าในการรับสินค้าและการนำสินค้าออกใช้ </span><span class="sxs-lookup"><span data-stu-id="088ed-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="088ed-119">นอกจากนี้การตั้งค่ายังกำหนดวิธีการคำนวณปริมาณการใช้สินค้าอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="088ed-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="088ed-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="088ed-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="088ed-122">ในฟิลด์กลุ่มสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-123">กลุ่มสินค้าใช้สำหรับการจัดการสินค้าคงคลังโดยการแบ่งสินค้าคงคลังออกเป็นกลุ่มตามลักษณะของสินค้า </span><span class="sxs-lookup"><span data-stu-id="088ed-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="088ed-124">ตัวอย่างเช่น เพื่อจัดการวิธีการโพสต์ข้อมูลไปยังบัญชีหลัก คุณสามารถสร้างชุดของกลุ่มสินค้าที่แตกต่างกันซึ่งถูกเชื่อมโยงกับบัญชีหลักเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="088ed-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="088ed-125">นี่จะทำให้คุณสามารถติดตามค่าสินค้าคงคลังของสินค้าที่สถานะต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="088ed-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="088ed-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="088ed-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="088ed-128">ในฟิลด์กลุ่มมิติการจัดเก็บ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-129">มิติการจัดเก็บช่วยให้คุณสามารถควบคุมวิธีการจัดเก็บสินค้า และนำสินค้าออกจากคลัง </span><span class="sxs-lookup"><span data-stu-id="088ed-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="088ed-130">ตัวอย่างเช่น มิติการจัดเก็บสามารถเป็นไซต์หรือโกดังได้</span><span class="sxs-lookup"><span data-stu-id="088ed-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="088ed-131">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="088ed-132">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="088ed-133">ในฟิลก์กลุ่มมิติการติดตาม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-134">กลุ่มมิติการติดตามกำหนดว่ามิติการติดตามใดที่คุณสามารถเพิ่มลงในผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="088ed-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="088ed-135">ตัวอย่างเช่น หมายเลขชุดงานและหมายเลขประจำสินค้าสามารถใช้เพื่อติดตามสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="088ed-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="088ed-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="088ed-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="088ed-138">ในฟิลด์หน่วยสินค้าคงคลัง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-139">หน่วยสินค้าคงคลังกำหนดวิธีแสดงจำนวนผลิตภัณฑ์เมื่อมีการจัดเก็บในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="088ed-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="088ed-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="088ed-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="088ed-142">ในฟิลด์หน่วยการซื้อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="088ed-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-143">หน่วยการซื้อกำหนดวิธีที่ผลิตภัณฑ์ถูกแสดงปริมาณ เมื่อมีการซื้อจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="088ed-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="088ed-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="088ed-145">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="088ed-146">ในฟิลด์หน่วยการขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="088ed-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-147">หน่วยการขายกำหนดวิธีที่ผลิตภัณฑ์ถูกแสดงปริมาณ เมื่อมีการขายให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="088ed-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="088ed-148">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="088ed-149">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="088ed-150">ในฟิลด์หน่วย BOM ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-151">หน่วย BOM กำหนดวิธีแสดงจำนวนผลิตภัณฑ์เมื่อรวมอยู่ในสูตรการผลิต (BOM) </span><span class="sxs-lookup"><span data-stu-id="088ed-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="088ed-152">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="088ed-153">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="088ed-154">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-155">กลุ่มภาษีขายสินค้าในกลุ่มภาษีขายกำหนดวิธีคำนวณภาษีขายสำหรับแต่ละผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="088ed-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="088ed-156">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="088ed-157">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="088ed-158">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="088ed-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="088ed-159">กลุ่มภาษีขายสินค้าในกลุ่มภาษีซื้อกำหนดวิธีคำนวณภาษีซื้อสำหรับแต่ละผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="088ed-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="088ed-160">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="088ed-161">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="088ed-162">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="088ed-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="088ed-163">เพิ่มลักษณะของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="088ed-163">Add product characteristics</span></span>
1. <span data-ttu-id="088ed-164">ขยายหรือยุบส่วนจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="088ed-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="088ed-165">ในฟิลด์น้ำหนักสุทธิ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="088ed-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="088ed-166">ในฟิลด์น้ำหนักหีบห่อ ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="088ed-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="088ed-167"> - ในฟิลด์ความลึกรวม ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="088ed-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="088ed-168"> - ในฟิลด์ความกว้างรวม ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="088ed-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="088ed-169">ในฟิลด์ความสูงรวม ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="088ed-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="088ed-170">ในฟิลด์จำนวน ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="088ed-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="088ed-171">เพิ่มมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="088ed-171">Add financial dimensions</span></span>
1. <span data-ttu-id="088ed-172">ขยายหรือยุบส่วนของการเพิ่มมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="088ed-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="088ed-173">ในฟิลด์หน่วยธุรกิจ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="088ed-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="088ed-174">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="088ed-175">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="088ed-176">ในฟิลด์ต้นทุนศูนย์กลาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="088ed-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="088ed-177">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="088ed-178">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="088ed-179">ในฟิลด์แผนก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="088ed-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="088ed-180">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="088ed-181">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="088ed-182">ในฟิลด์กลุ่มสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="088ed-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="088ed-183">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="088ed-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="088ed-184">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088ed-184">In the list, click the link in the selected row.</span></span>

