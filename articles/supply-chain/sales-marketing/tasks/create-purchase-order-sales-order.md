---
title: การสร้างใบสั่งซื้อจากใบสั่งขาย
description: 'กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อที่ขึ้นอยู่กับใบสั่งขาย '
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d7ce50532fb5bd6723b783d96d756085142e10
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843396"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="7e5b2-103">การสร้างใบสั่งซื้อจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7e5b2-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7e5b2-104">กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อที่ขึ้นอยู่กับใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="7e5b2-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="7e5b2-105">ปริมาณของผลิตภัณฑ์ในใบสั่งซื้อได้ถูกกำหนดไว้แล้วเพื่อตอบสนองความต้องการของใบสั่งขายเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="7e5b2-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="7e5b2-106">การดำเนินการตามความต้องการขายด้วยวิธีนี้เป็นทางเลือกหนึ่งเพื่อความครอบคลุมและการทำงานได้เต็มประสิทธิภาพของการกระจายการวางแผนความต้องการ </span><span class="sxs-lookup"><span data-stu-id="7e5b2-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="7e5b2-107">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="7e5b2-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="7e5b2-108">การสร้างใบสั่งซื้อจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7e5b2-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="7e5b2-109">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7e5b2-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="7e5b2-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7e5b2-110">Click New.</span></span>
3. <span data-ttu-id="7e5b2-111">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7e5b2-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7e5b2-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7e5b2-113">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7e5b2-113">Click OK.</span></span>
6. <span data-ttu-id="7e5b2-114">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7e5b2-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7e5b2-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7e5b2-116">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก D0001 ได้</span><span class="sxs-lookup"><span data-stu-id="7e5b2-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="7e5b2-117">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7e5b2-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="7e5b2-118">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-118">Click Add line.</span></span>
10. <span data-ttu-id="7e5b2-119">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7e5b2-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7e5b2-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7e5b2-121">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก T0020 ได้</span><span class="sxs-lookup"><span data-stu-id="7e5b2-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="7e5b2-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7e5b2-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="7e5b2-123">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7e5b2-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="7e5b2-124">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="7e5b2-124">Click Save.</span></span>
15. <span data-ttu-id="7e5b2-125">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7e5b2-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="7e5b2-126">คลิกใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-126">Click Purchase order.</span></span>
    * <span data-ttu-id="7e5b2-127">หน้าการสร้างใบสั่งซื้อแสดงรายการใบสั่งขายที่เปิดค้างไว้ทั้งหมดตามที่ได้คัดลอกมาจากใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="7e5b2-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="7e5b2-128">คุณสามารถทบทวนรายละเอียดใบสั่งได้ และถ้าจำเป็น คุณสามารถปรับเปลี่ยนรายละเอียดได้เช่น ปริมาณการซื้อและเงื่อนไขการกำหนดราคา ก่อนที่คุณจะสร้างการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="7e5b2-129">เลือกตัวเลือกการรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7e5b2-129">Select the Include all option.</span></span>
    * <span data-ttu-id="7e5b2-130">ถ้าคุณต้องการสร้างใบสั่งซื้อสำหรับเฉพาะชุดย่อยของรายการใบสั่งขาย ให้เลือกรายการเหล่านี้ทีละรายการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="7e5b2-131">ฟิลด์บัญชีผู้จัดจำหน่ายอาจหรืออาจจะไม่ได้ถูกเติมด้วยหมายเลขผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="7e5b2-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="7e5b2-132">ถ้าผู้จัดจำหน่ายเริ่มต้นได้มีการตั้งค่าไว้สำหรับผลิตภัณฑ์ (ในความครอบคลุมสินค้าที่เกี่ยวข้อง) แล้วผู้จัดจำหน่ายนี้จะถูกคัดลอกไปยังรายการ </span><span class="sxs-lookup"><span data-stu-id="7e5b2-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="7e5b2-133">มิฉะนั้น คุณต้องป้อนผู้จัดจำหน่ายด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="7e5b2-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="7e5b2-134">ในคู่มือนี้ ไม่สนใจว่าฟิลด์บัญชีผู้จัดจำหน่ายมีค่าบรรจุอยู่แล้วหรือไม่  ขั้นตอนต่อไปนี้จะให้คุณเลือกผู้จัดจำหน่ายใหม่ซึ่งแตกต่างกันในแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="7e5b2-135">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7e5b2-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="7e5b2-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="7e5b2-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7e5b2-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="7e5b2-138">เลือกรายการใบสั่งที่สอง</span><span class="sxs-lookup"><span data-stu-id="7e5b2-138">Select the second order line.</span></span>
22. <span data-ttu-id="7e5b2-139">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7e5b2-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="7e5b2-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="7e5b2-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7e5b2-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="7e5b2-142">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7e5b2-142">Click Validate.</span></span>
26. <span data-ttu-id="7e5b2-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7e5b2-143">Click OK.</span></span>
    * <span data-ttu-id="7e5b2-144">ข้อความจะแจ้งให้คุณทราบว่ามีการสร้างใบสั่งซื้อหนึ่งรายการหรือมากกว่า </span><span class="sxs-lookup"><span data-stu-id="7e5b2-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="7e5b2-145">ระบบจะสร้างใบสั่งซื้อแยกต่างหากสำหรับแต่ละผู้จัดจำหน่ายที่คุณระบุไว้สำหรับรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7e5b2-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="7e5b2-146">ซึ่งหมายความว่า ถ้ามีรายการใบสั่งขายหลายรายการการจัดส่งถูกจัดส่งโดยผู้จัดจำหน่ายเดียวกัน ใบสั่งซื้อใบเดียวที่มีหลายรายการจะถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="7e5b2-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="7e5b2-147">ตรวทานใบสั่งซื้อที่มีการสร้างขึ้นจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7e5b2-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="7e5b2-148">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="7e5b2-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="7e5b2-149">คลิกใบสั่งที่เกี่ยวข้องกับ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-149">Click Related orders.</span></span>
    * <span data-ttu-id="7e5b2-150">หน้าใบสั่งที่เกี่ยวข้องแสดงรายการทั้งหมดที่สร้างขึ้นจากใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="7e5b2-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="7e5b2-151">ในตัวอย่างนี้ มีใบสั่งซื้อสองรายการถูกสร้างขึ้นสำหรับสองผู้จัดจำหน่ายที่แตกต่างกันตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="7e5b2-152">คลิกเพื่อติดตามลิงค์ในฟิลด์ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="7e5b2-153">รายการใบสั่งซื้อแต่ละรายการจะสัมพันธ์กับรายการใบสั่งขายที่นำไปสู่การซื้อ </span><span class="sxs-lookup"><span data-stu-id="7e5b2-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="7e5b2-154">ความสัมพันธ์กับใบสั่งขายมีการระบุไว้บนแท็บผลิตภัณฑ์ในแท็บด่วนรายละเอียดรายการ ในฟิลด์ชนิดการอ้างอิง หมายเลขอ้างอิง และการอ้างอิงล็อต</span><span class="sxs-lookup"><span data-stu-id="7e5b2-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="7e5b2-155">ขยายหรือยุบส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="7e5b2-156">คลิกแท็บผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7e5b2-156">Click the Product tab.</span></span>
    * <span data-ttu-id="7e5b2-157">ล็อตอ้างอิงยืนช่วยให้มั่นใจว่าจะมีการคิดต้นทุนจากการซื้อปัจจุบันกับใบสั่งขายที่แนบ</span><span class="sxs-lookup"><span data-stu-id="7e5b2-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="7e5b2-158">คุณสามารถไปที่ใบสั่งขายเริ่มต้น โดยการเปิดลิงค์ในฟิลด์หมายเลขอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="7e5b2-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

