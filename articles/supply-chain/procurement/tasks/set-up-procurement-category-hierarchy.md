--- 
title: "ตั้งค่าประเภทการจัดซื้อตามลำดับชั้น"
description: "ขั้นตอนนี้แสดงวิธีการสร้างโหนดใหม่ในลำดับชั้นประเภทการจัดซื้อและวิธีการตั้งค่าประเภทการจัดซื้อที่จะใช้ในกระบวนการจัดซื้อ "
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 767fbe69eb918b6e37842ad1c393d08d11346e71
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="7f5ae-103">ตั้งค่าประเภทการจัดซื้อตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="7f5ae-103">Set up a procurement category hierarchy</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f5ae-104">ขั้นตอนนี้แสดงวิธีการสร้างโหนดใหม่ในลำดับชั้นประเภทการจัดซื้อและวิธีการตั้งค่าประเภทการจัดซื้อที่จะใช้ในกระบวนการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="7f5ae-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="7f5ae-105">โดยทั่วไป งานเหล่านี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="7f5ae-106">ก่อนที่คุณจะสามารถเริ่มขั้นตอนนี้ ต้องมีประเภทตามลำดับชั้นของชนิดการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="7f5ae-107">ถ้าคุณกำลังใช้ข้อมูลบริษัทสาธิต คุณสามารถเรียกใช้ขั้นตอนนี้ในบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="7f5ae-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="7f5ae-108">เพิ่มประเภทการจัดซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="7f5ae-108">Add a new procurement category</span></span>
1. <span data-ttu-id="7f5ae-109">ไปที่การจัดซื้อและการจัดหา > ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="7f5ae-110">คลิกแก้ไขลำดับชั้นของประเภท</span><span class="sxs-lookup"><span data-stu-id="7f5ae-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="7f5ae-111">ลำดับชั้นประเภทการจัดซื้อปัจจุบันจะแสดงอยู่ทางด้านซ้ายของหน้า </span><span class="sxs-lookup"><span data-stu-id="7f5ae-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="7f5ae-112">คุณกำลังจะปรับเปลี่ยนลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="7f5ae-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="7f5ae-113">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="7f5ae-113">Click New category node.</span></span>
    * <span data-ttu-id="7f5ae-114">ระบบจะเลือกโหนดบนสุดตามค่าเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="7f5ae-114">The system selects the top node by default.</span></span> <span data-ttu-id="7f5ae-115">ถ้าคุณกำลังรันขั้นตอนนี้เป็นคู่มืองาน คุณสามารถคลิกปุ่มปลดล็อค และเลือกโหนดหลักอื่นเพื่อแทรกโหนดของคุณใหม่ลงไป</span><span class="sxs-lookup"><span data-stu-id="7f5ae-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="7f5ae-116">หลังจากที่เสร็จเรียบร้อย ล็อคคู่มืองานอีกครั้ง จากนั้นคลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="7f5ae-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="7f5ae-117">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="7f5ae-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7f5ae-118">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7f5ae-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="7f5ae-119">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7f5ae-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="7f5ae-120">ชื่อที่จำง่ายไม่จำเป็น </span><span class="sxs-lookup"><span data-stu-id="7f5ae-120">The friendly name is optional.</span></span> <span data-ttu-id="7f5ae-121">มันจะปรากฏในประเภทการค้นหาพร้อมด้วยชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="7f5ae-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="7f5ae-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7f5ae-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="7f5ae-123">เพิ่มผลิตภัณฑ์ไปยังประเภทการจัดซื้อใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="7f5ae-124">ไปที่การจัดซื้อและการจัดหา > ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="7f5ae-125">เลือกโหนดคุณเพิ่งเพิ่มเข้ามา </span><span class="sxs-lookup"><span data-stu-id="7f5ae-125">Select the node you just added.</span></span> <span data-ttu-id="7f5ae-126">ถ้าคุณกำลังใช้งานขั้นตอนนี้เป็นคู่มืองานคุณอาจต้องการปลดล็อคคู่มืองานเพื่อเลือกโหนด</span><span class="sxs-lookup"><span data-stu-id="7f5ae-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="7f5ae-127">เปิด/ปิดการขยายส่วนผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="7f5ae-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="7f5ae-128">คลิกเพิ่มเพื่อเชื่อมโยงผลิตภัณฑ์กับประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="7f5ae-129">เลือกผลิตภัณฑ์ที่คุณต้องการเพิ่มในประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="7f5ae-130">คลิกลูกศรเพื่อเลือกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7f5ae-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="7f5ae-131">เลือกผลิตภัณฑ์อื่นเพื่อเพิ่มในประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="7f5ae-132">คลิกลูกศรเพื่อเลือกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7f5ae-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="7f5ae-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7f5ae-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="7f5ae-134">เพิ่มผู้จัดจำหน่ายที่ได้รับอนุมัติและที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="7f5ae-135">สลับการขยายของส่วนผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7f5ae-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="7f5ae-136">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="7f5ae-136">Click Add.</span></span>
    * <span data-ttu-id="7f5ae-137">คุณสามารถเพิ่มผู้จัดจำหน่ายให้กับประเภทการจัดซื้อ และระบุว่าผู้จัดจำหน่ายเป็นที่ต้องการหรือเพิ่งได้รับอนุมัติในประเภทนั้น</span><span class="sxs-lookup"><span data-stu-id="7f5ae-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="7f5ae-138">เมื่อคุณลบผู้จัดจำหน่ายจากประเภท ธุรกรรมกับผู้จัดจำหน่ายในอดีตในประเภทนี้จะไม่ถูกลบ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="7f5ae-139">ค้นหาผู้จัดจำหน่ายที่คุณต้องการเพิ่มในประเภท</span><span class="sxs-lookup"><span data-stu-id="7f5ae-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="7f5ae-140">คลิกลูกศรเพื่อเลือกผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7f5ae-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="7f5ae-141">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7f5ae-141">Click OK.</span></span>
6. <span data-ttu-id="7f5ae-142">เลือกแถวผู้จัดจำหน่ายที่คุณต้องการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="7f5ae-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="7f5ae-143">ในฟิลด์สถานะผู้จัดจำหน่าย ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="7f5ae-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="7f5ae-144">การตั้งค่าการเลือกผู้จัดจำหน่ายในกฎนโยบายประเภทควบคุมว่า ไม่ว่าผู้จัดจำหน่ายจะเป็นที่ต้องการ ได้รับอนุมัติ หรือผู้จัดจำหน่ายทั้งหมด จะพร้อมใช้งานกับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="7f5ae-145">เพิ่มข้อมูลเพิ่มเติมไปยังประเภท</span><span class="sxs-lookup"><span data-stu-id="7f5ae-145">Add additional information to the category</span></span>
1. <span data-ttu-id="7f5ae-146">เปิด/ปิดการขยายของส่วนกลุ่มเกณฑ์การประเมินผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7f5ae-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="7f5ae-147">แท็บนี้ช่วยให้คุณสามารถกำหนดว่าเงื่อนไขผู้จัดจำหน่ายในประเภทการจัดซื้อใด ควรจะถูกจัดอันดับ </span><span class="sxs-lookup"><span data-stu-id="7f5ae-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="7f5ae-148">การจะทำเช่นนี้ คุณจะคลิกเพิ่ม จากนั้นเลือกกลุ่มการประเมินผู้จัดจำหน่ายที่ประกอบด้วยเงื่อนไขคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="7f5ae-149">เปิด/ปิดการขยายส่วนแบบสอบถาม </span><span class="sxs-lookup"><span data-stu-id="7f5ae-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="7f5ae-150">แท็บนี้ช่วยให้คุณสามารถเพิ่มแบบสอบถามที่จะปรากฏบนใบสั่ง ตราบใดที่คุณตั้งค่าชนิดของกิจกรรมเป็น "ขอ" </span><span class="sxs-lookup"><span data-stu-id="7f5ae-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="7f5ae-151">ผู้ขอต้องกรอกแบบสอบถามก่อนที่จะส่งใบขอซื้อสำหรับผลิตภัณฑ์เฉพาะหรือผลิตภัณฑ์ในประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="7f5ae-152">เปิด/ปิดการขยายของส่วนกลุ่มภาษีขายตามประเภทสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f5ae-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="7f5ae-153">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า: ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7f5ae-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7f5ae-154">เลือกกลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="7f5ae-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="7f5ae-155">เปิด/ปิดการขยายส่วนหน้าประเภท</span><span class="sxs-lookup"><span data-stu-id="7f5ae-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="7f5ae-156">หน้าประเภทถูกสร้างในหน้าลำดับชั้นของประเภท </span><span class="sxs-lookup"><span data-stu-id="7f5ae-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="7f5ae-157">โดยประกอบด้วยข้อมูลเกี่ยวกับประเภทการจัดซื้อ เช่น ข้อมูลเกี่ยวกับชนิดของผลิตภัณฑ์ในประเภท รูปภาพของผลิตภัณฑ์ในประเภท หรือประกาศเช่นส่วนลดที่มีอยู่ในประเภทนั้น</span><span class="sxs-lookup"><span data-stu-id="7f5ae-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="7f5ae-158">ข้อมูลในหน้าประเภทถูกแสดงบนใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="7f5ae-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="7f5ae-159">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f5ae-159">Close the page.</span></span>


