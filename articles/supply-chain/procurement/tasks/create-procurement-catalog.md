--- 
title: "สร้างแค็ตตาล็อกการจัดซื้อ"
description: "คำแนะนำนี้แสดงวิธีการสร้างแค็ตตาล็อกการจัดซื้อ "
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2bda068c71b768eb0caadfdbf8b4fe5620bd8eea
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="beaa8-103">สร้างแค็ตตาล็อกการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="beaa8-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="beaa8-104">คำแนะนำนี้แสดงวิธีการสร้างแค็ตตาล็อกการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="beaa8-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="beaa8-105">โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหา </span><span class="sxs-lookup"><span data-stu-id="beaa8-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="beaa8-106">คุณจะทราบว่าพนักงานสามารถใช้แค็ตตาล็อกเมื่อสร้างใบสั่งได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="beaa8-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="beaa8-107">ก่อนที่คุณจะสามารถสร้างแค็ตตาล็อก จะต้องมีประเภทการจัดซื้อตามลำดับชั้นในระบบของคุณก่อน</span><span class="sxs-lookup"><span data-stu-id="beaa8-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="beaa8-108">ลำดับชั้นจะสืบทอดโดยแค็ตตาล็อกใหม่ พร้อมกับผลิตภัณฑ์ทั้งหมดที่อยู่ในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="beaa8-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="beaa8-109">คุณสามารถใช้คำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF ที่ประเภทการจัดซื้อตามลำดับชั้นพร้อมใช้งาน ตลอดจนตัวอย่างที่ใช้ในกระบวนงาน</span><span class="sxs-lookup"><span data-stu-id="beaa8-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="beaa8-110">ตรวจสอบให้แน่ใจว่ามีประเภทการจัดซื้อตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="beaa8-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="beaa8-111">ไปที่การจัดซื้อและการจัดหา > ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="beaa8-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="beaa8-112">ประเภทการจัดซื้อตามลำดับชั้นจะพร้อมใช้งานในบริษัทข้อมูลสาธิต USMF และได้เพิ่มผลิตภัณฑ์ในประเภทเครื่องจักร/คอมพิวเตอร์สำนักงาน </span><span class="sxs-lookup"><span data-stu-id="beaa8-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="beaa8-113">ถ้าคุณกำลังใช้งานกระบวนงานนี้เป็นคู่มืองาน คุณจะต้องปลดล็อคคำแนะนำถ้าคุณต้องการเรียกดูประเภท</span><span class="sxs-lookup"><span data-stu-id="beaa8-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="beaa8-114">ถ้าไม่มีลำดับชั้น คุณจะต้องสร้างขึ้นโดยการคลิกสร้าง </span><span class="sxs-lookup"><span data-stu-id="beaa8-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="beaa8-115">การดำเนินการนี้สามารถทำได้เพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="beaa8-115">This can only be done once.</span></span>  
2. <span data-ttu-id="beaa8-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="beaa8-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="beaa8-117">สร้างแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="beaa8-117">Create a catalog</span></span>
1. <span data-ttu-id="beaa8-118">ไปที่การจัดซื้อและการจัดหา > แค็ตตาล็อก > แค็ตตาล็อกการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="beaa8-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="beaa8-119">คลิกที่แค็ตตาล็อกการจัดซื้อใหม่เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="beaa8-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="beaa8-120">ในฟิลด์ชื่อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="beaa8-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="beaa8-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="beaa8-121">Click OK.</span></span>
5. <span data-ttu-id="beaa8-122">ในแผนภูมิ ขยาย 'ประเภทการจัดซื้อขององค์กร'</span><span class="sxs-lookup"><span data-stu-id="beaa8-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="beaa8-123">ในแผนภูมิ ขยาย 'เครื่องจักรสำนักงาน'</span><span class="sxs-lookup"><span data-stu-id="beaa8-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="beaa8-124">ในแผนภูมิ เลือก 'คอมพิวเตอร์'</span><span class="sxs-lookup"><span data-stu-id="beaa8-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="beaa8-125">ผลิตภัณฑ์จากประเภทการจัดซื้อจะแสดงในรายการ </span><span class="sxs-lookup"><span data-stu-id="beaa8-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="beaa8-126">ถ้าคุณต้องการเพิ่มผลิตภัณฑ์ในประเภทที่คุณต้องการทำเช่นนี้ในหน้าประเภทการจัดซื้อตามลำดับชั้น หรือในหน้ารายละเอียดสินค้า</span><span class="sxs-lookup"><span data-stu-id="beaa8-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="beaa8-127">ชนิดการอัพเดตเริ่มต้นกำหนดว่าผลิตภัณฑ์ใหม่ที่ถูกเพิ่มลงในประเภทการจัดซื้อตามลำดับชั้นจะปรากฏทันทีในแค็ตตาล็อกหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="beaa8-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="beaa8-128">ถ้าชนิดการอัพเดตถูกตั้งค่าเป็นไดนามิก การเปลี่ยนแปลงจะมองเห็นได้ในทันที</span><span class="sxs-lookup"><span data-stu-id="beaa8-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="beaa8-129">ถ้าชนิดการอัพเดตเป็นคงที่ ผลิตภัณฑ์จะสามารถมองเห็นได้เฉพาะสำหรับผู้ที่ใช้แค็ตตาล็อกหลังจากที่แค็ตตาล็อกได้รับการเผยแพร่ใหม่</span><span class="sxs-lookup"><span data-stu-id="beaa8-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="beaa8-130">การดำเนินการเผยแพร่จะพร้อมใช้งานบนบานหน้าต่างการดำเนินการที่อยู่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="beaa8-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="beaa8-131">ถ้าผลิตภัณฑ์ถูกลบออกจากประเภทการจัดซื้อตามลำดับชั้น การเปลี่ยนแปลงจะปรากฏทันที โดยไม่คำนึงถึงค่าในฟิลด์ชนิดการอัพเดตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="beaa8-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="beaa8-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="beaa8-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="beaa8-133">คลิกที่ซ่อน</span><span class="sxs-lookup"><span data-stu-id="beaa8-133">Click Hide.</span></span>
10. <span data-ttu-id="beaa8-134">ในบานหน้าต่างการดำเนินการ คลิกประเภทการนำทาง</span><span class="sxs-lookup"><span data-stu-id="beaa8-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="beaa8-135">คลิกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="beaa8-135">Click Disable.</span></span>
12. <span data-ttu-id="beaa8-136">ในบานหน้าต่างการดำเนินการ คลิกประเภทการนำทาง</span><span class="sxs-lookup"><span data-stu-id="beaa8-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="beaa8-137">คลิกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="beaa8-137">Click Enable.</span></span>
14. <span data-ttu-id="beaa8-138">คลิกเรียกใช้แค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="beaa8-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="beaa8-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="beaa8-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="beaa8-140">กำหนดให้เรียกดูแค็ตตาล็อกได้</span><span class="sxs-lookup"><span data-stu-id="beaa8-140">Make the catalog visible</span></span>
1. <span data-ttu-id="beaa8-141">ไปที่การจัดซื้อและการจัดหา > การตั้งค่า > นโยบาย > นโยบายการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="beaa8-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="beaa8-142">เลือก USMF นโยบายการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="beaa8-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="beaa8-143">คุณต้องเลือกนโยบายการจัดซื้อสำหรับนิติบุคคลที่ผู้ปฏิบัติงานเชื่อมโยงกับโพรไฟล์ผู้ใช้ของคุณได้รับอนุญาตให้สั่งผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="beaa8-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="beaa8-144">ในข้อมูลสาธิต USMF ใช้ที่เป็นผู้ดูแลระบบจะเชื่อมต่อกับผู้ปฏิบัติงานที่ชื่อว่า Julia Funderburk และเธอจะสั่งสินค้าใน USMF ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="beaa8-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="beaa8-145">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="beaa8-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="beaa8-146">เลือกแค็ตตาล็อกที่คุณเพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="beaa8-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="beaa8-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="beaa8-147">Click OK.</span></span>
6. <span data-ttu-id="beaa8-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="beaa8-148">Close the page.</span></span>
7. <span data-ttu-id="beaa8-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="beaa8-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="beaa8-150">ใช้แค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="beaa8-150">Use the catalog</span></span>
1. <span data-ttu-id="beaa8-151">ไปที่การจัดซื้อและการจัดหา > ใบขอซื้อ > ใบขอซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="beaa8-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="beaa8-152">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="beaa8-152">Click New.</span></span>
3. <span data-ttu-id="beaa8-153">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="beaa8-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="beaa8-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="beaa8-154">Click OK.</span></span>
5. <span data-ttu-id="beaa8-155">คลิกเพิ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="beaa8-155">Click Add products.</span></span>
6. <span data-ttu-id="beaa8-156">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="beaa8-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="beaa8-157">คุณสามารถใช้ประเภทตามลำดับชั้นที่ด้านซ้ายหรือตัวกรองที่อยู่ด้านบนของรายการเพื่อกรองข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="beaa8-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="beaa8-158">คลิกเพิ่มลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="beaa8-158">Click Add to lines.</span></span>
8. <span data-ttu-id="beaa8-159">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="beaa8-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="beaa8-160">คลิกเพิ่มลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="beaa8-160">Click Add to lines.</span></span>
10. <span data-ttu-id="beaa8-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="beaa8-161">Click OK.</span></span>


