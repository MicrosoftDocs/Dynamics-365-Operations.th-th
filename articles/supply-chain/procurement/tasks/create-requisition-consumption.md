--- 
title: "สร้างใบขอซื้อเพื่อปริมาณการใช้"
description: "ขั้นตอนนี้นำคุณไปสู่กระบวนการของการสร้างใบขอซื้อ"
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07fe007005fcbbac1beecadb14dbd752376a0bd4
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="cc13d-103">สร้างใบขอซื้อเพื่อปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="cc13d-103">Create a requisition for consumption</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc13d-104">ขั้นตอนนี้นำคุณไปสู่กระบวนการของการสร้างใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="cc13d-105">ซึ่งจะแสดงวิธีต่างๆในการค้นหาผลิตภัณฑ์ในแค็ตตาล็อกการจัดซื้อและวิธีการเพิ่มผลิตภัณฑ์ที่ไม่ได้อยู่ในแค็ตตาล็อกของคุณ</span><span class="sxs-lookup"><span data-stu-id="cc13d-105">It shows you different ways to search for products in your procurement catalogue and how to add a product that isn’t in your catalogue.</span></span> <span data-ttu-id="cc13d-106">ก่อนที่คุณเริ่มกระบวนงานนี้คุณจะต้องมีนโยบายการจัดซื้อที่ตั้งค่าด้วยปริมาณการใช้เป็นชนิดเริ่มต้นของใบขอซื้อ </span><span class="sxs-lookup"><span data-stu-id="cc13d-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="cc13d-107">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="cc13d-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="cc13d-108">กระบวนงานสามารถถูกดำเนินการได้โดยโปรไฟล์ผู้ใช้ที่ถูกตั้งค่าเป็นผู้ปฏิบัติงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cc13d-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="cc13d-109">ตามปกติแล้วงานนี้จะถูกดำเนินการโดยพนักงาน</span><span class="sxs-lookup"><span data-stu-id="cc13d-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="cc13d-110">พนักงานรักษาบทบาทความปลอดภัยจะอนุญาตให้คุณดำเนินงาน หรือถ้าคุณกำลังใช้ USMF คุณสามารถเข้าสู่ระบบในฐานะ Alicia</span><span class="sxs-lookup"><span data-stu-id="cc13d-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="cc13d-111">สร้างใบเบิกค่าเดินทางใหม่</span><span class="sxs-lookup"><span data-stu-id="cc13d-111">Create a new requisition</span></span>
1. <span data-ttu-id="cc13d-112">ไปที่การจัดซื้อและการจัดหา > ใบขอซื้อ > ใบขอซื้อที่ฉันจัดเตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="cc13d-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="cc13d-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="cc13d-113">Click New.</span></span>
3. <span data-ttu-id="cc13d-114">ในฟิลด์ชื่อ ให้ใส่ชื่อใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="cc13d-115">ในฟิลด์วันที่ร้องขอ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cc13d-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="cc13d-116">โดยค่าเริ่มต้น วันที่ร้องขอและวันที่ลงบัญชีจะถูกคัดลอกไปยังรายการใบขอซื้อ </span><span class="sxs-lookup"><span data-stu-id="cc13d-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="cc13d-117">สามารถถูกเปลี่ยนแปลงได้ที่ระดับรายการ </span><span class="sxs-lookup"><span data-stu-id="cc13d-117">They can be changed at the line level.</span></span> <span data-ttu-id="cc13d-118">วันร้องขอนั้นเป็นวันที่จัดส่งที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="cc13d-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="cc13d-119">ในฟิลด์วันที่ลงบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cc13d-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="cc13d-120">วันลงบัญชีจะใช้ เพื่อบันทึกรายการบัญชีในบัญชีแยกประเภททั่วไป และตรวจสอบว่ามีเงินทุนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="cc13d-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="cc13d-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cc13d-121">Click OK.</span></span>
7. <span data-ttu-id="cc13d-122">ในฟิลด์เหตุผล ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="cc13d-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cc13d-123">โดยค่าเริ่มต้นเหตุผลทางธุรกิจที่คุณเลือกนั้นจะปรากฏขึ้นสำหรับรายการใบขอซื้อแต่คุณสามารถเปลี่ยนได้ที่ระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="cc13d-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="cc13d-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="cc13d-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="cc13d-125">เลือกเหตุผล</span><span class="sxs-lookup"><span data-stu-id="cc13d-125">Select the reason</span></span>
10. <span data-ttu-id="cc13d-126">ในฟิลด์รายละเอียดให้ป้อนคำอธิบายเหตุผลสำหรับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="cc13d-127">เพิ่มรายการในใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="cc13d-128">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="cc13d-128">Click Add line.</span></span>
    * <span data-ttu-id="cc13d-129">มีสองวิธีในการเพิ่มรายการใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="cc13d-130">ถ้าคุณทราบหมายเลขผลิตภัณฑ์แล้วหรือคุณทราบแล้วว่าคุณกำลังร้องขอผลิตภัณฑ์ที่ไม่ได้อยู่ในแค็ตตาล็อกผลิตภัณฑ์ จากนั้นคุณสามารถเพิ่มรายการได้โดยตรงด้วย "เพิ่มรายการ"</span><span class="sxs-lookup"><span data-stu-id="cc13d-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalogueue, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="cc13d-131">ส่วนอีกวิธีคือการใช้ "เพิ่มผลิตภัณฑ์" ที่คุณสามารถใช้ในการค้นหาและการกรองข้อมูลเพื่อค้นหารายการในแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cc13d-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalogueue.</span></span>    
2. <span data-ttu-id="cc13d-132">คลิกแถวที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="cc13d-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="cc13d-133">ผู้ขอคือผู้ปฏิบัติงานที่ได้ทำการขอใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="cc13d-134">โดยค่าเริ่มต้น บุคคลที่จัดเตรียมใบขอซื้อคือผู้ปฏิบัติงานที่ร้องขอได้ </span><span class="sxs-lookup"><span data-stu-id="cc13d-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="cc13d-135">คุณจำเป็นต้องได้รับสิทธิ์ในการจัดเตรียมรายการใบขอซื้อในนามของผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="cc13d-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="cc13d-136">ถ้าคุณมีสิทธิ์ดังกล่าวแล้วผู้ปฏิบัติงานอื่น ๆ จะแสดงในการค้นหานี้</span><span class="sxs-lookup"><span data-stu-id="cc13d-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="cc13d-137">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cc13d-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="cc13d-138">สินค้าที่พร้อมใช้งานสำหรับคุณเพือเลือกจะถูกจำกัดโดยนโยบายการเข้าถึงประเภทและแค็ตตาล็อกการจัดซื้อสำหรับนิติบุคคลที่จัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-138">The items that are available for you to choose are limited by the category access policy and the procurement catalogue for the buying legal entity.</span></span>   
4. <span data-ttu-id="cc13d-139">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="cc13d-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="cc13d-140">เพิ่มผลิตภัณฑ์เพิ่มเติมลงในใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="cc13d-141">คลิกเพิ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cc13d-141">Click Add products.</span></span>
    * <span data-ttu-id="cc13d-142">นี่เป็นตัวเลือกที่คุณสามารถค้นหาผลิตภัณฑ์ในแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cc13d-142">This is the option where you can search for products in the product catalogueue.</span></span>    
2. <span data-ttu-id="cc13d-143">ในฟิลด์ค้นหาโหนดประเภทการจัดซื้อ พิมพ์ส่วนแรกของชื่อของประเภทที่คุณกำลังค้นหา และจากนั้น คลิกป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc13d-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="cc13d-144">ตัวอย่างเช่น ชนิดคอมพิวเตอร์</span><span class="sxs-lookup"><span data-stu-id="cc13d-144">For example, type comput.</span></span>  
3. <span data-ttu-id="cc13d-145">ใช้ทางลัด InvokeDefaultButton </span><span class="sxs-lookup"><span data-stu-id="cc13d-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="cc13d-146">ใช้ตัวกรองในการกรองรายการผลิตภัณฑ์ในประเภทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cc13d-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="cc13d-147">เลือกบัตรผลิตภัณฑ์ที่คุณต้องการเพิ่มในใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="cc13d-148">คลิกเพิ่มลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="cc13d-148">Click Add to lines.</span></span>
7. <span data-ttu-id="cc13d-149">ในฟิลด์ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="cc13d-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="cc13d-150">ในฟิลด์ค้นหาโหนดประเภทการจัดซื้อ พิมพ์ส่วนแรกของชื่อของประเภทที่คุณกำลังค้นหา และจากนั้น คลิกป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc13d-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="cc13d-151">ตัวอย่างเช่น ชนิดสูง (ปากกาเน้นข้อความ)</span><span class="sxs-lookup"><span data-stu-id="cc13d-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="cc13d-152">ใช้ทางลัด InvokeDefaultButton </span><span class="sxs-lookup"><span data-stu-id="cc13d-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="cc13d-153">คลิกเพิ่มผลิตภัณฑ์ที่ไม่อยู่ในรายการลงในรายการเพื่อเพิ่มผลิตภัณฑ์ที่ไม่แสดงในแค็ตตาล็อกการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalogue.</span></span>
11. <span data-ttu-id="cc13d-154">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cc13d-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="cc13d-155">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="cc13d-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="cc13d-156">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="cc13d-156">Click OK.</span></span>
14. <span data-ttu-id="cc13d-157">ในฟิลด์คำอธิบายสินค้า ให้เพิ่มคำอธิบายของสินค้า</span><span class="sxs-lookup"><span data-stu-id="cc13d-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="cc13d-158">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="cc13d-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="cc13d-159">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="cc13d-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="cc13d-160">ถ้าคุณทราบราคาสำหรับผู้จัดจำหน่ายรายใดรายหนึ่ง (ที่คุณเลือกในฟิลด์บัญชีผู้จัดจำหน่าย) จากนั้นคุณสามารถป้อนราคานั้น</span><span class="sxs-lookup"><span data-stu-id="cc13d-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="cc13d-161">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="cc13d-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cc13d-162">ผู้จัดจำหน่ายที่จะพร้อมใช้งานในฟิลด์นี้ ขึ้นอยู่กับนโยบายการจัดซื้อและสถานะที่ผู้จัดจำหน่ายมีสำหรับประเภทการจัดซื้อปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="cc13d-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="cc13d-163">ตามทางเลือกหนึ่งในการเลือกผู้จัดจำหน่ายที่นี่ คุณสามารถคลิกปุ่มแนะนำผู้จัดจำหน่ายได้</span><span class="sxs-lookup"><span data-stu-id="cc13d-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="cc13d-164">ในรายการ ให้เลือกผู้จัดจำหน่ายที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="cc13d-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="cc13d-165">ในฟิลด์หมายเลขสินค้าภายนอก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cc13d-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="cc13d-166">นี่คือหมายเลขอ้างอิงสำหรับผลิตภัณฑ์ที่เป็นที่รู้จักโดยผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="cc13d-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="cc13d-167">ตัวอย่างเช่น นี่อาจเป็นหมายเลขสินค้าของผลิตภัณฑ์ในแค็ตตาล็อกของผู้จัดจำหน่ายเอง</span><span class="sxs-lookup"><span data-stu-id="cc13d-167">For example, this could be the item number of the product in the vendor's own catalogue.</span></span>  
20. <span data-ttu-id="cc13d-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cc13d-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="cc13d-169">กระจายยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="cc13d-169">Distribute amounts</span></span>
1. <span data-ttu-id="cc13d-170">คลิกข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="cc13d-170">Click Financials.</span></span>
2. <span data-ttu-id="cc13d-171">คลิกกระจายยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="cc13d-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="cc13d-172">กระบวนการนี้แสดงให้คุณเห็นถึงวิธีการกระจายต้นทุนสำหรับรายการแรกระหว่าง 2 บัญชี </span><span class="sxs-lookup"><span data-stu-id="cc13d-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="cc13d-173">นอกจากนี้ยังทำได้ในภายหลังเมื่อใบขอซื้ออยู่ในระหว่างการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="cc13d-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="cc13d-174">คลิกแบ่งเพื่อสร้างรายการการกระจาย</span><span class="sxs-lookup"><span data-stu-id="cc13d-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="cc13d-175">ในฟิลด์บัญชีแยกประเภทเลือกศูนย์ต้นทุนแรกที่ควรเป็นส่วนหนึ่งของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="cc13d-175">In the Ledger account field select the first cost centre that should take part of the cost.</span></span>
5. <span data-ttu-id="cc13d-176">เลือกรายการการกระจายอื่น</span><span class="sxs-lookup"><span data-stu-id="cc13d-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="cc13d-177">ในฟิลด์บัญชีแยกประเภทระบุศูนย์ต้นทุนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="cc13d-177">In the Ledger account field specify the other cost centre.</span></span>
7. <span data-ttu-id="cc13d-178">คลิกกระจายเท่าๆ กัน</span><span class="sxs-lookup"><span data-stu-id="cc13d-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="cc13d-179">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cc13d-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="cc13d-180">ดูรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="cc13d-180">View line details</span></span>
1. <span data-ttu-id="cc13d-181">สลับการขยายของส่วนรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="cc13d-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="cc13d-182">ส่งใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc13d-182">Submit the requisition</span></span>
1. <span data-ttu-id="cc13d-183">คลิกลำดับงานเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cc13d-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="cc13d-184">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="cc13d-184">Click Submit.</span></span>
3. <span data-ttu-id="cc13d-185">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cc13d-185">Close the page.</span></span>
4. <span data-ttu-id="cc13d-186">ในฟิลด์ข้อคิดเห็น พิมพ์หมายเหตุสำหรับผู้อนุมัติใบสั่งขอ</span><span class="sxs-lookup"><span data-stu-id="cc13d-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="cc13d-187">คลิก ส่ง</span><span class="sxs-lookup"><span data-stu-id="cc13d-187">Click Submit.</span></span>
6. <span data-ttu-id="cc13d-188">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cc13d-188">Close the page.</span></span>
7. <span data-ttu-id="cc13d-189">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="cc13d-189">Refresh the page.</span></span>


